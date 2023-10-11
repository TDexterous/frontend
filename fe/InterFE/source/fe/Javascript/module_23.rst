Module 23 : JAVASCRIPT - Math
=============================

Math
----

- The Math object holds a set of constants and methods that enable more complex mathematical operations than the basic arithmetic operators.
- We can not instantiate a Math Object.
- The Math object is static so it's properties and methods accessed directly.

**Ex:**

1. Math.PI
2. Math.abs()

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
            document.write(Math.PI + "<br>");
            document.write(Math.sqrt(64) + "<br>");		
            document.write(Math.abs(-64) + "<br>");		
            document.write(Math.abs(null) + "<br>");
            document.write(Math.pow(2, 3) + "<br>");		// 2*2*2
            document.write(Math.trunc(12.564) + "<br>");  // only integer part
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/math.png
   :width: 800

Properties
^^^^^^^^^^

- **E**: Returns Euler's number (approx. 2.718)
- **LN2**: Returns the natural logarithm of 2 (approx. 0.693)
- **LN10**: Returns the natural logarithm of 10 (approx. 2.302)
- **LOG2E**: Returns the base-2 logarithm of E (approx. 1.442)
- **LOG10E**: Returns the base-10 logarithm of E (approx. 0.434)
- **PI**: Returns PI (approx. 3.14)
- **SQRT1_2**: Returns the square root of 1/2 (approx. 0.707)
- **SQRT2**: Returns the square root of 2 (approx. 1.414)

Methods
^^^^^^^

- **Math.abs(arg)**: Returns the absolute value of arg
- **Math.acos(arg)**: Returns the arccosine of arg, in radians
- **Math.acosh(arg)**: Returns the hyperbolic arccosine of arg
- **Math.asin(arg)**: Returns the arcsine of arg, in radians
- **Math.asinh(arg)**: Returns the hyperbolic arcsine of arg
- **Math.atan(arg)**: Returns the arctangent of arg as a numeric value between -PI/2 and PI/2 radians
- **Math.atan2(arg1, arg2)**: Returns the arctangent of the quotient of its arguments
- **Math.atanh(arg)**: Returns the hyperbolic arctangent of arg
- **Math.cbrt(arg)**: Returns the cubic root of arg
- **Math.ceil(arg)**: Returns arg, rounded upwards to the nearest integer
- **Math.cos(arg)**: Returns the cosine of arg (arg is in radians)
- **Math.cosh(arg)**: Returns the hyperbolic cosine of arg
- **Math.exp(arg)**: Returns the value of Ex
- **Math.floor(arg)**: Returns arg, rounded downwards to the nearest integer
- **Math.log(arg)**: Returns the natural logarithm (base E) of arg
- **Math.random()**: Returns a random number between 0 and 1
- **Math.round(arg)**: Rounds arg to the nearest integer
- **Math.max(arg1, arg2, ...,arg_n)**: Returns the number with the highest value
- **Math.min(arg1, arg2, ...,arg_n)**: Returns the number with the lowest value
- **Math.pow(arg1, arg2)**: Returns the value of arg to the power of arg2
- **Math.sin(arg)**: Returns the sine of arg (arg is in radians)
- **Math.sinh(arg)**: Returns the hyperbolic sine of arg
- **Math.sqrt(arg)**: Returns the square root of arg
- **Math.tan(arg)**: Returns the tangent of an angle
- **Math.tanh(arg)**: Returns the hyperbolic tangent of a number
- **Math.trunc(arg)**: Returns the integer part of a number (arg)

Min and Max Method
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
            document.write(Math.min(50, 5, 90, 6, 100) + "<br>");		
            document.write(Math.max(50, 5, 90, 6, 100) + "<br>");		
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/math_1.png
   :width: 800

Floor Method
------------

- The floor() method rounds a number DOWNWARDS to the nearest integer, and returns the result.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                document.write(Math.floor(2.1) + "<br>");		
                document.write(Math.floor(6.65) + "<br>");		
                document.write(Math.floor(0.4) + "<br>");
                document.write(Math.floor(0.6) + "<br>");
                document.write(Math.floor(-2.1) + "<br>");
                document.write(Math.floor(-6.65) + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/math_2.png
   :width: 800

Round Method
------------

- The round() method rounds a number to the nearest integer.
- 6.4 will be rounded down, 6.5 will be rounded up.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                document.write(Math.round(2.1) + "<br>");
                document.write(Math.round(6.4) + "<br>");			
                document.write(Math.round(6.5) + "<br>");
                document.write(Math.round(6.6) + "<br>");			
                document.write(Math.round(0.4) + "<br>");
                document.write(Math.round(0.5) + "<br>");
                document.write(Math.round(-2.1) + "<br>");
                document.write(Math.round(-6.4) + "<br>");
                document.write(Math.round(-6.5) + "<br>");
                document.write(Math.round(-6.6) + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/math_3.png
   :width: 800

Random Method
-------------

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                document.write(Math.random() + "<br>");
                document.write(Math.random()*10 + 1);
                //var x = Math.floor((Math.random() * 100) + 1);
                // document.write(x);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/math_4.png
   :width: 800

