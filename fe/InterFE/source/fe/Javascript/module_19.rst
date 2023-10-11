Module 19 : JAVASCRIPT - Boolean
================================

- Boolean is the built-in object corresponding to the primitive Boolean data type.
- JavaScript boolean can have one of two values: true or false.

**Primitive Values**

1. var primitiveTrue = true;
2. var primitiveFalse = false;

**Boolean Function**

1. var functionTrue = Boolean(true);
2. var functionFalse = Boolean(flase);

**Boolean Constructor**

1. var constructorTrue = new Boolean(true);
2. var constructorFalse = new Boolean(false); 

- If value parameter is omitted or is 0, -0, null, false, NaN, undefined, or the empty string (""), the object has an initial value of false.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // Boolean
                document.write("10: "+Boolean(10) + "<br>");
                document.write("-10: "+Boolean(-10) + "<br>");
                document.write("0: "+Boolean(0) + "<br>");
                document.write("-0: "+Boolean(-0) + "<br>");
                document.write("Hello: "+Boolean("Hello") + "<br>");
                document.write("Empty: "+Boolean("") + "<br>");
                document.write("NaN: "+Boolean(NaN) + "<br>");
                document.write("null: "+Boolean(null) + "<br>");
                document.write("undefined: "+Boolean(undefined) + "<br>");
                document.write("true: "+Boolean(true) + "<br>");
                document.write("false: "+Boolean(false) + "<br>");
                document.write("No Para: "+Boolean() + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/boolean.png
   :width: 800

