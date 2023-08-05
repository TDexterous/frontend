Module 6 : JAVASCRIPT - Operators
=================================

What is an Operator?
--------------------

- In JavaScript, an operator is a symbol or special character that performs an operation on one or more operands (values or variables) and returns a result.
- Operators are fundamental components of any programming language, and they allow you to perform various computations and manipulate data.
- JavaScript includes several types of operators, such as:

1. Arithmetic Operators
2. Comparison(Relational) Operators
3. Logical Operators
4. Bitwise Operators
5. Assignment Operators

- Let's see them one by one:

1. Arithmetic Operators
-----------------------

- These Operators perform basic arithmetic operations like addition, subtraction, multiplication, division, modulus (remainder), and exponentiation.

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        
        <body>
        <script>
            var a = 20;
            var b = 10;
            var c = a + b + 30;
            document.write(c);
        </script>
    </body>
    </html>

Output:

.. code-block:: HTML

    60

Ex-2:

.. code-block:: javascript
   :linenos:

   let a = 5;
   let b = 2;
   
   console.log(a + b); // 7
   console.log(a - b); // 3
   console.log(a * b); // 10
   console.log(a / b); // 2.5
   console.log(a % b); // 1
   console.log(a ** b); // 25 (5 raised to the power of 2)

2. Comparison(Relational) Operators
-----------------------------------

- These Operators compare values and return a Boolean result (true or false).

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        
        <body>
        <script>
            var a = 10;
            var b = "10";
            var c = a === b;
            document.write(c);
        </script>
    </body>
    </html>

Output:

.. code-block:: HTML

    false

Ex-2:

.. code-block:: javascript
   :linenos:

   let num1 = 5;
   let num2 = 10;
   
   console.log(num1 < num2); // true
   console.log(num1 > num2); // false
   console.log(num1 <= num2); // true
   console.log(num1 >= num2); // false
   console.log(num1 === num2); // false (strict equality)
   console.log(num1 !== num2); // true (strict inequality)

3. Logical Operators
--------------------

- These Operators are used to combine or negate Boolean values.

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        
        <body>
        <script>
            var a = 10<5;	// false
            var b = 20<8;	// false
            var c = a || b; // false && false 
            document.write(c);
        </script>
    </body>
    </html>

Output:

.. code-block:: HTML

    false

Ex-2:

.. code-block:: javascript
   :linenos:

   let isTrue = true;
   let isFalse = false;
   
   console.log(isTrue && isFalse); // false (logical AND)
   console.log(isTrue || isFalse); // true (logical OR)
   console.log(!isTrue); // false (logical NOT)

4. Bitwise Operators
--------------------

- These Operators perform operations at the bit level.

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        
        <body>
        <script>
            var a = 5;		// 00000101
            var b = 6;		// 00000110
            var c = a | b; 	// 00000111 
            document.write(c);
        </script>
    </body>
    </html>

Output:

.. code-block:: HTML

    7

Ex-2:

.. code-block:: javascript
   :linenos:

   let num3 = 5; // Binary: 00000101
   let num4 = 3; // Binary: 00000011
   
   console.log(num3 & num4); // 1 (Bitwise AND)
   console.log(num3 | num4); // 7 (Bitwise OR)
   console.log(num3 ^ num4); // 6 (Bitwise XOR)
   console.log(~num3); // -6 (Bitwise NOT)
   console.log(num3 << 1); // 10 (Bitwise left shift)
   console.log(num3 >> 1); // 2 (Bitwise right shift)

5. Assignment Operators
-----------------------

- These Operators are used to assign values to variables.

Ex-1:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        
        <body>
        <script>
            var m = 15;
                m += 10;		// m = m+10
            document.write(m);
        </script>
    </body>
    </html>

Output:

.. code-block:: HTML

    25

Ex-2:

.. code-block:: javascript
   :linenos:

   let x = 10;
   x += 5; // Equivalent to x = x + 5
   console.log(x); // 15
   
   let y = 7;
   y *= 2; // Equivalent to y = y * 2
   console.log(y); // 14

