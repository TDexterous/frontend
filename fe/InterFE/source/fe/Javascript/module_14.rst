Module 14 : JAVASCRIPT - Objects
================================

Objects In Javascript
---------------------

- An object is a collection of properties, and a property is an association between a name (or key) and a value.
- A property's value can be a function, in which case the property is known as a method.
- In addition to objects that are predefined in the browser, you can define your own objects.

Type of Objects
---------------

1. **User-defined Objects** - These are custom objects created by the programmer to bring structure and consistency to a particular programming task.
2. **Native Objects** - These are provided by the JavaScript language itself like String, Number, Boolean, Function, Date, Object, Array, Math, RegExp, Error as well as object that allow creation of user-defined objects and composite types.
3. **Host Objects** - These objects are not specified as part of the JavaScript language but that are supported by most host environments, typically browsers like window, navigator.
4. **Document Objects** - These are part of the Document Object Model (DOM), as defined by the W3C. These objects presents present the programmer with a structured interface to HTML and XML documents. Access to the document objects is provided by the browser via the document property of the window object (window.document).

Declaration and initialization of Object
----------------------------------------

1) Using Object Literal
^^^^^^^^^^^^^^^^^^^^^^^

Syntax:

.. code-block:: javascript
    
    var object_name = { };

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var fees = { };		// Declaring empty object
                fees['Rahul'] = 100;	// initializing 
                fees['Sumit'] = 200;
                fees['Rohan'] = 300;
            /*
                fees.Rahul = 100;
                fees.Sumit = 200;
                fees.Rohan = 300;
            */
                document.write(fees['Sumit']);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    200

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var fees = { };	
                fees['Rahul'] = 100;
                fees['total'] = function () {return(100+200+300);};
            // fees.total = function(){return(100+200+300);};
                document.write(fees.total());
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    600

Syntax-2:

.. code-block:: javascript

    var object_name = {key1:value1, key2:value2, key_n:value_n};

Ex-3:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var fees = {Rahul:100, Sumit:200, Rohan:300};
            /*
                var fees = {
                            Rahul:100, 
                            Sumit:200, 
                            Rohan:300
                        };
            */
                document.write(fees['Rahul']);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    100

Syntax-3:

.. code-block:: javascript

    var object_name = {key1:value1, key2:value2, key_n:value_n, key: function};

Ex-4:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var fees = {Rahul:100, Sumit:200, Rohan:300, total: function(){return(100+200+300)}};
            /*
                var fees = {
                            Rahul:100, 
                            Sumit:200, 
                            Rohan:300,
                            total: function(){return(100+200+300)}
                        };
            */
                document.write(fees.total());
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    600

2) Using Object Constructor
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Syntax:

.. code-block:: javascript

    var object_name = new Object( );

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var fees = new Object();
                fees['Rahul'] = 100;
                fees['Sumit'] = 200;
                fees['Rohan'] = 300;
            /*
                fees.Rahul = 100;
                fees.Sumit = 200;
                fees.Rohan = 300;
            */	
                document.write(fees['Rahul']);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    100

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var fees = new Object();
                fees['Rahul'] = 100;
                fees['Sumit'] = 200;
                fees['Rohan'] = 300;
                fees['total'] = function (){return(100+200+300);};
            /*
                fees.Rahul = 100;
                fees.Sumit = 200;
                fees.Rohan = 300;
                fees.total = function(){return(100+200+300);};
            */	
                document.write(fees.total());
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    600

Accessing Object Properties
---------------------------

- A property of an object is some piece of named data it contains.
- These are accessed with dot operator applied to an object alternative to the dot operator is the array [ ] operator.

Syntax:

.. code-block:: javascript

    object_name.property_name

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var fees = {Rahul:100, Sumit:200, Rohan:300};
                document.write(fees['Rahul'] + "<br>");
                document.write(fees["Rahul"]  + "<br>");
                document.write(fees.Rahul);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    100
    100
    100

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var fees = {Rahul:100, "Super Man": 400};
                document.write(fees['Super Man'] + "<br>");
                document.write(fees["Super Man"]  + "<br>");
                // document.write(fees.Super Man); We Cannt access multiword key by dot notation
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    400
    400

