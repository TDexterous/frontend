Module 17 : JAVASCRIPT - Array 
==============================

Array
-----

- Arrays are collection of data items stored under a single name.
- Array provide a mechanism for declaring and accessing several data items with only one identifier, thereby simplifying the task of data management.
- We use array when we have to deal with multiple data items.
- Arrays are a special type of objects.
- The typeof operator in JavaScript returns "object" for arrays.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var stu = ["Rahul", "Raj"];
                document.write(stu);
                document.write(typeof(stu));
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Rahul,Rajobject

Declaration and initialization of Array
---------------------------------------

1. Using Array Literal
^^^^^^^^^^^^^^^^^^^^^^

Syntax-1:

.. code-block:: javascript

    var array_name = [ ];

Syntax-2:

.. code-block:: javascript

    var array_name = [value1, value2, value_n];

**Note** - By default, array starts with index 0.

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var techno = [];	// empty array
                techno[0] = "Rahul";
                techno[1] = "Ram";
                techno[2] = 56;
                techno[3] = "Jay";
                document.write(techno);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Rahul,Ram,56,Jay

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var techno = ["Rahul", "Ram", 56, "Jay"];
                document.write(techno);			
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Rahul,Ram,56,Jay

Ex-3:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var a = 10, b = 20, c = 30;
                var techno = [a, b, c];
                document.write(techno);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    10,20,30

2. Using Array Constructor 
^^^^^^^^^^^^^^^^^^^^^^^^^^

Syntax-1:

.. code-block:: javascript

    var array_name = new Array( );

Syntax-2:

.. code-block:: javascript

    var array_name = new Array(value1, value2, value_n);

Syntax-3:

.. code-block:: javascript

    var array_name = new Array(single_numeric_value);

- This will create an empty array with 5 length.
- So this is not good idea to use Array Constructor if you have only single numeric value.

Ex:-1

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // var techno = [];
                var techno = new Array();		// empty array
                techno[0] = "Rahul";
                techno[1] = "Ram";
                techno[2] = 56;
                techno[3] = "Jay";
                document.write(techno[2]);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    56

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // var techno = ["Rahul", "Ram", 56, "Jay"];
                var techno = new Array("Rahul", "Ram", 56, "Jay");

                document.write(techno[3]);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Jay

Ex-3:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var techno = new Array(10);

                document.write(techno);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    ,,,,,,,,,

Array Important Points
----------------------

- JavaScript arrays are zero-indexed: the first element of an array is at index 0.
- Using an invalid index number returns undefined.
- It's possible to quote the JavaScript array indexes as well (e.g., techno['2'] instead of techno[2]), although it's not necessary.
- Arrays cannot use strings as element indexes but must use integers.
- There is no associative array in JavaScript.
	techno["fees"] = 200;
- No advantage to use Array Constructor so better to use Array Literal for creating Arrays in JavaScript.

Accessing Array Elements
------------------------

- In JavaScript, you can access individual elements in an array using square brackets [] notation with the index of the element you want to retrieve.
- Array indexing in JavaScript is zero-based, which means the first element is at index 0, the second element is at index 1, and so on.

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
                    var techno = ["Rahul", "Ram", 56, "Jay"];
                    document.write (techno);
                */
                var techno = [];
                techno[0] = "Rahul";
                techno[1] = "Ram";
                techno[2] = 56;
                techno[3] = "Jay";
                techno[24] = "Extra";
                document.write(techno);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Rahul,Ram,56,Jay,,,,,,,,,,,,,,,,,,,,,Extra

Modifying Array Elements
------------------------

- In JavaScript, you can modify array elements by accessing them using their index and then assigning a new value to that index.

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var techno = ["Rahul", "Ram", 56, "Jay"];
                document.write (techno + "<br>");
                techno[0] = "Rohit";
                document.write (techno + "<br>");
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Rahul,Ram,56,Jay
    Rohit,Ram,56,Jay

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var techno = ["Rahul", "Ram", 56, "Jay"];
                var technodexterous = techno;
                document.write(technodexterous + "<br>");
                document.write(techno + "<br>");
                technodexterous[0] = "Rohit";
                document.write(techno + "<br>");
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Rahul,Ram,56,Jay
    Rahul,Ram,56,Jay
    Rohit,Ram,56,Jay

