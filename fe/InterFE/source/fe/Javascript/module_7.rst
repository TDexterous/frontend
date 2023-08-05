Module 7 : JAVASCRIPT - Prompt Method()
=======================================

- prompt() : The browser provides a built-in function which can be used to get input from the user, named prompt.
- The prompt() method displays a dialog box that prompts the visitor for input. 
- Once the prompt function obtains input from the user, it returns that input. 

Syntax:

.. code-block:: javascript
    
    prompt(text, defaultText)

Ex-1:

.. code-block:: javascript
   :linenos:
   
   prompt("Enter Your Name : ", "name");
   prompt("Enter Your Roll No. : ");

Ex-2:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        
        <body>
        <script>
            var a = prompt("Enter Your Name: ", "Techno-Dexterous");
            document.write(a);
        </script>
    </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/input_1.png
   :width: 600

- If you press ok it will show below output.

.. image:: D:/Courses/Javascript_images/input_2.png
   :width: 400

