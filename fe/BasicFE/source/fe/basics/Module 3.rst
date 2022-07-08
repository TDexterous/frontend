Module 3 : HTML-Basic Formatting Tags
=====================================


1) HTML Basic Tags
-------------------

1) Heading Tag :
    HTML has 6 levels of headings. While displaying any heading , browser adds one line before and one after that heading.

Ex. :

.. code-block:: html
    :linenos:

    <!DOCTYPE html>
    <html>
        <head>
            <title>Heading Example</title>
        </head>
        <body>
            <h1>Heading 1</h1>
            <h2>Heading 2</h2>
            <h3>Heading 3</h3>
            <h4>Heading 4</h4>
            <h5>Heading 5</h5>
            <h6>Heading 6</h6>
        </body>
    </html>


2) Paragraph Tag :

Ex. :

.. code-block:: html
    :linenos:

    <!DOCTYPE html>
    <html>
        <head>
            <title>Paragraph Example</title>
        </head>
        <body>
            <p> This is paragraph 1 </p>
            <p> This is paragraph 2 </p>
        </body>
    </html>

3) Line Break Tag :
    There is space after **br** then forward slash **<br />**.

Ex. :

.. code-block:: html
    :linenos:

    <!DOCTYPE html>
    <html>
        <head>
            <title>Line Break  Example</title>
        </head>
        <body>
            <p> Hello <br />
                You delivered the parcel.<br />
                Thanks<br />
                XYZ </p>
        </body>
    </html>

4) Centering Content :
    You can use **<center>** tag to put any content in the center of the page or any table cell.

Ex. :

.. code-block:: html
    :linenos:

    <!DOCTYPE html>
    <html>
        <head>
            <title> Centring Content Example </title>
        </head>
        <body>
            <p> Example of Centering Content </p>
            <center>
                <p> This is Centering Content text </p>
            </center>
        </body>
    </html>

5) Horizontal Lines :
    Horizontal lines are used to visually break-up sections of a document.

    The <hr> tag creates a line from the current position in the document to the right margin and breaks the line.

Ex. :

.. code-block:: html
    :linenos:

    <!DOCTYPE html>
    <html>
        <head>
            <title>Horizontal Line Example</title>
        </head>
        <body>
            <p>This is the ex. of Horizontal Line</p>
            <hr />
            <p>This is line below the Horizontal Line</p>
        </body>
    </html>

6) Preserve Formatting

Ex. :

.. code-block:: html
    :linenos:

    <!DOCTYPE html>
    <html>
        <head>
            <title>Preserve Formatting Example</title>
        </head>
        <body>
            <pre>
                function testFunction( Example ){
                    alert (Example)
                }
            </pre>
        </body>
    </html>

2) HTML Formatting Tags
------------------------
    Formatting Tags used to format your text in special types.

    * <b> - Bold text
    * <strong> - Important text
    * <i> - Italic text
    * <em> - Emphasized text
    * <mark> - Marked text
    * <small> - Smaller text
    * <del> - Deleted text
    * <ins> - Inserted text
    * <sub> - Subscript text
    * <sup> - Superscript text

    Ex. :

    * <b> This is bold text </b>

    * <strong> This text is important! </strong>

    * <i> This text is italic </i>

    * <em> This text is emphasized </em>

    * <small> This is smaller text. </small>

    * <p> Do not forget to complete <mark> Assignment </mark> today.</p>

    * <p>My favorite color is <del> Green </del> Blue </p>

    * <p>My favorite color is <del>Green</del> <ins>Blue</ins>.</p>

    * <p>This is <sub>subscripted</sub> text.</p>

    * <p>This is <sup>superscripted</sup> text.</p>


3) HTML Color Coding
---------------------

You can set the color for page level or for particular tags.

We will see for **<body>** tag ie. Page level.

The body tag has following attributes :

    * bgcolor = color for the background of the page.

    * text = color for the text.

    * alink = active links or selected links.

    * link = linked text color.

    * vlink = visited link color.


Ex. : 

.. code-block:: html
    :linenos:

    <!DOCTYPE html>
    <html>
        <head>
            <title>HTML Colors by Name</title>
        </head>
        <body text = "blue" bgcolor = "green">
            <p>This is Example for the color</p>
        </body>
    </html>


Color Coding Methods
####################
There are following three different methods to set colors in your web page :

    a) Color names = You can specify color names directly like green, blue or red , etc.

    b) Hex codes = A six-digit code which shows the amount of red, green, and blue that makes up the color.

    c) Color decimal or percentage(%) values = This value is specified using the rgb( ) property.

a) Color names : 
    W3C Standard 16 Colors 

    +------------+------------+-----------+-----------+
    |   Black    |    Gray    | Silver    | White     | 
    +------------+------------+-----------+-----------+
    |   Yellow   |    Lime    | Aqua      | Fuchsia   |
    +------------+------------+-----------+-----------+
    |    Red     |    Green   | Blue      | Purple    |
    +------------+------------+-----------+-----------+
    |   Maroon   |    Olive   | Navy      | Teal      |
    +------------+------------+-----------+-----------+


b) Hex Code :
    A hexadecimal is a 6 digit representation of a color. 

    * First 2 digits (RR) represent Red 
    * Next 2 digits (GG) Green 
    * Last 2 digits (BB) Blue


    The each hex codes starts with hash (#) sign.
    Ex. :

    +------------+------------+-----------+
    |  #000000   |   #00FF00  | #FFFF00   | 
    +------------+------------+-----------+
    |  #FF0000   |   #0000FF  | #00FFFF   |
    +------------+------------+-----------+
    |  #FF00FF   |   #C0C0C0  | #FFFFFF   |
    +------------+------------+-----------+


c) RGB Values :
    The color value is specified using the rgb( ).

    The rgb takes three values ie. red, green, and blue and each value of red, green, and blue is between 0 and 255 or a percentage.

    Ex. : rgb(0,0,0) , rgb(255,0,0) , rgb(0,255,0)




   
