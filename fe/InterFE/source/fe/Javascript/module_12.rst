Module 12 : JAVASCRIPT - Functions
==================================

1) Function Definition
----------------------

- Function are subprograms which are used to compute a value or perform a task.

Type of Function
^^^^^^^^^^^^^^^^

1. Library or Built-in functions.

Ex: - valueOf( ) , write( ), alert( ) etc

2. User-defined functions.

2) Creating and Calling a Function
----------------------------------

Creating a Function
^^^^^^^^^^^^^^^^^^^

Syntax:

.. code-block:: javascript

    function function_name( )
    {
        Block of statement;
    }

Ex:

.. code-block:: javascript
   :linenos:

    function display( )
    {
        document.write("Techno-Dexterous");
    }

Calling a Function
^^^^^^^^^^^^^^^^^^

Syntax:

.. code-block:: javascript
    
    function_name( );

Ex:

.. code-block:: javascript
   :linenos:
   
   display( );

- Now we will see a practical example with output.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Defining Function
                function display(){
                    document.write("Techno Dexterous");
                }
                display();	// Calling Function 
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Techno Dexterous

**Rules**

- Function name only starts with a letter, an underscore ( _ ).
- Function name cannot start with a number. 
- Do not use reserved keywords. e.g. else, if etc.
- Function names are case-sensitive in JavaScript.

How Function Call Works
^^^^^^^^^^^^^^^^^^^^^^^

- The code inside a function isn't executed until that function is called.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // How function call works
                document.write("First Line <br>");
                display();
                document.write("Techno Dexterous <br>");
                function display(){
                    document.write("Inside Function <br>");
                }
                document.write("Last Line <br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/function_call_works.png
   :width: 300

3) Function with Parameters
---------------------------

- JavaScript function definitions do not specify data types for parameters.
- JavaScript functions do not perform type checking on the passed arguments.
- JavaScript functions do not check the number of arguments received.

Syntax:

.. code-block:: javascript

    function function_name (parameter1, parameter2, ....)
    {
        Block of statement;   
    }

Ex:

.. code-block:: HTML
   :linenos:

    function display(name)
    {
        document.write(name);
    }

Call Function with Parameter
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Syntax:

.. code-block:: javascript
    
    function_name(argument1, argument2);

Ex:

.. code-block:: HTML
   :linenos:

   display("Techno-Dexterous");

- Now we will see a practical example with output.

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Function with Parameters
                function display(name){
                    document.write(name);
                }
                display("Techno-Dexterous");
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Techno-Dexterous

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Function with Parameters
                function display(name1, name2){
                    document.write(name1 + " to " + name2 + "<br>");
                }
                display("Welcome", "Techno-Dexterous");
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML
    
    Welcome to Techno-Dexterous

Function Argument Missing
^^^^^^^^^^^^^^^^^^^^^^^^^

- If a function is called with missing arguments, the missing values are set to undefined.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Function Argument Missing
                function add(a, b, c){
                    document.write("A: " + a + " B: " + b + " C: " + c);
                }
                add(10, 20);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    A: 10 B: 20 C: undefined

4) Arguments Object
-------------------

- The arguments object contains an array of the arguments used when the function was called.
- This object contains an entry for each argument passed to the function, the first entry's index starting at 0.
- The arguments object is not an Array.
- It is similar to an Array, but does not have any Array properties except length.

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function display(name)
                {
                    //document.write(name);
                    document.write(arguments[0]);
                }
                display("Techno-Dexterous");
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Techno-Dexterous

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function display(name1, name2)
                {
                    //document.write(name1, name2);
                    document.write(arguments[0] + " " + arguments[1]);
                }
                display("Techno-Dexterous", "World");
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Techno-Dexterous World

Ex-3:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function display(name1, name2)
                {
                    arguments[0] = "Hello";
                    document.write(arguments[0] + " " + arguments[1]);
                }
                display("Techno-Dexterous", "World");
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Hello World

Ex-4:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function display(name1 , name2)
                {
                    document.write(arguments.length);
                }
                display("Techno-Dexterous", "Hello", "World");
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    3

Ex-5:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function display()
                {
                    document.write(arguments.length);
                }
                display("Techno-Dexterous", "Hello", "World");
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    3

Ex-6:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function display(name1, name2)
                {
                    for(var i = 0; i<arguments.length; i++)
                    {
                        document.write(arguments[i] + " ");
                    }
                }
                display("Techno-Dexterous", "World");
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Techno-Dexterous World

