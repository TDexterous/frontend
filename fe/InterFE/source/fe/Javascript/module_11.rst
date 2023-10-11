Module 11 : JAVASCRIPT - Loop Control
=====================================

1) Break Statement
------------------

- This statement is used to "jumps out" of a loop.
- The break statement breaks the loop and continues executing the code after the loop (if any).

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
        <script>
            for(i=1; i<=10; i++)
            {
                if(i==8)
                {
                    break;	// stop loop
                }
                document.write(i);
                document.write("<br>");
            }
        </script>
    </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/break.png
   :width: 300

2) Continue Statement
---------------------

- This statement is used to "jumps over" one iteration in the loop.
- The continue statement breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
        <script>
            for(i=1; i<=10; i++)
            {
                if(i==8)
                {
                    continue;	// skip loop
                }
                document.write(i);
                document.write("<br>");
            }
        </script>
    </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/continue.png
   :width: 300

