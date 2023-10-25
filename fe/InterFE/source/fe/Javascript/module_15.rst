Module 15 : JAVASCRIPT - Prototype
==================================

What is Prototype?
------------------

- Every object has an internal prototype that gives it its structure.
- This internal prototype is a reference to an object describing the code and data that all objects of that same type will have in common.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var  Mobile = function(model_no){
                    // Instance Member
                    this.model = model_no;
                    this.price = 3000;
                };
                var samsung = new Mobile('Galaxy');
                var nokia = new Mobile('3310');			
                // classname.prototype.key = 'value';
                // Prototype Member
                Mobile.prototype.color = 'white';
                
                document.write(samsung.color);
                console.log(samsung);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/prototype.png
   :width: 800

How to iterate Instance and Prototype Member using for in Loop
--------------------------------------------------------------

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var  Mobile = function(model_no){
                    // Instance Member
                    this.model = model_no;
                    this.price = 3000;
                };
                var samsung = new Mobile('Galaxy');
                var nokia = new Mobile('3310');			
                // classname.prototype.key = 'value';
                // Prototype Member
                Mobile.prototype.color = 'white';
                for (var key in samsung){
                    document.write(key);
                }
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    modelpricecolor

Prototype Object
----------------

- Every object is associated with another Object in JavaScript.

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head >
            <title>Techno Dexterous</title>
        </head>
        <body>
            <p id="myp" class="myclass1" style= "color:yellowgreen;">Paragraph</p>
            <script>
                // It will return Object.prototype
                console.log(Object.prototype);

                // creating an empty object and prototype object of this 
                // object is Object.prototype
                var b = {};

                // We are checking what is the Prototype Object of b which 
                // should be Object.prototype
                // b will inherit all properties of Object.prototype Object
                console.log(Object.getPrototypeOf(b)); 

                // Further check what is the Prototype Object of Object.prototype it should be null
                console.log(Object.getPrototypeOf(Object.prototype)); 

                // Check the above stuff with new operator
                var b1 = new Object();
                console.log(Object.getPrototypeOf(b1));

                // checking with Array
                // First check what is the Array.prototype
                console.log(Array.prototype);

                // creating empty Array Object
                var b2 = new Array();

                // check what is the Prototype of Object b2
                // it will be Array.Prototype
                console.log(Object.getPrototypeOf(b2));

                // Now check what is the Prototype Object of Array.prototype
                console.log(Object.getPrototypeOf(Array.prototype));
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/prototype_1.png
   :width: 800

How Prototype Works
-------------------

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>

    <head>
        <title>Techno Dexterous</title>
    </head>

    <body>
        <script>
            function Mobile(){

            }
            // Mobile is the object created by Function which is actually Function itself
            console.log(Mobile);

            // prototype is a property of Mobile which points to the Prototype Object of Mobile
            console.log(Mobile.prototype);  // it will show Prototype Object of Mobile Function

            // Creating a new Object using new keyword
            var lg = new Mobile();

            // When you create a new object of that function using new keyword JS Engine creates an object and sets a property named __proto__ which points to its function’s prototype object
            console.log(lg.__proto__);                // Mobile.prototype

            // Verifying all stuffs
            console.log(lg.__proto__ === Mobile.prototype);     // true
            console.log(Mobile === lg.__proto__.constructor);      // true
            console.log(Mobile === Mobile.prototype.constructor);   // true
        </script>
    </body>

    </html>

Output:

.. image:: D:/Courses/Javascript_images/prototype_2.png
   :width: 800

Ex-3:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>

    <head>
        <title>Techno Dexterous</title>
    </head>

    <body>
        <script>
            function Mobile(){
            }
            // Creating a new Object using new keyword
            var lg = new Mobile();
            // This will show undefined becoz a is neither defined in the funtion nor in the function's prototype
            // it first checks if lg object have property a as it doesn't have it so it go to its prototype object pointed by __proto__ and ask him if he has property a as it also doesn't have it so finally we receive undefined. This is how it works behind the browser and JS Engine is the responsible for this task
            console.log(lg.a);
        </script>
    </body>

    </html>

Output:

.. image:: D:/Courses/Javascript_images/prototype_3.png
   :width: 800

