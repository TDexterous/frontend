Module 9 : JAVASCRIPT - Switch Statement
========================================

- Check several possible constant values for an expression.

Syntax-1:

.. code-block:: javascript

    switch(expression){
        case expression 1:
            block of statements 1;
            break;
        case expression2;:
            block of statements 2;
            break;
        .
        .
        default:
            default block of instructions;
        }

- All the cases will be evaluated if you don't use break statement.

Syntax-2:

.. code-block:: javascript

    switch(expression){
        case expression 1:
            block of statements 1;
            break;
        case expression 2:
        case expression 3:
            block of statements 2;
            break;
        
        default:
            default block of instructions;
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
            var day = "Sat";
            switch(day){
                case "mon":
                case "Mon":
                document.write("Working Day");
                break;
                case "Sat":
                case "Sun":
                document.write("Holiday");
                break;
                default:
                document.write("Wrong");
            }
        </script>
    </body>
    </html>

- After executing above example it will show below output.

Output:

.. code-block:: HTML

    Holiday