Removing Array Elements
-----------------------

- Array elements can be removed using delete operator.
- This operator sets the array element it is invoked on to undefined but does not change the array's length.

Syantx:

.. code-block:: javascript

    delete Array_name[index];

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var techno = ["Rahul", "Ram", 56, "Jay"];
                document.write(techno + "<br>");
                delete techno[0];
                document.write(techno + "<br>");
                document.write(techno[0] + "<br>");
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Rahul,Ram,56,Jay
    ,Ram,56,Jay
    undefined

Array Length Property
---------------------

- The length property retrieves the index of the next available position at the end of the array.
- The length property is automatically updated as new elements are added to the array.
- For this reason, length is commonly used to iterate through all elements of an array.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var techno = ["Rahul", "Ram", 56, "Jay"];
                document.write(techno.length);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    4

Iteration of Array using for Loop
---------------------------------

- Iterating through an array using a for loop in JavaScript is a common programming task.
- It allows you to access each element in the array one by one and perform some operation on it.
- Here's how you can iterate through an array using a for loop:

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var techno = ["Rahul", "Ram", 56, "Jay"];
            //  var techno = new Array("Rahul", "Ram", 56, "Jay");
                for(let i=0; i<=3; i++){
                    document.write(techno[i] + "<br>");
                }
                
                /* In case if you dont know array length use length property with for loop 
                for(let i=0; i<techno.length; i++){
                    document.write(techno[i] + "<br>");
                }
                */
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Rahul
    Ram
    56
    Jay

forEach Loop
------------

- The forEach calls a provided function once for each element in an array, in order.

Syntax:

.. code-block:: javascript

    array.forEach(function (value, index, arr) { 
            });

**Where,** 
       value - It is the current value of array index.

       index - Array's index number.
       
       arr - The array object the current element belongs to

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var techno = ["Rahul", "Ram", 56, "Jay"];
                techno.forEach(function (value, index) {
                    document.write(value + " " + index + "<br>");
                });
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Rahul 0
    Ram 1
    56 2
    Jay 3

for of Loop
-----------

- The for...of statement creates a loop iterating over iterable objects.

Syntax:

