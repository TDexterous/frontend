Module 22 : JAVASCRIPT - Numbers
================================

Numbers
-------

- Number type in JavaScript includes both integer and floating point values.
- JavaScript numbers are always stored as double precision floating point numbers, following the international IEEE 754 standard.
- JavaScript also provide an object representation of numbers.

**Ex-**
	- 12
	- 23.45
	- 5e3

**Primitive**

1. var a = 10;	// Whole Number
2. var a = 10.45;	// Decimal Number
3. var a = 5e3;	// 5000 // 5 x 10^3	exponent 
4. var a = 34e-5;	// 0.00034  exponent 

**Constructor**

1. var a = new Number(10);
2. var a = new Number(10.45);
3. var a = new Number(5e3);

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var a = 10;
                var b = 10.45;
                var c = 5e3;
                var d = 34e-5;
                var x = new Number(100);
                document.write(typeof(a) + " :");
                document.write(a + "<br>");
                document.write(typeof(b) + " :");
                document.write(b + "<br>");
                document.write(typeof(c) + " :");
                document.write(c + "<br>");
                document.write(typeof(d) + " :");
                document.write(d + "<br>");
                document.write(typeof(x) + " :");
                document.write(x + "<br>");
                
                var e = "100";
                document.write(typeof(e) + " :");
                document.write(e + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/numbers.png
   :width: 800

Number with String
------------------

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // Number with String
                var a = "50";
                var b = 10;
                var c = 20;
                var d = "Hello";
                
                // + works as concat with string
                document.write(b + c + "<br>"); // Number + Number = Number
                document.write(a + b + "<br>");	// String + Number = String
                document.write(b + a + "<br>");	// Number + String = String
                document.write(b + d + "<br>");	// Number + String = String
                document.write(d + b + "<br>");	// String + Number = String
                document.write("<br>");	
                
                // other than + 
                document.write(c - b + "<br>");	// Number - Number = Number
                document.write(a - b + "<br>");	// String - Number = Number
                document.write(b - a + "<br>");	// Number - String = Number
                document.write(b - d + "<br>");	// Number - String = NaN (Number)
                document.write(d - b + "<br>");	// String - Number = NaN (Number)
                document.write("<br>");
                
                // Type of 
                document.write(typeof(b + c) + "<br>"); // Number + Number = Number
                document.write(typeof(a + b) + "<br>");	// String + Number = String
                document.write(typeof(b + a) + "<br>");	// Number + String = String
                document.write(typeof(b + d) + "<br>");	// Number + String = String
                document.write(typeof(d + b) + "<br>");	// String + Number = String
                document.write("<br>");	
                
                // other than + 
                document.write(typeof(c - b) + "<br>");	// Number - Number = Number
                document.write(typeof(a - b) + "<br>");	// String - Number = Number
                document.write(typeof(b - a) + "<br>");	// Number - String = Number
                document.write(typeof(b - d) + "<br>");	// Number - String = NaN
                document.write(typeof(d - b) + "<br>");	// String - Number = NaN
                document.write("<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/numbers_1.png
   :width: 800

NaN
---

- The NaN property represents "Not-a-Number" value.
- This property indicates that a value is not a legal number.
- NaN never compare equal to anything, even itself. 
- The NaN property is the same as the Number.Nan property.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // NaN (Not a Number)
                var a = "50";
                var b = 10;
                var c = 20;
                var d = "Hello";
                document.write(a/b + "<br>");
                document.write(c/d);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/numbers_2.png
   :width: 800

NaN is not equal to Anything
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
                if(NaN == NaN){
                    document.write("Equal");
                } else {
                    document.write("Not Equal");
                }
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/numbers_3.png
   :width: 800

Global isNaN () Method
----------------------

- The isNaN() function is used to determines whether a value is an illegal number (Not-a-Number).
- This function returns true if the value equates to NaN. Otherwise it returns false.
- This function is different from the Number specific Number.isNaN() method.
- The global isNaN() function, converts the tested value to a Number, then tests it.

Syntax:

.. code-block:: javascript

    isNaN(value)

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                // isNaN( ) 
                var a = "50";
                var b = 10;
                var c = 20;
                var d = "Hello";
                if(isNaN(a)){
                    document.write(`not number`);
                } else {
                    document.write(`number`);
                }
                document.write("<br>" + typeof(a));
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/numbers_4.png
   :width: 800

Infinity and -Infinity
----------------------

- Infinity or -Infinity is the value JavaScript will return if a number is too large or too small.
- All Infinity values compare equal to each other. 

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // Infinity and - Infinity
                document.write(5 / 0);
                document.write("<br>");
                document.write(-5 / 0);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/numbers_5.png
   :width: 800

Number Methods
--------------

- There are too many number methods we can see all of them one by one:

1. toString()
^^^^^^^^^^^^^

- toString () Method returns a number as a string in other words it converts number into string.
- We can use this method to output numbers as hexadecimal (16), octal(8), binary(2).

Syntax:

.. code-block:: javascript

    Variable_name.toString();

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var a = 10;
                document.write(typeof(a) + "<br>");
                document.write(a.toString() + "<br>");
                document.write(typeof(a.toString()) + "<br>");
                document.write(a.toString(2));
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/numbers_6.png
   :width: 800

2. toExponential()
^^^^^^^^^^^^^^^^^^

- The toExponential() method converts a number into an exponential notation.

Syntax:

.. code-block:: javascript

    Variable_name.toExponential(y)

- Where y is an integer between 0 and 20 representing the number of digits in the notation after the decimal point.
- If omitted, it is set to as many digits as necessary to represent the value.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var a = 58975.98745;
                document.write(a.toExponential() + "<br>");
                document.write(a.toExponential(2) + "<br>");
                document.write(a.toExponential(4) + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/numbers_7.png
   :width: 800

3. toFixed()
^^^^^^^^^^^^

- The toFixed() method converts a number into a string, keeping a specified number of decimals also it rounds the decimal.
- If the desired number of decimals are higher than the actual number, nulls are added to create the desired decimal length.

Syntax:

.. code-block:: javascript

    a.toFixed(y)

- Where y is the number of digits after the decimal point.
- Default is 0 (no digits after the decimal point)

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var a = 19.65823;
                document.write(a.toFixed() + "<br>");
                document.write(a.toFixed(2) + "<br>");
                document.write(a.toFixed(4) + "<br>");
                document.write(a.toFixed(8) + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/numbers_8.png
   :width: 800

4. toPrecision()
^^^^^^^^^^^^^^^^

- The toPrecision() method formats a number to a specified length.
- A decimal point and nulls are added (if needed), to create the specified length.

Syntax:

.. code-block:: javascript

    Variable_name.toPrecision(y) 

- Where y is the number of digits.
- If omitted, it returns the entire number (without any formatting)

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var a = 19.65823;
                document.write(a.toPrecision() + "<br>");
                document.write(a.toPrecision(2) + "<br>");
                document.write(a.toPrecision(4) + "<br>");
                document.write(a.toPrecision(9) + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/numbers_9.png
   :width: 800

5. Number.isInteger()
^^^^^^^^^^^^^^^^^^^^^

- The Number.isInteger() method determines whether a value an integer.
- This method returns true if the value is of the type Number, and an integer, Otherwise it returns false.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
            document.write("No Parameter: " + Number.isInteger() + "<br>");
            document.write("100: " + Number.isInteger(100) + "<br>");
            document.write("-100: " + Number.isInteger(-100) + "<br>");
            document.write("100.45: " + Number.isInteger(100.45) + "<br>");
            document.write("200-100: " + Number.isInteger(200-100) + "<br>");
            document.write("0.1: " + Number.isInteger(0.1) + "<br>");
            document.write('"100" ' + Number.isInteger("100") + "<br>");
            document.write('"Hello" ' + Number.isInteger("Hello") + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/numbers_10.png
   :width: 800

6. Number.isSafeInteger()
^^^^^^^^^^^^^^^^^^^^^^^^^

- The Number.isSafeInteger() method determines whether a value is a safe integer.
- A safe integer is an integer that can be exactly all integers from (2^53 - 1) to -(2^53 - 1)
- This method returns true if the value is of the type Number, and a safe integer. Otherwise it returns false.

Ex:

.. code-block:: HTML
   :linenos:

   <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
    document.write("No Parameter: " + Number.isSafeInteger() + "<br>");
    document.write("100: " + Number.isSafeInteger(100) + "<br>");
    document.write("-100: " + Number.isSafeInteger(-100) + "<br>");
    document.write("100.45: " + Number.isSafeInteger(100.45) + "<br>");
    document.write("200-100: " + Number.isSafeInteger(200-100) + "<br>");
    document.write("0.1: " + Number.isSafeInteger(0.1) + "<br>");
    document.write('"100" ' + Number.isSafeInteger("100") + "<br>");
    document.write('"Hello" ' + Number.isSafeInteger("Hello") + "<br>");
    document.write("564547567544563643543655665567756756756756: " + Number.isSafeInteger(564547567544563643543655665567756756756756) + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/numbers_11.png
   :width: 800

Global JS Methods
-----------------

JavaScript global methods can be used on all JavaScript data types.

- Number ()
- parseInt ()
- parseFloat ()

1. Number ()
^^^^^^^^^^^^

- The Number() function converts the object argument to a number that represents the object's value.
- If the value cannot be converted to a legal number, NaN is returned.
- If the parameter is a Date object, the Number() function returns the number of milliseconds since midnight January 1, 1970 UTC.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
            var a = true;
            var b = false;
            var c = 100;
            var d = "100";
            var e = "Hello";
            var f = new Date();
            document.write("True: " + Number(a) + "<br>");
            document.write("False: " + Number(b) + "<br>");
            document.write("100 " + Number(c) + "<br>");
            document.write('"100" ' + Number(d) + "<br>");
            document.write('"Hello" ' + Number(e) + "<br>");
            document.write("Date " + Number(f) + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/numbers_12.png
   :width: 800

2. parseInt ()
^^^^^^^^^^^^^^

- The parseInt() function parses a string and returns an integer.

Syntax:

.. code-block:: javascript

    parseInt(string, radix)

- The radix parameter is used to specify which numeral system to be used, for example, a radix of 16 (hexadecimal) indicates that the number in the string should be parsed from a hexadecimal number to a decimal number.

If the radix parameter is omitted, JavaScript assumes the following:

1) If the string begins with "0x", the radix is 16 (hexadecimal)
2) If the string begins with any other value, the radix is 10 (decimal)

- Only the first number in the string is returned.
- Leading and trailing spaces are allowed.
- If the first character cannot be converted to a number, parseInt() returns NaN.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
            document.write(parseInt("10")+"<br>");
            document.write(parseInt("12.00")+"<br>");
            document.write(parseInt("15.45")+"<br>");
            document.write(parseInt("10 20 30")+"<br>");
            document.write(parseInt("   90   ")+"<br>");
            document.write(parseInt("10 years")+"<br>");
            document.write(parseInt("years 10")+"<br>");
            document.write(parseInt("020")+"<br>");
            document.write(parseInt("12", 8)+"<br>");// 12 octal = 10 decimal
            document.write(parseInt("0x12")+"<br>");// 12 hex = 18 decimal
            document.write(parseInt("10", 16)+"<br>");// 10 hex = 16 decimal
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/numbers_13.png
   :width: 800

3. parseFloat ()
^^^^^^^^^^^^^^^^

- The parseFloat() function parses a string and returns a floating point number.
- This function determines if the first character in the specified string is a number.
- If it is, it parses the string until it reaches the end of the number, and returns the number as a number, not as a string.

Syntax:

.. code-block:: javascript

    parseFloat(string)

- Only the first number in the string is returned!
- Leading and trailing spaces are allowed.
- If the first character cannot be converted to a number, parseFloat() returns NaN.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
            document.write(parseFloat("10")+"<br>");
            document.write(parseFloat("12.00")+"<br>");
            document.write(parseFloat("15.45")+"<br>");
            document.write(parseFloat("10 20 30")+"<br>");
            document.write(parseFloat("   90   ")+"<br>");
            document.write(parseFloat("10 years")+"<br>");
            document.write(parseFloat("years 10")+"<br>");
            document.write(parseFloat("020")+"<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/numbers_14.png
   :width: 800