Ex-7:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function display()
                {
                    for(var i = 0; i<arguments.length; i++)
                    {
                        document.write(arguments[i] + " ");
                    }
                }
                display("Techno-Dexterous", "Hello", "World");
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Techno-Dexterous Hello World

Ex-8:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function display()
                {
                    arguments[0] = "Hello";
                    for(var i = 0; i<arguments.length; i++)
                    {
                        document.write(arguments[i] + " ");
                    }
                }
                display("Techno-Dexterous", "World");
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Hello World

Many Function Arguments
^^^^^^^^^^^^^^^^^^^^^^^

- If a function is called with too many arguments, these arguments can be reached using the arguments object which is a built-in.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Too Many Function Argument
                // Extra argument can be accessed using arguments object
                function add(a, b){
                    document.write("A: " + a + " B: " + b + " C: " + arguments[2]);
                }
                add(10, 20, 30);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    A: 10 B: 20 C: 30

5) Default Parameter
--------------------

Syntax-1:

.. code-block:: javascript

    function function_name (para1, para2, para3="value")
    {
        Block of statement;   
    }

Syntax-2:

.. code-block:: javascript

    function function_name (para1, para2="value", para3) 	// problem undefined
    {
        Block of statement;   
    }

Syntax-3:

.. code-block:: javascript

    function function_name (para1, para2="value1", para3="value2")
    {
        Block of statement;   
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
                // Default Parameters
                function add(a, b, c = 70){
                    document.write("A= " + a + "<br>");
                    document.write("B= " + b + "<br>");
                    document.write("C= " + c + "<br>");
                }
                add(10, 20);		// 10 20 70
                add(10, 20, 30);	// 10 20 30
                add(10);		// 10 undefined 70
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/default_parameter.png
   :width: 300

- JavaScript also allows the use of arrays and null as default values.

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Default Parameters
                // null assigned to c
                function add(a, b, c = null){
                    document.write("A= " + a + "<br>");
                    document.write("B= " + b + "<br>");
                    document.write("C= " + c + "<br>");
                }
                add(10, 20);		// 10 20 null
                add(10, 20, 30);	// 10 20 30
                add(10);		// 10 undefined null
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/default_parameter_null.png
   :width: 300

Ex-3:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Default Parameter
                // Array
                function add(num, a=["Techno", "Dexterous"]){
                    document.write("Num= " + num + "<br>");
                    document.write("A= " + a[0] + "<br>");
                    document.write("A= " + a[1] + "<br>");
                }
                add(20, [10, 40]);
                add(20);
                add();
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/default_parameter_array.png
   :width: 300

6) Rest Parameters
------------------

- The rest parameter allows to represent an indefinite number of arguments as an array.

Syntax-1:

.. code-block:: javascript

    function function_name (...args)
    {
        Block of statement;   
    }

Syntax-2:

.. code-block:: javascript

    function function_name (a, ...args)
    {
        Block of statement;   
    }

- The rest operator must be the last parameter to a function.

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Rest Parameters
                function show(...args){
                    document.write(args);
                }
                show(10,20,30,40,50);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    10,20,30,40,50

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Rest Parameters
                function show(a, ...args){
                    document.write(a + "<br>");
                    document.write(args);
                }
                show(10,20,30,40,50);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    10
    20,30,40,50

Ex-3:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Rest Parameters
                function show(a, ...args){
                    document.write(a + "<br>");
                    document.write(args[0] + " " + args[1] + " " + args[2]);
                }
                show(10,20,30,40,50);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    10
    20 30 40

7) Rest Vs Arguments
--------------------

There are three main differences between rest parameters and the arguments object:-

- Rest parameters are only the ones that haven't been given a separate name, while the arguments object contains all arguments passed to the function.
- The arguments object is not a real array, while Rest Parameters are Array instances, meaning methods like sort, map, forEach or pop can be applied on it directly.
- The arguments object has additional functionality specific to itself (like the callee property).

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Rest Parameters
                function restShow(...args){
                    console.log(args);
                }
                restShow(10,20,30,40,50);
                
                // Arguments Object
                function show(){
                    console.log(arguments);
                }
                show(10,20,30,40,50);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/rest_vs_argument.png
   :width: 800

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Rest Parameters
                function restShow(a, ...args){
                    console.log("a: " + a);
                    console.log(args);
                }
                restShow(10,20,30,40,50);
                
                // Arguments Object
                function show(a){
                    console.log("a: " + a);
                    console.log(arguments);
                }
                show(10,20,30,40,50);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/rest_vs_argument_2.png
   :width: 800

8) Return Statement
-------------------

- A return statement may be return Any type data, including arrays and objects.

Syntax-1: 

.. code-block:: javascript
    
    return (variable or expression);