.. code-block:: javascript

    for (var variable_name of array) {
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
                var techno = ["Rahul", "Ram", 56, "Jay"];
                for(let value of techno){
                    document.write(value);
                }
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    RahulRam56Jay

How to get Input from User in Array
-----------------------------------

You can get input from user in an empty array :- 

- var geek= [ ];
- var geek = new Array( );
- var geek = new Array(3); // 3 is length of array

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
            // Defining Array 
                var elements = prompt("Enter number of Elements: ");
                var techno= [];
                
            // Input for Array
                for(var i = 0; i<=elements; i++){
                    techno[i] = prompt("Enter Name: ");
                }
            // Display Values
                for(var value of techno){
                    document.write(value + "<br>");
                }
            /*	
                // Defining Array
                var techno = new Array(3);		// length of array 3
                
                // Array Length
                var ln = techno.length;
                
                // Input 
                for(let i =0; i<= ln; i++){
                    techno[i] = prompt("Enter Name: ");
                }
                
                // Display Values
                for(var value of techno){
                    document.write(value + "<br>");
                }	
            */
            </script>
        </body>
    </html>

Output:

- After running above code we will get below output screen. we have to Enter number of Elements. for e.g. i will give 2 as input.

.. image:: D:/Courses/Javascript_images/array.png
   :width: 800

After that we have to Enter Name.

- First iteration (i = 0): It prompts for a name and stores "Rahul" in techno[0].

.. image:: D:/Courses/Javascript_images/array_1.png
   :width: 800

- Second iteration (i = 1): It prompts for another name and stores "Sonam" in techno[1].

.. image:: D:/Courses/Javascript_images/array_2.png
   :width: 800

- Third iteration (i = 2): It prompts for another name and stores "Ajit" in techno[2].

.. image:: D:/Courses/Javascript_images/array_3.png
   :width: 800

- However, our loop runs three times due to the condition i <= elements. Then we will get expected output as below:

.. image:: D:/Courses/Javascript_images/array_4.png
   :width: 800

Multidimensional Array
----------------------

- Multidimensional array is Arrays of Arrays.
- Multidimensional array can be 2D, 3D, 4D etc.

Ex:

	2D - var name **[** [ ], [ ], [ ] **]**

2D Array
^^^^^^^^

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
                var techno = [[], [], []];
                techno[0][0] = "Rahul";
                techno[0][1] = "Dell";
                techno[0][2] = 10;
                techno[1][0] = "Sonam";
                techno[1][1] = "HP";
                techno[1][2] = 20;
                techno[2][0] = "Sumit";
                techno[2][1] = "Zed";
                techno[2][2] = 30;
            */
            // Using Array Literal
                var techno = [
                                ["Rahul", "Dell", 10], 
                                ["Sonam", "HP", 20], 
                                ["Sumit", "Zed", 30]
                            ];
                
                // using Array Constructor
                // var techno = new Array(["Rahul", "Dell", 10], ["Sonam", "HP", 20], ["Sumit", "Zed", 30]);
                            
                for(let i =0; i<3; i++){
                    for(let j =0; j<3; j++){
                        // document.write(techno[i][j] + " ");
                        document.write( i + " " + j + " " + techno[i][j] + " ");
                    }
                    document.write("<br>")
                }
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_5.png
   :width: 800

How to Create Empty 2D Array
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // Undefined 2D array
                
                // using array literal
                    var techno = [[], []];
                
                // using array constructor
                // var techno = new Array([], []);
                
                for(let i =0; i<2; i++){
                    for(let j =0; j<3; j++){
                        document.write(i + " " + j + "|");
                    }
                    document.write("<br>")
                }	
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_6.png
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
                var techno = [];
                var rows = 2;
                var cols = 3;
                for(var i = 0; i < rows; i++){ 
                    techno[i] = []; 
                }		
                for(var i =0; i< rows; i++){
                    for(var j = 0; j< cols; j++){
                        document.write(techno[i][j] + "  ");
                        // document.write(i + " "+ j + "|");
                    }
                    document.write("<br>");
                }
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_7.png
   :width: 800

Ex-3:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var rows = 3;
                var cols = 2;
                var techno = new Array(rows);
                for (var i = 0; i < rows; i++) {
                techno[i] = new Array(cols);
                }
            
                for(var i =0; i<rows; i++){
                    for(var j=0; j<cols; j++){
                        document.write(techno[i][j] + "  ");
                        // document.write(i + " "+ j + "|");
                    }
                    document.write("<br>");
                }
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_8.png
   :width: 800

How to get Input from user in 2D Array
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
                // Defining 2D Array
                var rows = 3;
                var cols = 2;
                var techno = new Array(rows);
                for (var i = 0; i < rows; i++) {
                techno[i] = new Array(cols);
                }

                // Input for Array
                for(var i =0; i<rows; i++){
                    for(var j=0; j<cols; j++){
                        techno[i][j] = prompt("Enter Name: ");
                    }
                }
                
                // Displaying value
                for(var i =0; i<rows; i++){
                    for(var j = 0; j<cols; j++){
                        document.write(i + " " + j + techno[i][j] + " | ");
                    }
                    document.write("<br>");
                }	
            </script>
        </body>
    </html>

Output:

- When you run this code in a web browser, you will see three prompts for each row and two prompts for each column, asking for input. given below:

.. image:: D:/Courses/Javascript_images/array_9.png
   :width: 800

.. image:: D:/Courses/Javascript_images/array_10.png
   :width: 800

.. image:: D:/Courses/Javascript_images/array_11.png
   :width: 800

.. image:: D:/Courses/Javascript_images/array_12.png
   :width: 800

.. image:: D:/Courses/Javascript_images/array_13.png
   :width: 800

.. image:: D:/Courses/Javascript_images/array_14.png
   :width: 800

- After prompting the inputs i.e. Names we will get expected output as below:

.. image:: D:/Courses/Javascript_images/array_15.png
   :width: 800

