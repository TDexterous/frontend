Module 1 : JAVASCRIPT - Overview
================================

1) What is JavaScript?
-----------------------

- JavaScript is the programming language of HTML and the Web. 
- It makes web page dynamic.
- It is an interpreted programming language with object-oriented capabilities.

2) JavaScript History
---------------------

- 1995 by Brendan Eich (NetScape).
- Mocha.
- LiveScript.
- JavaScript.
- ECMAScript.

3) Advantages of JavaScript
---------------------------

- Client Side Execution.
- Validation on Browser.
- Easy Language.

4) Disadvantages of JavaScript
------------------------------

- Less Secure.
- No Hardware Access.
- JavaScript Enable Browsers.

5) JavaScript Development Tools
-------------------------------

- Notepad
- Notepad ++
- Any Text Editor

6) Way of adding JavaScript
---------------------------

• Inline
   - Inside head Tag
   - Inside body Tag

• External file
   - Inside head Tag
   - Inside body Tag

1. Inline
^^^^^^^^^

**Inside head Tag**

.. code-block:: HTML
   :linenos:

   <html>

        <head>
            <title>Hello JS</title>
            <script type="text/javascript">
                document.write("Hello Techno-Dexterous");
            </script>
        </head>

        <body>
            <h1>I am Heading</h1>
            <p>I am first Paragraph.</p>
        </body>

    </html>

**Inside body Tag**

.. code-block:: HTML
   :linenos:

   <html>

        <head>
            <title>Hello JS</title>
        </head>

        <body>
            <h1>I am Heading</h1>
            <p>I am first Paragraph.</p>
            <script type="text/javascript">
                document.write("Hello Techno-Dexterous");
            </script>
        </body>

    </html>

2. External
^^^^^^^^^^^

**Inside head Tag**

.. code-block:: HTML
   :linenos:

   <html>

        <head>
            <title>Hello JS</title>
            <script src="Techno.js" type="text/javascript">
            </script>
        </head>

        <body>
            <h1>I am Heading</h1>
            <p>I am first Paragraph.</p>
        </body>

    </html>

- In above code Techno.js is present which code has below:

**Techno.js**

.. code-block:: HTML
   :linenos:
   
   document.write("Hello Techno-Dexterous");

- It is linked with HTML code.

**Inside body Tag**

.. code-block:: HTML
   :linenos:

   <html>

        <head>
            <title>Hello JS</title>
        </head>

        <body>
            <h1>I am Heading</h1>
            <p>I am first Paragraph.</p>
            <script src="Techno.js" type="text/javascript">
            </script>
        </body>

    </html>

- In above code Techno.js is present which code has below:

**Techno.js**

.. code-block:: HTML
   :linenos:
   
   document.write("Hello Techno-Dexterous");

- It is linked with HTML code.

7) Script Tag In JavaScript
---------------------------

- <script> :- Opening Script Tag.
- src :- It's an attribute of script tag. It defines source/location of script file.
- Techno.js :- This is our script file. Where Techno is file name and .js is the extension of javascript file.
- type :- It's an attribute of script tag which tells the browser it is a javascript. This is optional now a days.
- text/javascript :- Its type of document. 
- document.write("Hello World"); :- This is a function to display data.
- </script> :- Closing Script tag.

8) How to link more than one External files in JavaScript
---------------------------------------------------------

- Below is the code to link more than one External files in JavaScript.

.. code-block:: HTML
   :linenos:

   <html>

        <head>
            <title>Hello JS</title>
        </head>

        <body>
            <h1>I am Heading</h1>
            <p>I am first Paragraph.</p>

            <script src="Techno1.js" type="text/javascript"></script>
            <script src="Techno2.js" type="text/javascript"></script>
            <script src="Techno3.js" type="text/javascript"></script>
        </body>

    </html>

9) How to use Inline and External together in JavaScript
--------------------------------------------------------

- We cannot use Inline & External in one script tag.
- We can use Inline and External together with two script tags like below:

.. code-block:: HTML
   :linenos:

   <html>

        <head>
            <title>Hello JS</title>
        </head>

        <body>
            <h1>I am Heading</h1>
            <p>I am first Paragraph.</p>

            <script type="text/javascript">
                document.write("Hello world");
            </script>

            <script src="Techno.js" type="text/javascript"> </script>
        </body>

    </html>