Syntax-2:

.. code-block:: javascript

    function function_name(para1, para2, ....)
    {
        Block of statement;
        return (expression);
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
                function add(a, b){
                    return (a+b);
                }
                document.write(add(10, 20));
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    30

9) Variable Scope
-----------------

JavaScript has two scopes: -

- Global.
- Local.

Global Scope
^^^^^^^^^^^^

- A variable that is declared outside a function definition is a global variable, and its value is accessible and modifiable throughout your program.
- In a web browser, global variables are deleted when you close the browser window (or tab), but remain available to new pages loaded into the same window.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // accessible from anywhere 
                var i = "I am global Variable";	// Global Variable
                
                function show(){
                    document.write(i + "<br>");	// accessible in function
                }
                show();
                
                document.write(i + "<br>");	// accessible outside
                
                function disp(){
                    document.write(i + "<br>");	// accessible in function
                }
                disp();
                
                if(true){
                    document.write(i + "<br>");	// accessible in block
                }
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    I am global Variable
    I am global Variable
    I am global Variable
    I am global Variable

Local Scope
^^^^^^^^^^^

- A variable that is declared inside a function definition is local.
- It is created and destroyed every time the function is executed, and it cannot be accessed by any code outside the function.
- Inside a function, if a variable has not been declared with var it is created as a global variable.

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // accessible from anywhere 
                var i = "I am global Variable";	// Global Variable
                
                function show(){
                    var j = "I am Local Variable";	// Local Variable
                    document.write(i + "<br>");	// i accessible in function
                    document.write(j + "<br>");	// j accessible in function	
                }
                show();
                
                document.write(i + "<br>");	// i accessible outside
                document.write(j + "<br>");	// j not accessible outside
                
                function disp(){
                    document.write(i + "<br>");	// i accessible in function
                    document.write(j + "<br>");	// j not accessible in other function
                }
                disp();
                
                if(true){
                    document.write(i + "<br>");	// accessible in block
                    document.write(j + "<br>");	// j not accessible in block
                }	
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    I am global Variable
    I am Local Variable
    I am global Variable

- If there is function inside a function the inner function can access outer function's variables but outer function can not access inner function's variables.
- Function arguments (parameters) work as local variables inside functions.

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function show(){
                    var j = "J a Local Vari of Outer Function"; // Local Variable
                    document.write(j + "<br>");	// j accessible in function
                    function innerFun(){
                        var k = "K a Local Vari of inner fun";	// Local variable
                        document.write(k + "<br>");	// k accessible in function
                        document.write(j + "<br>");	// j accessible in function
                    }
                    innerFun();
                    document.write(j + "<br>");	// j accessible in function
                    document.write(k + "<br>");	// k not accessible for outer fun
                }
                show();
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    J a Local Vari of Outer Function
    K a Local Vari of inner fun
    J a Local Vari of Outer Function
    J a Local Vari of Outer Function

- Below is the example of Local Variable Becomes Global.

Ex-3:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // accessible from anywhere 
                var i = "I am global Variable";	// Global Variable
                
                function show(){
                // Remove var from j, it become global variable
                    j = "I am Local Variable";	// Global Variable
                    document.write(i + "<br>");	// i accessible in function
                    document.write(j + "<br>");	// j accessible in function	
                }
                show();
                
                document.write(i + "<br>");	// i accessible outside
                document.write(j + "<br>");	// j accessible outside
                
                function disp(){
                    document.write(i + "<br>");	// i accessible in function
                    document.write(j + "<br>");	// j accessible in other function
                }
                disp();
                
                if(true){
                    document.write(i + "<br>");	// i accessible in block
                    document.write(j + "<br>");	// j accessible in block
                }
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    I am global Variable
    I am Local Variable
    I am global Variable
    I am Local Variable
    I am global Variable
    I am Local Variable
    I am global Variable
    I am Local Variable

Block Scope
^^^^^^^^^^^

- Variables declared with var do not have block scope.
- Identifiers declared with let and const do have block scope.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                if(true){
                    var i = 10;	// accesssible from anywhere
                    document.write(i + "<br>");
                }
                // in other programming i is not accessible outside block
                // but in javascript it is accessible
                document.write(i + "<br>");	// i accessible outside block
                
                if(true){
                    let j = 10;	// only accessible within block
                    document.write(j + "<br>");
                }
                // when we declare variable with let
                // it is only accessible within block
                document.write(j + "<br>");	// j not accessible 
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    10
    10
    10

10) Variable Hoisting
---------------------