Ex-4:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>

    <head>
        <title>Techno Dexterous</title>
    </head>

    <body>
        <script>
            function Mobile(){
            }
            // This property is defined in Function's Prototype Object so all Objects will have access to this property and this is just one single property for all objects. It doesn't make copies for objects separately. usually we defined methods as a prototype method member rather than Prototype variable memeber
            Mobile.prototype.a = 10;   

            // Creating a new Object using new keyword
            var lg = new Mobile();

            // It first checks if lg object have property a as it doesn't have it so it go to its prototype object pointed by __proto__ and ask him if he has property a as it has so finally we receive 10. This is how it works behind the browser and JS Engine is the responsible for this task
            console.log(lg.a);
        </script>
    </body>

    </html>

Output:

.. image:: D:/Courses/Javascript_images/prototype_4.png
   :width: 800

Ex-5:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>

    <head>
        <title>Techno Dexterous</title>
    </head>

    <body>
        <script>
            function Mobile(){
                this.a = 20;
            }
            // This property is defined in Function's Prototype Object so all Objects will have access to this property and this is just one single property for all objects. It doesn't make copies for objects separately. usually we defined methods as a prototype method member rather than Prototype variable memeber
            Mobile.prototype.a = 10;   

            // Creating a new Object using new keyword
            var lg = new Mobile();

            // It first checks if lg object have property a as it has so it will return 10 and will stop checking further in the prototype object
            console.log(lg.a);      // 20
        </script>
    </body>

    </html>

Output:

.. image:: D:/Courses/Javascript_images/prototype_5.png
   :width: 800

Prototype Inheritance
---------------------

- Prototype inheritance is a key feature of the JavaScript programming language.
- In JavaScript, objects can inherit properties and methods from other objects through their prototypes.
- This concept is rooted in the prototype-based programming paradigm, which sets JavaScript apart from more traditional class-based languages.

Here's a detailed explanation of prototype inheritance in JavaScript:

1. **Constructor Functions:** In JavaScript, you can create objects using constructor functions. These functions serve as templates for creating multiple objects with shared properties and methods. Constructors are defined using regular functions and are usually named with an initial capital letter.
2. **Prototype Object:** Each constructor function has a property called prototype, which points to an object. This object is the prototype of objects created using that constructor function. Properties and methods added to the prototype are shared among all instances created from the constructor.
3. **Instance Objects:** When you create an instance of an object using a constructor, the new instance inherits properties and methods from the constructor's prototype.
4. **Property Lookup:** When you access a property or method on an instance, JavaScript first checks if the property exists directly on the instance. If not, it looks for the property in the instance's prototype (the prototype of the constructor).
5. **Prototype Chain:** If the property is not found in the prototype, JavaScript continues the search in the prototype's prototype, forming a chain. This chain of prototypes is known as the prototype chain.
6. **Object Creation and Inheritance:**

.. code-block:: javascript
   :linenos:

    // Constructor function
    function Person(name) {
        this.name = name;
    }

    // Adding a method to the prototype
    Person.prototype.sayHello = function() {
        console.log(`Hello, my name is ${this.name}`);
    };

    // Creating instances
    const person1 = new Person("Alice");
    const person2 = new Person("Bob");

    person1.sayHello(); // Output: Hello, my name is Alice
    person2.sayHello(); // Output: Hello, my name is Bob

7. **Modifying Prototypes:** You can modify the prototype of a constructor even after instances have been created. The changes will be reflected in all existing and future instances.
8. **Prototype-based Nature:** Unlike class-based languages, JavaScript's inheritance model is based on prototypes. JavaScript doesn't have traditional classes until the introduction of class syntax in ECMAScript 2015 (ES6), which is essentially syntactic sugar over prototype-based inheritance.

In modern JavaScript, you can also use the class syntax to define constructors and work with inheritance. Under the hood, this syntax still relies on prototypes for inheritance.

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>

    <head>
        <title>Techno Dexterous</title>
    </head>

    <body>
        <script>
            // Super Class
            var Mobile = function(){
                this.a = 10;
            }
            
            // Prototype Property of Mobile
            Mobile.prototype.z = 30;

            // Sub Class
            var Samsung = function(){
                // It initialize and call Super class constructor without this you can not access super class property using sub class object
                Mobile.call(this);      
                this.b = 20;
            }

            // Prototype Inheritance
            Samsung.prototype = Object.create(Mobile.prototype);
            Samsung.prototype.constructor = Samsung;

            var s = new Samsung();
            document.write(s.a + "<br>");
            document.write(s.b + "<br>");
            document.write(s.z + "<br>");
        </script>
    </body>

    </html>

