Module 21 : JAVASCRIPT - String Methods
=======================================

1) String Length Property
-------------------------

- The length property returns the length of a string.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // length property
                var str = "Hello TechnoDexterous";
                document.write(str.length);
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    21

2) charAt() Method
------------------

- The charAt() method returns the character at a specified index (position) in a string.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // charAt(position) Method
                var str = "Hello TechnoDexterous";
                document.write(str.charAt(9));
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    h

3) charCodeAt() Method
----------------------

- The charCodeAt() method returns the unicode of the character at a specified index in a string.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // charCodeAt(position) Method
                var str = "Hello TechnoDexterous";
                document.write(str.charCodeAt(2));
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    108

4) toUpperCase() Method
-----------------------

- Convert string to upper case.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // toUpperCase( ) Method
                var str = "Hello TechnoDexterous";
                document.write(str.toUpperCase());
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    HELLO TECHNODEXTEROUS

5) toLowerCase() Method
-----------------------

- Convert string to Lower case.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // toLowerCase( ) Method
                var str = "HELLO TECHNODEXTEROUS";
                document.write(str.toLowerCase());
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    hello technodexterous

6) trim() Method
----------------

- It removes white space from both side of string.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // trim( ) Method
                var str = "         Hello TechnoDexterous";
                document.write(str.trim());
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Hello TechnoDexterous

7) replace() Method
-------------------

- The replace() method replaces a specified value with another value in a string, replace() function replaces only the first match.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // replace(old, new) Method	
                var str = "Hello TechnoDexterous";
                document.write(str.replace("TechnoDexterous", "World"));
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Hello World

8) split() Method
-----------------

- The split ( ) method breaks the string up into separate string accodring to a delimeter passed as its first argument.
- The result is returned in an array.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                //  split() Method	
                var str = "Hi guys Lets Learn JavaScript";
                var arr = str.split(" ");
                document.write(arr);
                
                document.write("<br>");
                
                var str1 = "Hi&guys&Lets&Learn&JavaScript";
                document.write(str1.split("&"));
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Hi,guys,Lets,Learn,JavaScript
    Hi,guys,Lets,Learn,JavaScript

9) indexOf() Method
-------------------

- The indexOf() method takes a string argument and returns the index of the first occurance of the argument in the string.
- If the argument is not found returns -1 .
- This method also accepts an optional second argument that specifies the index at which to start the search.
- The indexOf() method cannot take powerful search values (regular expressions).

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // indexOf() Method
                var str = "Hi guys Lets Learn JavaScript";
                document.write(str.indexOf("e"));	// 9
                document.write("<br>");
                document.write(str.indexOf("e", 10));	//14
                document.write("<br>");
                document.write(str.indexOf("Lets"));	// 8	
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    9
    14
    8

10) search() Method
-------------------

- The search() method searches a string for a specified value and returns the position of the match.
- The search() method cannot take a second start position argument.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // search() Method
                var str = "Hi guys Lets Learn JavaScript";
                document.write(str.search("e"));
                document.write("<br>");
                document.write(str.search("Lets"));
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    9
    8

11) slice() Method
------------------

- The slice() extracts a part of a string and returns the extracted part in a new string.
- The method takes 2 parameters: the starting index (position), and the ending index (position).
- The method returns a string containing the string beginning at the given index up to but not including the character at the index speficied by the second argument.
- If a parameter is negative, the position is counted from the end of the string.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // slice() Method	
                var str = "Hi guys Lets Learn JavaScript";
                document.write(str.slice(8, 14));	// 14 not included
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Lets L

12) substring() Method
----------------------

- The substring() is similar to slice().
- The first argument specifies the index at which the desired substring begins.
- The optional second argument indicates the index at which the desired substring ends.
- The method returns a string containing the substring beginning at the given index up to but not including the character at the index speficied by the second argument.
- The difference between slice and substring is that substring() cannot accept negative indexes.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // substring() Method
                var str = "Hi guys Lets Learn JavaScript";
                document.write(str.substring(3, 11));	// 11 not included
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    guys Let

13) substr() Method
-------------------

- The substr() is similar to slice().
- The substr() method returns the part of a string between the start index and a number of characters after it.
- substr() extracts length characters from a string, counting from the start index.
- If start is a positive number, the index starts counting at the start of the string.
- If start is a negative number, the index starts counting from the end of the string.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // substr() Method
                var str = "Hi guys Lets Learn JavaScript";
                document.write(str.substr(8, 8));	
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    Lets Lea

