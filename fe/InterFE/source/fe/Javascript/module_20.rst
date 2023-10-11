Module 20 : JAVASCRIPT - String
===============================

What is String?
---------------

- String is the built in object corresponding to the primitive string data type. 
- String is group of characters.

**Primitive**

1. var str = "Hello TechnoDexterous";
2. var str = 'Hello TechnoDexterous'; 
3. ``var str = `Hello TechnoDexterous`;``

**Constructor**

1. var str = new String ("Hello TechnoDexterous");
2. var str = new String ('Hello TechnoDexterous');
3. ``var str = new String (`Hello TechnoDexterous`);``

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var str1 = "Hello TechnoDexterous1";
                var str2 = 'Hello TechnoDexterous2';
                var str3 = `Hello TechnoDexterous3`;
                document.write(str1 + "<br>");
                document.write(str2 + "<br>");
                document.write(str3 + "<br>");
                document.write("I am 'Good' Boy <br>");
                document.write('I am "Good" Boy <br>');
                document.write("12345<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/string.png
   :width: 800

String Concatenation
--------------------

- String concatenation in JavaScript refers to the process of combining two or more strings to create a new string.
- You can concatenate strings using the + operator or by using template literals (introduced in ES6) with backticks (``).

Concat + Operator
^^^^^^^^^^^^^^^^^

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var firstName = "Techno";
                var lastName = "Dexterous";
                document.write(firstName + " " + lastName);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/string_1.png
   :width: 800

Concat () Method
^^^^^^^^^^^^^^^^

- The concat () method accepts any number of arguments and returns the string obtained by concatenating the arguments to the string on which it was invoked.

Syntax:

.. code-block:: javascript

    string.concat(string1, string2, string_n);

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // concat ( ) Method
                var str1 = "Hello";
                var str2 = "TechnoDexterous";
                var str3 = "Something";
                var new_str = str1.concat(str2, str3, "ANything");
                document.write(new_str);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/string_2.png
   :width: 800

Escape Notation
---------------

- \0	the NULL character
- \'	single quote
- \"	double quote
- \\	backslash
- \n	new line
- \r	carriage return
- \v	vertical tab
- \t	tab
- \b	backspace
- \f	form feed

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                console.log("Hello\nTechnoDexterous");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/string_3.png
   :width: 800

Template Literal/Template Strings
---------------------------------

- Template literals are string literals allowing embedded expressions.
- You can use multi-line strings and string interpolation features with them.
- Template literals are enclosed by the back-tick (``) character instead of double or single quotes. 

1. var str1 = "Hello TechnoDexterous";
2. var str2 = 'Hello TechnoDexterous'; 
3. ``var str3 = `Hello TechnoDexterous`;``

Multiple Line String
^^^^^^^^^^^^^^^^^^^^

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
            /* Wrong Syntax
                console.log("Hello
                TechnoDexterous");
            */
                console.log(`Hello 
    TechnoDexterous
    Something`);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/string_4.png
   :width: 800

String Interpolation
^^^^^^^^^^^^^^^^^^^^

- Template literals can contain placeholders.
- These are indicated by the dollar sign and curly braces (${expression})

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var str = "Hello TechnoDexterous";
                document.write(`${str} <br>`);
                document.write(`${str} World`);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/string_5.png
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
                var a = 5;
                var b = 4;
                document.write(`${a+b}`);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/string_6.png
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
                function myfun (say){
                    return say;
                }
                document.write(`${myfun("Hello")}`);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/string_7.png
   :width: 800

Tagged Template
---------------

- Tagged Templates are advanced form of Template literal.
- Tags allow you to parse template literals with a function.
- The first argument of a tag function contains an array of string values.
- The remaining arguments are related to the expressions.
- In the end, your function can return your manipulated string.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // There are 5 movie tickets Each Rs 200 and if you buy 5 tickets get discount Rs. 50 Each
                // There are 5 movie tickets Each Rs 200 and if you buy less than 5 tickets get discount Rs. 0 Each
                var noofticket = 5;
                var buyticket = 4;
                var eachprice = 200;
                var disprice = 50;
                // function ticket(theory, ...rest) {}
                function ticket (theory, nticket, eprice, bticket, dprice){
                        if(bticket < 5){
                            dprice = 0;
                            return `${theory[0]}${nticket}${theory[1]}${eprice}${theory[2]}${bticket}${theory[3]}${dprice}${theory[4]}`
                        } else {
                            return `${theory[0]}${nticket}${theory[1]}${eprice}${theory[2]}${bticket}${theory[3]}${dprice}${theory[4]}`
                        }
                }
                
                document.write(ticket`There are ${noofticket} movie tickets Each Rs ${eachprice} and if you buy ${buyticket} tickets get discount Rs. ${disprice} Each`);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/string_8.png
   :width: 800

