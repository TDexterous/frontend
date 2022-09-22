Module 2 : HTML-Introduction
============================

1) History of HTML
------------------

* HTML was created by Sir Tim Berners-Lee in late 1991 but was not officially released. It was published in 1995 as HTML 2.0.

* HTML 4.01 was published in late 1999 and was a major version of HTML.

* Currently used version of HTML is HTML 5.0

* It is an extended version of HTML 4.01 which was published in year 2012.

2) What you need to do to get going and make your first HTML Page
-----------------------------------------------------------------

    1) Text-Editor :
        - Notepad 
        - Visual Studio considered
        - Atom
        - Sublime Text

    2) Browser :
        - Chrome
        - Safari
        - Firefox
        - Microsoft Edge

**A Simple HTML document**

.. code-block:: html
    :linenos:

    <!DOCTYPE html>
    <html>
    <head>
    <title> Page title </title>
    </head>
    <body>
        <h1> My First heading </h1>
        <p> My first Paragraph </p>
    </body>
    </html>


* The <!DOCTYPE html> declaration defines that this document is an HTML5 document

* The <html> element is the root element of an HTML page

* <head> element contains meta information about the HTML page

* <title> element specifies a title for the HTML page (in the browser's title bar)

* <body> element is a container for all the visible contents, such as headings, paragraphs, images, hyperlinks, tables, lists, etc.

* <h1> element defines a large heading

* <p> element defines a paragraph



**HTML Element = <p> This is a paragraph </p>**

where , 
    - <p> This is a paragraph </p> = Element
    - This is a paragraph          = Content
    - <p>                          = Opening Tag
    - </p>                         = Closing Tag



* The main  parts of element are :
    - Opening tag
    - Closing tag
    - Content

3) What are HTML Tags and Attributes ?
--------------------------------------

HTML Tags
#########

* HTML Tags are like keywords which defines that how web browser will format and display the content.
* HTML tags must enclosed within **<>** these brackest.
* Every tag in HTML perform different tasks.

    <tagname> Content </tagname>

* Some tag doesn't have closing tag

    - <br> Stands for line break
    - <hr> Stands for Horizontal line

HTML Attribute
##############

* An Attribute provides extra information about an HTML element

* It has two sections :

    a) Name of Attribute
    b) Value of Attribute

a) The name defines the property that we require to sections
b) The Value is a propertythat defines the value of that property

Ex. <p id ="attribute">This is attribute ex</p>

* Tag is a way of denoting HTML element in the program
* An attribute is a way of defining the characteristics od an HTML element
* Whereas element is the collection of start-tag, it's attribute and end-tag and everything in between.

4) HTML Tag vs. Element
-----------------------

5) HTML Attributes
------------------

