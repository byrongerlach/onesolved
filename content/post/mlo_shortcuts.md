Keyboard Shortcuts
The MLO team pays special attention to accelerating application usage. There are keyboard shortcuts for frequently used operations. The most important keyboard shortcuts are listed below.
 
		Note: Not all keyboard shortcuts are listed here. Please investigate the application menu, local menus, and hints to find out the shortcut for the operation you need.
 
Shortcut	Action or command
Alt+F1	Properties pane open/close 
Alt+1	Toggle between Task List and Task Notes (Contexts List and Contexts Notes)
Alt+2	General properties section open/close
Alt+3	Timing & Reminder properties section open/close
Alt+4	Effort properties section open/close
Alt+5	Project properties section open/close
Alt+6	Task Statistics properties section open/close
F6	Collapse entire outline or To-Do lists
F7	Expand entire outline or To-Do list
Alt+Shift+Left	Rearrange tasks in the outline
Alt+Shift+Right
Alt+Shift+Up
Alt+Shift+Down
Ctrl+Up	Select next/previous visible task in Outline/To-Do without focusing this task list. The current active control will be still focused during task change by this shortcut. Useful to iterate quickly through the list of tasks and change specific task parameter.
Ctrl+Down
Alt+Up	Select next/previous sibling in the current outline
Alt+Down
Ctrl+Alt+Up	Select next/previous project in the current outline
Ctrl+Alt+Down
Ctrl+`	Collapse/Expand all subtasks of the current task
Shift+Ctrl+0	Set quick bookmark #1, 2...9 to a task in the outline 
Shift+Ctrl+1
...
Shift+Ctrl+9
Ctrl+0	Go to bookmark #1, 2...9 in the outline 
Ctrl+1
...
Ctrl+9
 
Ctrl+<	Go to previous/next bookmark set
Ctrl+>
Ctrl+Alt+>	Open Bookmarks dialog
Alt+C	Edit Context for a task
Alt+L	Select Context for a task from the list
Alt+V	Select View in the Outline or To-Do tab
Alt+P	Toggle complete subtasks in order 
Alt+Y	Toggle hide in todo 
Alt+R	Reminder
Alt+J	Toggle "This is a Project"
Alt+X	Max time required 
Alt+W	Toggle Weekly goal 
Alt+A	Toggle context Filter selector / To-Do list 
Alt+D	Set Due Date for a task
Ctrl+= 	Increase/decrease task due date by one day.
Ctrl+-
Ctrl+Alt= 	Increase/decrease task due date by one week.
Ctrl+Alt-
Insert	Create a task (Context)
Alt+Insert	Create a subtask
Ctrl+Del	Delete a task (Context)
Ctrl+R	Zoom-in
Ctrl+Alt+R	Zoom-out
Alt+Left	Jump back/forward to previously selected task
Alt+Right	Jump forward to the next task in history
	
	
	
	
	
	
	
	
	The list of the shortcuts is not complete here. Please discover other shortcuts in the application main menu, local menus, and hints to the commands. In task properties, press Alt to see underlined chars which are the shortcuts for corresponding commands.
		 
		Note: You can change the default keys or key combinations assigned to the common MLO functions or commands. For more information, see Hot Keys.




Input parsing
MLO can parse -or interpret- the text you enter in some text input fields. For example you can enter "in 30 min" or "next Friday at 2pm" in date and time pickers. 
 
In the Rapid Task Entry dialog, you can type "Call Bob about the party tomorrow at 3pm remind 10 min in advance". The task "Call Bob about the party" will be added to the outline with corresponding parameters parsed from the rest of the input.
 
You can also parse the task caption entered to the Outliner if you press Alt+Enter instead of Enter.
 
 
Parsing input in date time pickers
Date time pickers like Start, Due and Reminder can parse user's input and convert it to valid date and time. Days of the week and months can be used in English and your current locale. 
 
Here are the examples of valid input which can be converted to date and time:
 
tomorrow 3pm
in 5 days
Friday        (nearest Friday in future)
next Friday        (next Friday after nearest Friday in future)
Tue 11:20
Jan26
August 26th
Nov 26 08
in 3 weeks 2pm
in 3 weeks Fri
in 30 min
in 2 months
today in 1h 25 min
next year
3-26-2008
26-3-2008
 
 
Parsing input in Rapid Task Entry dialog and Outline
 
If you want MLO to parse date and time from your input you should enter your tasks using the following pattern: 
<What?> <When?> 
 
Examples: 
Organize party with my friends 5/22 
Call Jim tomorrow 4pm 
Prepare report for Bob 15:10 22/5 
 
		 
		Note: Parsing is deactivated in Rapid Task Entry dialog by default. To activate it you should open this dialog, click Options button and check Parse input like... check box.
		 
		Note: Date and time is parsed according to the rules applied for date time pickers described above.
		 
		Tip: use –s or –start to put the date only in the start date field when parsing in RTE or the Outline: "Call Bob tomorrow -s"
		 
		Tip: use –d or –due to put the date only in the due date field when parsing in RTE or the Outline: "Send report -due in 5d"
		 
		Tip: If MLO fails to parse your input correctly press Ctrl+Z in the main window to return the original text to RTE change the text and try again.
 
 
Reminder 
If you add reserved words "remind" or "reminder", or the abbreviation "rmd" to the phrase, the reminder will be set in MLO. 
The pattern: 
<What?> [<When?>] remind[er] I rmd [<When?>] 
 
 
Examples: 
Organize party with my friends May 22 reminder May 21 3pm 
Call Jim in 3 days at 4pm remind 10 min in advance 
Send report to Bob in 3 days remind me tomorrow 2pm
Call Jim tomorrow at 4pm remind me 
Send report rmd 3pm
 
 
Context
If you add reserved words "context" or "@" to the phrase the contexts will be added to the task. The contexts should be separated by semicolons (;) 
The pattern:
<What?> [<When?>] [remind[er]] [<When?>] [context | @] <context1>; <context2>; <context3>
 
Examples:
Call Jim tomorrow context @office; @calls
Send report in 3 days remind tomorrow 10:00 @ ProjectX 
 
		Tip: If the context starts with "@" you can skip the reserved words. In this case the first word which starts with "@" is interpreted as a context.
		Example:
		Call Jim tomorrow @office; @calls
		Tip: you can use the +@ switch to add contexts to the task (not replace them).  Example: “Call Bob +@ phone” or "Buy ticket +@internet"
 
 
More complex inputs 
You can use short and long week day names and names of months in English or in your current locale. You can also use phrases like "today", "tomorrow", "next Friday", "in 3 weeks",  "in 4 weeks Fri", "in 3 years", "in 2 months 1 week  4 days" etc. You can use abbreviation: d=day(s); w=week(s); m=month(s) or = minute(s); min=minute(s); h, hr, hrs = hour(s). 
 
Examples: 
Send report next Tue 11am 
Send report in 3 weeks Monday 15:30 remind me tomorrow 10am 
Send report Jan 10 
Send report February8 2009 context 
Send report in 1 month 2 weeks 1 day @ ProjectX; Reports
Send report in 1 m 2 w 1 d 
Send report remind me in 3 hrs 
 
 
Reserved words 
MLO tries to interpret your input and separate reserved words from the task caption. However it is not always possible. For example if you use numbers in the task caption, it may be interpreted as a date, or you may want to use reserved words "reminder", "context" etc.  If MLO fails to correctly parse your entry, use quotation marks (") to separate you task caption from parameters that should be parsed. 
 
Examples: 
"Inform about meeting with Bob tomorrow 16:00" tomorrow at 16:00 remind me 10 m 
"Send next reminder to Jim" tomorrow 
 
The text inside quotation marks is not parsed and placed in the task caption.
 
Complete list of reserved words:
1) The week day names (short and log) in English and in your current locale (Mon, Monday, .. Sun, Sunday)
2) Names of months (short and log) in English and your current locale (Jan, January... Dec, December)
3) Numbers (0, 1..9)
4) The following words:
context,@, remind, reminder, next, in, after, before, day, days, d, month, months, m, year, years, y, week, weeks, 
tomorrow, w, am, pm, p, h, hr, hrs, hours, hour, minute, minutes, min, mins, today, now
 
 
Additional parsing switches
Additional parsing switches can be used in Rapid Task Entry or Outline parsing
 
Additional parsing switches:
-i1 -i2 … -i5 : set Importance for the task 1=min .. 5=max
-u1 -u2 … -u5 : set Urgency  for the task 1=min .. 5=max
-e1 -e2 … -e5 : set Effort for the task 1=min .. 5=max
-t<time> : set time required for the task. Examples –t10; -t2h15min
-tmax<time> : set time required max for the task
-l<time> : set lead time for the task. Example: -l2d; -l3d15m
-s or -start : the date will be placed in the Start field
-d or -due : the date will be placed in the Due field
-h : hide task in todo
-o : complete subtasks in order
-p : set IsProject option for the task
-f : set Folder option for the task
-g : set Goal option for the task
-fl<FlagName>: set flag for the task. Example: "Buy umbrella -flGreen"
-c<Color>: set font color for the task
-toprj<ProjectName> or -toprj=<ProjectName> : move task to a project. Example: "Paint wall -toprjHome"
-tofld<FolderName> or -tofld=<FolderName> : move task to a folder
-to<TaskName> or -to=<TaskName> : move task to make it a subtask of specified task.
+@: add contexts to the task (not replace).  Example: “Call Bob +@ phone”
-star or -* : set starred to the task. Example: "Call Mike tomorrow -star"
 
 
 
Example. Type this in the outline and press Alt+Enter when in-place editor is active:
“Call Katrin -t10 tomorrow 3p remind me 15 min in advance @calls -i1 -e4 -cr”
As a result of the parsing a task with the following parameters will be added to your outline:
Caption: “Call Katrin”, 
Due Date: tomorrow 3:00pm, 
Reminder 2:45pm,
Context: @calls, 
Time Required 10min, 
Importance Max, 
Effort: More,
Color: Red. 
 
 
Parsing task caption in the Outliner
You can benefit from input parsing in the Task Outliner as well. To parse the task caption entered in the Outliner, press Alt+Enter while you are in in-place editor mode. The task caption will be parsed according to the rules described above.
 
		Tip: If MLO fails to parse your input press Ctrl+Z several times to return to the initial caption of the task.