Accessing Object Methods
------------------------

- Object members that are functions are called methods.
- These are accessed with dot operator applied to an object alternative to the dot operator is the array [ ] operator.

Syntax:

.. code-block:: javascript

    object_name.Method_name( );

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var fees = {
                    Rahul: 100, 
                    Sumit: 200, 
                    Rohan: 300, 
                    total: function ( ) { return(100+200+300); }			
                };
                document.write(fees.total());
            // document.write(fees['total']());
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    600

Adding Object Properties & Methods
----------------------------------

Syntax:

.. code-block:: javascript

    Object_name.Property_name = value;
    Object_name['Property_name'] = value;

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var fees = {Rahul:100, Sumit:200};
                
                document.write(fees.Rahul + " "+ fees.Sumit + "<br>");
                
                fees.Sonam = 600;	// fees.['Sonam'] = 600;
                
                document.write(fees.Sonam + " " + fees.Rahul + " "+ fees.Sumit + "<br>");
                
                fees.show = function () {};
                
                console.log(fees);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/object.png
   :width: 800

Deleting Properties
-------------------

- Delete operator is used to delete instance properties.

Syntax:

.. code-block:: javascript

    delete object_name.property_name

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var fees = {Rahul:100, Sumit:200};
                
                document.write(fees.Rahul + " "+ fees.Sumit + "<br>");
                
                delete fees.Rahul;

                document.write(fees.Rahul + " "+ fees.Sumit);
                
                console.log(fees);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/object_1.png
   :width: 800

After removal with delete operator, the property has the undefined value. 

Factory Function
----------------

- When a function returns an object, we call it a factory function.
- It can produce object instance without new keyword or classes.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function mobile( ) {
                    return {
                        model: 'Galaxy',
                        price: function(){return "Price Rs. 3000";} 
                    };
                }
                var samsung = mobile( );
                document.write(samsung.model + " "+samsung.price( ));
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Galaxy Price Rs. 3000

Factory Function with Parameter
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function mobile(model_no) {
                    return {
                        model: model_no,
                        price: function(){
                            return "Price is Rs. 3000";
                        } 
                    };
                }
                var samsung = mobile('galaxy');
                var nokia = mobile('3310');
                document.write(samsung.model + " "+samsung.price( ) + "<br>");
                document.write(nokia.model + " "+nokia.price( ));
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    galaxy Price is Rs. 3000
    3310 Price is Rs. 3000

Constructor
-----------

- Object instance are created with constructor, which are basically special function that prepare new instance of an object for use.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function Mobile(){
                    this.model = '3310';
                    this.price = function(){
                        document.write(this.model + " Price Rs. 3000");
                    }
                }
                var samsung = new Mobile();
                samsung.price();
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    3310 Price Rs. 3000

Constructor with Parameter
^^^^^^^^^^^^^^^^^^^^^^^^^^

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function Mobile(model_no){
                    this.model = model_no;
                    this.price = function(){
                        document.write(this.model + " Price Rs.3000 <br>");
                    }
                }
                var samsung = new Mobile('Galaxy');
                var nokia = new Mobile('3310');
                samsung.price();
                nokia.price();
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Galaxy Price Rs.3000
    3310 Price Rs.3000

Check Properties Exist
----------------------

1. typeof operator
^^^^^^^^^^^^^^^^^^

Syntax:

.. code-block:: javascript

    if (typeof object_name.key !== 'undefined')

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function Mobile(model_no){
                    this.model = model_no;
                    this.memory = 4;
                }
                
                var samsung = new Mobile('Galaxy');
                var nokia = new Mobile('3310');
                
                if(typeof nokia.memory !== 'undefined'){
                    document.write("Available");
                } else {
                    document.write("Doesnt Exist");
                }
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Available

2. in operator 
^^^^^^^^^^^^^^

Syntax:

.. code-block:: javascript

    if ('key' in object_name)

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function Mobile(model_no){
                    this.model = model_no;
                    this.memory = 4;
                }
                
                var samsung = new Mobile('Galaxy');
                var nokia = new Mobile('3310');
                
                if('memory' in nokia){
                    document.write("Available");
                } else {
                    document.write("Doesnt Exist");
                }
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Available

