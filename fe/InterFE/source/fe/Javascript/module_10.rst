Module 10 : JAVASCRIPT - Loops
==============================

1) For Loop
-----------

- The for loop is frequently used, usually where the loop will be traversed a fixed number of times.

Syntax:

.. code-block:: javascript

	for (initialization;    test condition;      increment or decrement)
	{
		block of statements;
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
            for(i=0; i<5; i++)
            {
                document.write(i + "<br>");
            }
        </script>
    </body>
    </html>

Output:

.. code-block:: HTML

    0
    1
    2
    3
    4

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
        <script>
            var i = 0;
            for(; i<5; i++)
            {
                document.write(i + "<br>");
            }
        </script>
    </body>
    </html>

Output:

.. code-block:: HTML

    0
    1
    2
    3
    4

Ex-3:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
        <script>
            var i = 0;
            for(; i<5;)
            {
                i++;
                document.write(i + "<br>");
            }
        </script>
    </body>
    </html>

Output:

.. code-block:: HTML

    1
    2
    3
    4
    5

Ex-4:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
        <script>
            var i = 0;
            for(; ; i++)
            {
                if(i==3)
                {
                    break;
                }
                document.write(i + "<br>");
            }
        </script>
    </body>
    </html>

Output:

.. code-block:: HTML

    0
    1
    2

2) Nested For Loop
------------------

- For loop inside for loop.

Syntax:

.. code-block:: javascript

	for (initialization;    test condition;      increment or decrement)
	{
		block of statements;
		for (initialization;    test condition;      increment or decrement)
		{
			block of statements;
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
            for(i=0; i<3; i++)
            {
                document.write("<strong>Outer Loop </strong>");
                document.write(i);
                document.write("<br>");
                for(j=0; j<5; j++)
                {
                    document.write("Inner Loop ");
                    document.write(j);
                    document.write("<br>");
                }
            }
        </script>
    </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/nested_for_loop.png
   :width: 300

3) While Loop
-------------

- The while loop keeps repeating an action until an associated condition returns false.

Syntax:

.. code-block:: javascript

	while (test condition)
	   {
	         body of the loop;
	         increment/decrement ;
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
            var i = 0;
            while(i<4)
            {
                document.write(i);
                i++;
                document.write("<br>");
            }
        </script>
    </body>
    </html>

Output:

.. code-block:: HTML

    0
    1
    2
    3

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
        <script>
            var i = 0;
            while(true)
            {
                if(i==3)
                {
                    break;
                }
                document.write(i);
                i++;
                document.write("<br>");
            }
        </script>
    </body>
    </html>

Output:

.. code-block:: HTML

    0
    1
    2

4) Nested While Loop
--------------------

- While Loop inside While Loop.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
        <script>
            var i = 0;
            while(i<3)
            {
                document.write("<strong>Outer Loop </strong>");
                document.write(i);
                i++;
                document.write("<br>");
                var j = 0;
                while(j<5)
                {
                    document.write("Inner Loop ");
                    document.write(j);
                    j++;
                    document.write("<br>");
                }
            }
        </script>
    </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/nested_while_loop.png
   :width: 300

5) Do While Loop
----------------