Output:

.. code-block:: HTML

    10
    20
    30

One Super & Two SubClasses
^^^^^^^^^^^^^^^^^^^^^^^^^^

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Super Class
                var Mobile = function(){

                }
                Mobile.prototype.getModel = function(){ return this.model; }

                // Sub Class
                var Samsung = function(model, price){
                    this.model = model;
                    this.price = price;
                }

                // Sub Class
                var Lenovo = function(model){
                    this.model = model;
                }
                
                // inheritance 
                Samsung.prototype = Object.create(Mobile.prototype);
                Samsung.prototype.constructor = Samsung;
                Lenovo.prototype = Object.create(Mobile.prototype);
                Lenovo.prototype.constructor = Lenovo;

                // always write child prototype after inheritance else it wont work
                Samsung.prototype.getPrice = function(){ return this.price; }

                var galaxy = new Samsung("Galaxy", 3000);
                var phab2 = new Lenovo('Phab 2')

                console.log(galaxy.getModel());
                console.log(galaxy.getPrice());
                console.log(phab2.getModel());
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/prototype_6.png
   :width: 800

Create Function For Prototype Inheritance
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Ex-3:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>

    <head>
        <title>Techno Dexterous</title>
    </head>

    <body>
        <script>
            // Function for inheritance
            function extend(Child, Parent) {
                Child.prototype = Object.create(Parent.prototype);
                Child.prototype.constructor = Child;
            }
            var Mobile = function () {

            }
            Mobile.prototype.getModel = function () {
                return this.model;
            }

            var Samsung = function (model, price) {
                this.model = model;
                this.price = price;
            }

            var Lenovo = function (model) {
                this.model = model;
            }

            // inheritance 
            extend(Samsung, Mobile);
            extend(Lenovo, Mobile);

            // always write child prototype after inheritance else it wont work
            Samsung.prototype.getPrice = function () {
                return this.price;
            }

            var galaxy = new Samsung("Galaxy", 3000);
            var phab2 = new Lenovo('Phab 2')

            console.log(galaxy.getModel());
            console.log(galaxy.getPrice());
            console.log(phab2.getModel());
        </script>
    </body>

    </html>

Output:

.. image:: D:/Courses/Javascript_images/prototype_7.png
   :width: 800

Call Super In SubClass
^^^^^^^^^^^^^^^^^^^^^^

Ex-4:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var Mobile = function(model){
                        this.model = model;
                }
                Mobile.prototype.getModel = function(){ return this.model; }

                var Samsung = function(model, price){
                    Mobile.call(this, model)
                    this.price = price;
                }

                // inheritance 
                Samsung.prototype = Object.create(Mobile.prototype);
                Samsung.prototype.constructor = Samsung;

                var galaxy = new Samsung("Galaxy", 3000);

                console.log(galaxy.getModel());
                console.log(galaxy.model);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/prototype_8.png
   :width: 800

Method Overriding
-----------------

- In JavaScript, method overriding is a concept where a subclass provides a specific implementation for a method that is already defined in its superclass.
- This allows you to customize or extend the behavior of the superclass method in the subclass.
- JavaScript is a prototype-based language, so there is no explicit "class" keyword for defining classes and methods, but you can achieve method overriding using prototypes or modern class syntax introduced in ES6.

Here's how method overriding can be done in JavaScript using prototype-based approach:

**Using Prototype-based Inheritance:**

Ex-1:

.. code-block:: javascript
   :linenos:

    // Define a superclass
    function Animal(name) {
    this.name = name;
    }

    // Add a method to the superclass
    Animal.prototype.makeSound = function() {
    console.log("Animal makes a sound");
    };

    // Define a subclass that inherits from Animal
    function Dog(name) {
    Animal.call(this, name);
    }

    // Inherit methods from the superclass
    Dog.prototype = Object.create(Animal.prototype);

    // Override the makeSound method in the subclass
    Dog.prototype.makeSound = function() {
    console.log("Dog barks");
    };

    // Create instances of Animal and Dog
    const genericAnimal = new Animal("Generic Animal");
    const myDog = new Dog("Buddy");

    // Call the overridden method
    genericAnimal.makeSound(); // Output: Animal makes a sound
    myDog.makeSound(); // Output: Dog barks

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Function for inheritance
                function extend(Child, Parent){
                    Child.prototype = Object.create(Parent.prototype);
                    Child.prototype.constructor = Child;
                }
                
                // Super Class
                var Mobile = function() {
                }
                // Prototype Member
                Mobile.prototype.show = function(){
                    return "Super Class Method";
                }
                
                // Sub Class
                var Samsung = function(){
                }
                
                // sub class Samsung extending super class Mobile
                extend(Samsung, Mobile);
                
                // Prototype Member for Sub Class
                Samsung.prototype.show = function(){
                    return "Sub Class Method";
                }
                
                // Creating object of sub class Samsung
                var sam = new Samsung();
                
                // Accessing super class property model
                // using sub class object
                document.write(sam.show());	
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Sub Class Method

