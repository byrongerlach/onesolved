---
title: "MS SQL Server Tips"
date: 2018-01-14
tags: ["MS SQL Server"]
categories: ["commands and shortcuts"]
draft: false
---

# Get DB Table Size

The following will list the size of each table: 

```
SELECT 
    s.Name AS SchemaName,
    t.NAME AS TableName,
    p.rows AS RowCounts,
    SUM(a.total_pages) * 8 AS TotalSpaceKB, 
    SUM(a.used_pages) * 8 AS UsedSpaceKB, 
    (SUM(a.total_pages) - SUM(a.used_pages)) * 8 AS UnusedSpaceKB
FROM 
    sys.tables t
INNER JOIN 
    sys.schemas s ON s.schema_id = t.schema_id
INNER JOIN      
    sys.indexes i ON t.OBJECT_ID = i.object_id
INNER JOIN 
    sys.partitions p ON i.object_id = p.OBJECT_ID AND i.index_id = p.index_id
INNER JOIN 
    sys.allocation_units a ON p.partition_id = a.container_id
WHERE 
    t.NAME NOT LIKE 'dt%'    -- filter out system tables for diagramming
    AND t.is_ms_shipped = 0
    AND i.OBJECT_ID > 255 
GROUP BY 
    t.Name, s.Name, p.Rows
ORDER BY 
    s.Name, t.Name
```

The above is discussed [here](http://stackoverflow.com/questions/1443704/query-to-list-number-of-records-in-each-table-in-a-database).

# Get Referenced DB Entities

The following will show what DB entities are referenced:

```
USE DB_NAME;

SELECT referencing_schema_name, referencing_entity_name, referencing_id, referencing_class_desc, is_caller_dependent
FROM sys.dm_sql_referencing_entities ('NAMESPACE.FIELD_NAME', 'OBJECT');
```
The above is discussed [here](http://msdn.microsoft.com/en-us/library/bb630351(v=sql.100).aspx)

# Get Row Counts from Tables

select t.name TableName, i.rows Records
from sysobjects t, sysindexes i
where t.xtype = 'U' and i.id = t.id and i.indid in (0,1)
order by TableName;

The above is discussed [here](https://stackoverflow.com/questions/1443704/query-to-list-number-of-records-in-each-table-in-a-database) and [here](http://www.sqlteam.com/forums/topic.asp?TOPIC_ID=21021).