- Hoisting is JavaScript's default behavior of moving declaration to the top of the function, if defined in a function, or the top of the global context, if outside a function.
- A variable can be used before it has been declared. 
- Only variable declarations are hoisted to the top, not variable initialization.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
            // Variable Hoisting
                var i = "Hello";
                document.write(i + "<br>");
                function show(){
                    document.write(i + "<br>");
                    var i = "Techno-Dexterous";
                    document.write(i + "<br>");
                }
                show();
                
                /*
                    var i; 
                    i = "Hello";
                    document.write(i + "<br>");
                    function show(){
                        var i;
                        document.write(i + "<br>");
                        i = "Techno Dexterous";
                        document.write(i + "<br>");
                    }
                    show();
                */
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Hello
    undefined
    Techno-Dexterous

11) Closure
-----------

- A closure is a function having access to the parent scope. It preserve the data from outside. 
- A closure is an inner function that has access to the outer (enclosing) function's variables.

For every closure we have three scopes:-

1. Local Scope ( Own scope)
2. Outer Functions Scope
3. Global Scope

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var i = 10;
                function show(){
                    var j = 20;
                    document.write(j +"<br>");
                    document.write(i +"<br>");
                }
                show();
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    20
    10

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                function show(){
                    var j = "J a Local Vari of Outer Function"; // Local Variable
                    document.write(j + "<br>");	// j accessible in function
                    function innerFun(){
                        var k = "K a Local Vari of inner fun";	// Local variable
                        document.write(k + "<br>");	// k accessible in function
                        document.write(j + "<br>");	// j accessible in function
                    }
                    innerFun();
                    document.write(j + "<br>");	// j accessible in function
                    document.write(k + "<br>");	// k not accessible for outer fun
                }
                show();
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    J a Local Vari of Outer Function
    K a Local Vari of inner fun
    J a Local Vari of Outer Function
    J a Local Vari of Outer Function

12) Function Expression
-----------------------

- When we create a function and assign it to a variable, known as function expression.

**Note:**

- You can't call function expression before function definition. 
- Function expressions in JavaScript are not hoisted, unlike function declarations.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
            // Function Expression
            // You can't use function expressions before you define them:
                var disp = function show(){
                    document.write("Hello Techno-Dexterous");
                };
                disp();
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Hello Techno-Dexterous

13) Anonymous Functions
-----------------------

- Anonymous functions allow the creation of functions which have no specified name.

1. Can be stored in a Variable 
2. Can be Returned in a Function
3. Can be pass in a Function 

Syntax:

.. code-block:: javascript

	function ( ) {
	   body of function;	
	};

Store Anonymous Function in Variable
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
            // Storing Anonymous Function in variable
                var disp = function(){
                    document.write("Hello Techno-Dexterous");
                };
                disp();
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Hello Techno-Dexterous

Passing Anonymous Function as Argument
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Passing Anonymous Function
                function disp(myfun){
                    return myfun();
                }
                
                document.write(disp(function(){
                    return "Techno-Dexterous";
                }));
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Techno-Dexterous

Returning Anonymous Function
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Returning Anonymous Function
                function disp(a){
                    return function(b){
                        return a+b;
                    };
                }
                var af = (disp(10));
                document.write(af(20));
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    30

14) Arrow Function
------------------

- An arrow function expression (previously, and now incorrectly known as fat arrow function) has a shorter syntax compared to function expressions.
- Arrow functions are always anonymous. 

Syntax:

.. code-block:: javascript

	( ) => {statements};

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Function Expression
                var myfun1 = function show(){
                        document.write("Techno-Dexterous");
                    };
                
                // Anonymous Function 
                var myfun2 = function(){
                        document.write("Techno-Dexterous");
                    };
                
                // Arrow Function 
                var myfun = () => {
                        document.write("Techno-Dexterous");
                    };
                myfun();
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Techno-Dexterous

- Do not call before definition.

Ex:

.. code-block:: HTML
   :linenos:

    myfun();
    var myfun = () => { document.write("Techno-Dexterous");};


- An arrow function cannot contain a line break between its parameters and its arrow.

Ex:

.. code-block:: HTML
   :linenos:

    var myfun = () 
    => { document.write("Techno-Dexterous");};
    myfun();

Arrow Function With Parameters
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**1. With one Parameter**

Syntax-1:

.. code-block:: javascript

    (para) => {statement};

Syntax-2:

.. code-block:: javascript
    
    para => {statement};

**2. More than one Parameter**

Syntax:

.. code-block:: javascript

    (para1, para2, paraN) => {statement};

**3. No Parameter**

Syntax:

.. code-block:: javascript

    ( ) => {statement};