MultiLevel Inheritance
----------------------

- Multi-level inheritance in JavaScript refers to the ability to create a chain of objects where each object inherits properties and methods from the object immediately preceding it in the chain.
- This allows you to create a hierarchy of objects with varying levels of specialization and shared behaviors.
- However, it's important to note that JavaScript uses prototype-based inheritance, which is different from classical class-based inheritance found in some other programming languages.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>

    <head>
        <title>Techno Dexterous</title>
    </head>

    <body>
        <script>
            // Super Class
            var Mobile = function(){
                this.a = 10;
            }
            
            // Prototype Property of Mobile
            Mobile.prototype.z = 30;

            // Sub Class
            var Samsung = function(){
                // It calls Super class constructor and initialize property without this you can not access super class property using sub class object
                Mobile.call(this);      
                this.b = 20;
            }

            var Galaxy = function(){
                Samsung.call(this);
                this.c = 100;
            }

            // Prototype Inheritance
            Samsung.prototype = Object.create(Mobile.prototype);
            Samsung.prototype.constructor = Samsung;

            Galaxy.prototype = Object.create(Samsung.prototype);
            Galaxy.prototype.constructor = Galaxy;

            var m = new Mobile();
            var s = new Samsung();
            var g = new Galaxy();

            document.write("Galaxy Object can access <br>")
            document.write("Mobile A: " + g.a + "<br>");
            document.write("Samsung B: " + g.b + "<br> ");
            document.write("Mobile Prototype Z: " + g.z + "<br>");
            document.write("Galaxy C: " + g.c + "<br> <br>");

            document.write("Samsung Object can access <br>");
            document.write("Mobile A: " + s.a + "<br>");
            document.write("Samsung B: " + s.b + "<br> ");
            document.write("Mobile Prototype Z: " + s.z + "<br>");
            document.write("Galaxy C: " + s.c + "<br><br>");

            document.write("Mobile Object can access <br>");
            document.write("Mobile A: " + m.a + "<br>");
            document.write("Samsung B: " + m.b + "<br> ");
            document.write("Mobile Prototype Z: " + m.z + "<br>");
            document.write("Galaxy C: " + m.c + "<br><br>");
        </script>
    </body>

    </html>

Output:

.. image:: D:/Courses/Javascript_images/prototype_9.png
   :width: 800

Composition or Mixins
---------------------

- Composition and mixins in JavaScript are techniques for building flexible and reusable code by combining or "mixing in" functionality from multiple sources, often without creating deep class hierarchies.
- These approaches provide an alternative to traditional class-based inheritance and can lead to more modular and maintainable code.

1. Composition
^^^^^^^^^^^^^^

- Composition involves creating objects by combining or composing multiple simpler objects to achieve a desired functionality.
- It's the idea of assembling smaller building blocks into a larger whole.

Here's an example using composition:

Ex:

.. code-block:: javascript
   :linenos:

    function canSwimMixin(obj) {
    obj.swim = function () {
        console.log(`${this.name} is swimming.`);
    };
    }

    function canFlyMixin(obj) {
    obj.fly = function () {
        console.log(`${this.name} is flying.`);
    };
    }

    const duck = { name: 'Duck' };
    const fish = { name: 'Fish' };

    canSwimMixin(duck);
    canFlyMixin(duck);
    canSwimMixin(fish);

    duck.swim(); // Duck is swimming.
    duck.fly();  // Duck is flying.
    fish.swim(); // Fish is swimming.

In this example, canSwimMixin and canFlyMixin are functions that add specific behaviors to objects duck and fish by simply mixing in those behaviors.

