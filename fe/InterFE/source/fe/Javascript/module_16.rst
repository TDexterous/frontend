Module 16 : JAVASCRIPT - ES 6
=============================

Class
-----

- JavaScript classes, introduced in ECMAScript 2015 or ES 6, Classes are in fact "special functions".
- There are two way to define class in JavaScript using class keyword:-

1. Class Declaration 
2. Class Expression

1. Class Declaration
^^^^^^^^^^^^^^^^^^^^

Syntax:

.. code-block:: javascript

    class class_name {
        constructor ( ) {
            Properties
        }
        Methods
    }

2. Class Expression
^^^^^^^^^^^^^^^^^^^

- Class expressions can be named or unnamed.

**unnamed Syntax:**

.. code-block:: javascript

    var Mobile = class {
      constructor( ) {
             Properties
        }
    };

**named Syntax:**

.. code-block:: javascript

    var Mobile = class Mobile2 {
    constructor( ) {
                Properties 
            }
    };

Constructor
-----------

- The constructor method is a special method for creating and initializing an object created within a class.
- There can be only one special method with the name "constructor" in a class.

Syntax:

.. code-block:: javascript

    class class_name {
        constructor ( ) {
            Properties
        }
    }

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
            /*
                var Mobile = function (){
                    this.model = 'Galaxy';
                    this.show = function() {
                        return "Class using Constructor";
                    }
                }
                // Prototype Member
                Mobile.prototype.display = function () {
                    return "Prototype Method";
                }
            */
                class Mobile {
                    constructor() {
                    // Instance Member
                        this.a = 12;
                        this.show = function () {
                            return "Instance Method";
                        };
                    }
                    // Prototype Member
                    display() {
                        return "Prototype Method";
                    }
                }
                
                var samsung = new Mobile ();
                document.write(samsung.display());	
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Prototype Method

Default Constructor
-------------------

- if you do not specify a constructor method a default constructor is used.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
            // Class Declaration 
                class Mobile {
                    display() {
                        return "Prototype Member";
                    }
                }
                
                var nokia = new Mobile();
                document.write(nokia.display());
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Prototype Member

Parameterized Constructor
-------------------------

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
            // Class Declaration 
                class Mobile {
                    constructor(model_no, color) {
                        this.model = model_no;
                        this.clr = color;
                    }
                    show() {
                        return this.model + " Price Rs. 3000 " + this.clr;
                    }
                }
                
                var nokia = new Mobile('Galaxy', 'White');
                var lg = new Mobile('Note4', 'black');
                document.write(nokia.show() + "<br>");
                document.write(lg.show());
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Galaxy Price Rs. 3000 White
    Note4 Price Rs. 3000 black

Class Hoisting
--------------

- Class Declarations and Class Expression are not hoisted.
- You first need to declare your class and then access it.

Ex-1:

.. code-block:: javascript
   :linenos:

    class Mobile {

    }

    var nokia = new Mobile( ) ;

Ex-2:

.. code-block:: javascript
   :linenos:

    var nokia = new Mobile ( );

    class Mobile {

    }

- Ex-1 is correct & Ex-2 is wrong.

Inheritance
-----------

.. image:: D:/Courses/Javascript_images/inheritance.png
   :width: 600

Class Inheritance
^^^^^^^^^^^^^^^^^

- The extends keyword is used in class declarations or class expressions to create a class which is a child of another class.
- The extends keyword can be used to subclass custom classes as well as built-in objects.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                class Father {
                    showFMoney(){
                        return "Father Money <br>";
                    }
                }
                class Son extends Father {
                    showSMoney(){
                        return "Son Money <br>";
                    }
                }
                
                class GrandSon extends Son {
                    showGMoney() {
                        return "GrandSon Money";
                    }
                }
                var g = new GrandSon();
                document.write(g.showFMoney());
                document.write(g.showSMoney());
                document.write(g.showGMoney());
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Father Money
    Son Money
    GrandSon Money

**Inherit Built-in Object**

- Date
- String
- Array

Super Method
^^^^^^^^^^^^

- Super ( ) is used to initialize parent class constructor.
- If there is a constructor present in subclass, it needs to first call super() before using "this".
- A constructor can use the super keyword to call the constructor of a parent class.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                class Father {
                    constructor(money){
                        this.Fmoney = money;
                    }
                    showFMoney(){
                        return this.Fmoney + " Father Money <br>";
                    }
                }
                class Son extends Father {
                    constructor(money) {
                        super(money);
                        this.a = 12;
                    }
                    showSMoney(){
                        return "Son Money <br>";
                    }
                }
                
                var s = new Son(10000);
                document.write(s.showFMoney());
                document.write(s.showSMoney());
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    10000 Father Money
    Son Money

Method Overriding
^^^^^^^^^^^^^^^^^

- Same function name with different implementation.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                class Father {
                    show(){
                        return "Super Class <br>";
                    }
                }
                
                class Son extends Father {
                    show(){
                        return "Sub Class";
                    }
                }
                var s = new Son();
                document.write(s.show());
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Sub Class

Static Method
^^^^^^^^^^^^^

- The static keyword is used to define a static method for a class.
- Static methods are called without creating object and cannot be called through a class instance (object).
- Static methods are often used to create utility functions for an application.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                class Mobile {
                    static disp(){
                        return "Static Method";
                    }
                }
                document.write(Mobile.disp());
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Static Method

