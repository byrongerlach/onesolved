
## Using Templates in Visual Studio 

tm


attachedProperty: 

public static readonly DependencyProperty propertyNameProperty = DependencyProperty.RegisterAttached(
            "propertyName",
            typeof(propertyType),
            typeof(TestInstanceIndicatorTest),
            new PropertyMetadata(default(propertyType)));

        public static void SetpropertyName(DependencyObject element, propertyType value)
        {
            element.SetValue(propertyNameProperty, value);
        }

        public static propertyType GetpropertyName(DependencyObject element)
        {
            return (propertyType)element.GetValue(propertyNameProperty);
        }


  Attribute: 

         [AttributeUsage(AttributeTargets.All, Inherited = false, AllowMultiple = true)]
        sealed class MyAttribute : Attribute
        {
            // See the attribute guidelines at 
            //  http://go.microsoft.com/fwlink/?LinkId=85236
            readonly string positionalString;

            // This is a positional argument
            public MyAttribute(string positionalString)
            {
                this.positionalString = positionalString;

                // TODO: Implement code here
                throw new NotImplementedException();
            }

            public string PositionalString { get; private set; }

            // This is a named argument
            public int NamedInt { get; set; }
        }


ctx wil give you the file name, or namespace name.

cw: Console.WriteLine


dependencyProperty:

 public static readonly DependencyProperty PropertyTypeProperty = DependencyProperty.Register("PropertyType", typeof(propertyType), typeof(TestInstanceIndicatorTest), new PropertyMetadata(default(propertyType)));

        public propertyType PropertyType
        {
            get
            {
                return (propertyType)GetValue(PropertyTypeProperty);
            }
            set
            {
                SetValue(PropertyTypeProperty, value);
            }
        }

e: enum

i: interface