2. Mixins
^^^^^^^^^

- Mixins are pre-defined sets of functionality that can be easily mixed into objects or classes to enhance their capabilities.
- They are typically implemented as objects or functions that extend the properties and methods of the target object or class.

Here's an example using mixins:

Ex:

.. code-block:: javascript
   :linenos:

    const canSwimMixin = {
    swim() {
        console.log(`${this.name} is swimming.`);
    },
    };

    const canFlyMixin = {
    fly() {
        console.log(`${this.name} is flying.`);
    },
    };

    class Animal {
    constructor(name) {
        this.name = name;
    }
    }

    Object.assign(Animal.prototype, canSwimMixin);

    class Bird extends Animal {}

    Object.assign(Bird.prototype, canFlyMixin);

    const duck = new Bird('Duck');
    const fish = new Animal('Fish');

    duck.fly();  // Duck is flying.
    fish.swim(); // Fish is swimming.

In this example, canSwimMixin and canFlyMixin are objects that contain specific behaviors. These behaviors are mixed into the Animal and Bird classes using Object.assign.

Composition With Object Literal
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
                // Composition or Mixins
                // Object.assign(target, source1, source_n)
                var eating = {
                    eat: function(){
                        return "I can Eat <br>";
                    }
                };
                var walking = {
                    walk: function(){
                        return "I can Walk <br>";
                    }
                };
                var talking = {
                    talk: function(){
                        return "I can Talk <br>";
                    }
                };
                
                var Rahul = Object.assign({}, eating, walking, talking);
                var RoboCop = Object.assign({}, walking, talking);
                document.write(Rahul.eat());
                document.write(Rahul.walk());
                document.write(Rahul.talk());

                document.write(RoboCop.walk());
                document.write(RoboCop.talk());	
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    I can Eat
    I can Walk
    I can Talk
    I can Walk
    I can Talk

Composition With Constructor Or Class
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Composition or Mixins
                // Object.assign(target, source1, source_n)
                
                // Eating Feature 
                var eating = {
                    eat: function(){
                        return "I can Eat <br>";
                    }
                };
                
                // Walking Feature
                var walking = {
                    walk: function(){
                        return "I can Walk <br>";
                    }
                };
                
                // Talking Feature
                var talking = {
                    talk: function(){
                        return "I can Talk <br>";
                    }
                };
                
                // Human Class
                var Human = function (){
                }
                
                // Compositing Features to Human
                Object.assign(Human.prototype, eating, walking, talking);
                
                // Robot Class
                var Robot = function () {
                }
                
                // Compositing Features to Robot
                Object.assign(Robot.prototype, walking, talking);
                
                // Creating Objects 
                var Rahul = new Human();
                var RoboCop = new Robot();
                
                // Using Features
                document.write(Rahul.eat());
                document.write(Rahul.walk());
                document.write(Rahul.talk());

                document.write(RoboCop.walk());
                document.write(RoboCop.talk());	
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    I can Eat
    I can Walk
    I can Talk
    I can Walk
    I can Talk

Mixin Function
^^^^^^^^^^^^^^

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Composition or Mixins
                // Object.assign(target, source1, source_n)
                
                // Creating Mixing Function
                function mixin (target, ...sources) {
                    Object.assign(target, ...sources);
                }
                
                // Eating Feature 
                var eating = {
                    eat: function(){
                        return "I can Eat <br>";
                    }
                };
                
                // Walking Feature
                var walking = {
                    walk: function(){
                        return "I can Walk <br>";
                    }
                };
                
                // Talking Feature
                var talking = {
                    talk: function(){
                        return "I can Talk <br>";
                    }
                };
                
                // Human Class
                var Human = function (){
                }
                
                // Compositing Features to Human
                mixin(Human.prototype, eating, walking, talking);
                
                // Robot Class
                var Robot = function () {
                }
                
                // Compositing Features to Robot
                mixin(Robot.prototype, walking, talking);
                
                // Creating Objects 
                var Rahul = new Human();
                var RoboCop = new Robot();
                
                // Using Features
                document.write(Rahul.eat());
                document.write(Rahul.walk());
                document.write(Rahul.talk());

                document.write(RoboCop.walk());
                document.write(RoboCop.talk());	
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    I can Eat
    I can Walk
    I can Talk
    I can Walk
    I can Talk