- Below is the example of above three Parameters.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Arrow Function with parameter 
                // One Parameter () optional  
                var myfun1 = a => {			// var myfun = (a) => {
                        document.write(a + "<br>");
                    };	
                myfun1(10);
                    
                // More than One Parameter () required  
                var myfun2 = (a, b) => {
                        document.write(a + b + "<br>");
                    };	
                myfun2(10, 20);

                // No Parameter () required  
                var myfun0 = () => {
                        document.write("Techno-Dexterous");
                    };
                myfun0();
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    10
    30
    Techno-Dexterous

**4. Default Parameter**

Syntax:

.. code-block:: javascript

    (para1, para2 = value) => {statement};

**5. Rest Parameter**

Syntax:

.. code-block:: javascript

    (para1, ...args) => {statement};

- Below is the example of above two Parameters.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Arrow Function with default para
                var myfunD = (a, b=20) => {
                        document.write(a + " " + b);
                    };
                //myfunD(10, 50);
                
                // Arrow Function with Rest para
                var myfunR = (a, ...args) => {
                        document.write(a + " " + args);
                    };
                myfunR(10, 50, 60, 70);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    10 50,60,70

Arrow Function With More Statements
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Below is the example of arrow function with more than one statements.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Arrow Function 
                var myfun1 = a => {
                        document.write(a + "<br>");
                    };
                    
                // Arrow Function 
                // use curly brackets when more than one statement			
                var myfun = a => {
                document.write(a + "<br>");
                document.write("Hello"); };
                myfun(10);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    10
    Hello

More Shorter Arrow Function
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Syntax:

.. code-block:: javascript

    (para1, para2) => expression;

Ex:

.. code-block:: HTML
   :linenos:
   
   (a, b) => a+b;

- Above code is equivalent to:

Ex:

.. code-block:: HTML
   :linenos:
   
    function add(a, b) {
        return a + b; 
    }

Syntax:

.. code-block:: javascript

    (para1, para2) => {expression};	// it won't work

Ex:

.. code-block:: HTML
   :linenos:
   
    (a, b) => {a+b};

Syntax:

.. code-block:: javascript

    (para1, para2) => {return expression};

Ex:

.. code-block:: HTML
   :linenos:

    (a, b) => {return a+b};

- Below is the practical example with output.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Function Expression
                var myfun1 = function show(a){
                        return a;
                    };
                
                // Anonymous Function 
                var myfun2 = function(b){
                        return b;
                    };
                
                // Arrow Function 
                var myfun = (c) => {
                        return c;
                    };
                
                // a bit more shorter Arrow Function 
                var myfunN = (c) => c;	
            
                document.write(myfun1(10));
                document.write(myfun2(20));
                document.write(myfun(30));
                document.write(myfunN(40));
    /*
        var myfunN = (c) => { c };
        if you put curly bracket it wont work 
        if you want to put curly bracket then
        you have to write return c 
        More Example
            var myfunN=(c)=>c;		// Work, It automatically returns c
            var myfunN=(c)=>{c};	// Won't Work
            var myfunN=(c)=>{return c};	// Work
            
            var myfunN=(a,b)=> a+b;		// Work, It automatically returns a+b
            var myfunN=(a,b)=>{a+b};	        // Won't Work
            var myfunN=(a,b)=>{return a+b};	// Work
    */			
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    10203040

15) Immediately Invoked Function Expression (IIFE)
--------------------------------------------------

- IIFE (Immediately Invoked Function Expression) is a JavaScript function that runs as soon as it is defined.
- It is a design pattern which is also known as Self-Executing Anonymous Function and contains two major parts.
- The first is the anonymous function with lexical scope enclosed within the Grouping Operator ().
- This prevents accessing variables within the IIFE idiom as well as polluting the global scope.
- The second part is creating the immediately executing function expression (), through which the JavaScript engine will directly interpret the function.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                (function(){
                    var a = 10;
                    document.write(a);
                })();
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    10

- Avoid Creating Global variable and Functions.
- As it doesn't define variable and function globally so there will be no name conflicts.
- Scope is limited to that particular function.

Pass by Value
^^^^^^^^^^^^^

- JavaScript arguments are passed by value: The function only gets to know the values, not the argument's locations.
- If a function changes an argument's value, it does not change the parameter's original value.
- Changes to arguments are not visible (reflected) outside the function.

Pass by reference
^^^^^^^^^^^^^^^^^

- In JavaScript, object references are values.
- Because of this, objects will behave like they are passed by reference:
- If a function changes an object property, it changes the original value.
- Changes to object properties are visible (reflected) outside the function.