3. hasOwnProperty()
^^^^^^^^^^^^^^^^^^^

Syntax:

.. code-block:: javascript

    if (object_name.hasOwnProperty("key"))

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function Mobile(model_no){
                    this.model = model_no;
                    this.color = 'white';
                }
                
                var samsung = new Mobile('Galaxy');
                var nokia = new Mobile('3310');
                
                if(nokia.hasOwnProperty('color')){
                    document.write("Available");
                } else {
                    document.write("Doesnt Exist");
                }
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Available

For in loop
-----------

- The for in loop is used to loop through an object's properties.

Syntax:

.. code-block:: javascript

    for (var variable_name in object_name){
        block of statement
    }

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function Mobile(model_no){
                    this.model = model_no;
                    this.color = 'white';
                    this.ram = '4GB';
                    this.price = function(){
                        document.write(this.model + " Price Rs.3000 <br>");
                    };
                }
                var samsung = new Mobile('Galaxy');
                var nokia = new Mobile('3310');
                for(var key in nokia)
                {
                    document.write(nokia[key] + "<br>");
                }
            /* Value with key
                for(var key in nokia)
                {
                    document.write(key + " : " + nokia[key] + "<br>");
                }
            */
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    3310
    white
    4GB
    function(){ document.write(this.model + " Price Rs.3000
    "); }

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function Mobile(model_no){
                    this.model = model_no;
                    this.color = 'white';
                    this.ram = '4GB';
                    this.price = function(){
                        document.write(this.model + " Price Rs.3000 <br>");
                    };
                }
                var samsung = new Mobile('Galaxy');
                var nokia = new Mobile('3310');
            // Method wont display
                for(var key in nokia){
                    if(typeof nokia[key] !== 'function'){
                        document.write(nokia[key] + "<br>");
                    }	
                }
            /* value with key, Method wont display
                for(var key in nokia){
                    if(typeof nokia[key] !== 'function'){
                    document.write(key + " : " + nokia[key] + "<br>"); 
                    }
                }
            */
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    3310
    white
    4GB

Class
-----

- A specific category can be defined as class.

Example:

.. image:: D:/Courses/Javascript_images/class.png
   :width: 800

Defining a Class
^^^^^^^^^^^^^^^^

- We define class in JavaScripts using custom constructor.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var  Mobile = function(model_no, sprice){
                    this.model = model_no;
                    this.color = 'white';
                    this.price = 3000;
                    this.sp = sprice;
                    this.sellingprice = function(){
                        return (this.price + this.sp);
                    };
                    this.data = function(){
                        document.write(" Model No: " + this.model + " Price: " + this.sellingprice());
                    }
                };
                var samsung = new Mobile('Galaxy', 2000);
                var nokia = new Mobile('3310', 1000);
                nokia.data();
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Model No: 3310 Price: 4000

Private Properties and Methods
------------------------------

- Using var or let or const you can create private properties and methods.

Example:

.. code-block:: HTML
   :linenos:

    this.price 
    var price
    let price

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var  Mobile = function(model_no, sprice){
                    this.model = model_no;
                    this.color = 'white';
                    var price = 3000;	// private property
                    this.sp = sprice;
                    // Private Method
                    var show = function() { return "Hello World";};
                };
                var samsung = new Mobile('Galaxy', 2000);
                var nokia = new Mobile('3310', 1000);
                document.write(nokia.price);
                document.write(nokia.show());
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/private_property.png
   :width: 800

- We cannot access private property or method from outside of the class as shown above.
- For accessing private property using Public method below is the example.

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var  Mobile = function(model_no, sprice){
                    this.model = model_no;
                    this.color = 'white';
                    var price = 3000;	// private property
                    this.sp = sprice;
                    // Public Method
                    this.sellingprice = function(){		
                        return (price);
                    };
                };
                var samsung = new Mobile('Galaxy', 2000);
                var nokia = new Mobile('3310', 1000);
                document.write(nokia.price);
                document.write(nokia.sellingprice());
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/private_property_1.png
   :width: 800

