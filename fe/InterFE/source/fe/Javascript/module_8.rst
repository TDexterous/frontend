Module 8 : JAVASCRIPT - If Statement
====================================

1) If Statement
---------------

- It is used to execute an instruction or block of instructions only if a condition is fulfilled.

Syntax:

.. code-block:: javascript

   if (condition)
	  {
	  	block of statements;
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
            var a = prompt("Enter Your Roll: ");
            if((a == 10))
            document.write("Name: Rahul");
        </script>
    </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/if_1.png
   :width: 600

- In the dialog box given above if you enter 10 & press ok it will show below output.
- Otherwise, it will show nothing or empty Page.

.. image:: D:/Courses/Javascript_images/if_2.png
   :width: 400

If statement with logical operator
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Syntax:

.. code-block:: javascript
    
    if ( (condition1) && (condition2) )
        {
        block of statements;
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
            var a = 10;
            var b = 20;
            if((a == 10) && (b == 20))
            document.write("Techno Dexterous");
        </script>
    </body>
    </html>

- After executing above example it will show below output.

Output:

.. code-block:: HTML

    Techno Dexterous

2) If else Statement
--------------------

- If else statement is used when a different sequence of instructions is to be executed depending on the logical value(True/False) of the condition evaluated.

Syntax:

.. code-block:: javascript

	if(condition)
	    {
	        Statement_1_Block;
	    }
	else
	   {
	        Statement_2_Block;
	   }
            Statement_3;

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
        <script>
            var a = prompt("Enter Your Roll: ");
            if(a == 10)
            document.write("Name: Rahul");
            else
            document.write("Wrong value");
        </script>
    </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/if_else_1.png
   :width: 600

- In the dialog box given above if you enter 10 & press ok it will show below output.

.. image:: D:/Courses/Javascript_images/if_else_2.png
   :width: 400

- Otherwise, if you enter a wrong value or simply press on cancel button it will show below output.

.. image:: D:/Courses/Javascript_images/if_else_3.png
   :width: 400

3) Else If Statement
--------------------

- To show a multi-way decision based on several conditions, we use else if statement.

Syntax:

.. code-block:: javascript

	If(condition_1)
	   {
	     statements_1_Block;
	   }
	else if(condition_2)
	  {
	      statement_2_Blocks;
	   }
	else if(condition_n)
	  {
	     Statements_n_Block;
	  }
	else
	     statements_x;

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
        <script>
            var result = 70;
            if(result <= 30)
            document.write("Fail");
            else if (result <= 40 )
            document.write("Pass");
            else if (result <= 60)
            document.write("Good");
            else
            document.write("Very Good");
        </script>
    </body>
    </html>

- After executing above example it will show below output.

Output:

.. code-block:: HTML

    Very Good

