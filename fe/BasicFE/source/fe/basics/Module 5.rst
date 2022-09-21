Module 5 : HTML-Lists
=====================

* It is used to list out some information.
* There are three different types of lists. 

    1) Ordered List or Numbered List (ol)
    2) Unordered List or Bulleted List (ul)
    3) Description List or Definition List (dl)


1) Ordered Lists :
------------------

    - In this type of list, all the list items are marked with numbers by default.
    - The ordered list starts with **<ol>** tag and the list items start with **<li>** tag.


Ex. 
    .. code-block:: html
        :linenos:

        <!DOCTYPE>
        <html>  
        <body>  
        <ol>  
            <li>ABC</li>  
            <li>PQR</li>  
            <li>XYZ</li>    
        </ol>  
        </body>
        </html>


Output : 

    1. ABC
    2. PQR
    3. XYZ


* There can be different types of ordered list:

    - Numeric Number (1, 2, 3)
    - Capital Roman Number (I, II, III)
    - Small Romal Number (i ,ii ,iii)
    - Capital Alphabet (A ,B ,C)
    - Small Alphabet (a ,b ,c)

* To specify in which type we want our list to be displayed, we need to add a property to our <ol> tag.
    i.e. **<ol type="I">**


Ex. 
    .. code-block:: html
        :linenos:

        <!DOCTYPE html>
        <html>
        <body>
            <ol type="I">  
                <li>ABC</li>  
                <li>PQR</li>  
                <li>XYZ</li>    
            </ol>  
        </body>
        </html>

Output :

    I.ABC

    II.PQR

    III.XYZ

* **Default type of <ol> is Numeric Number.**


2) Unordered Lists
------------------

    - In this the list items are marked with bullets.
    - It starts with <ul> tag and list items start with the <li> tag.

Ex. 
    .. code-block:: html
        :linenos:

        <!DOCTYPE>
        <html>  
        <body>  
            <ul>  
                <li>ABC</li>  
                <li>PQR</li>  
                <li>XYZ</li>    
            </ul>  
        </body>
        </html>

Output : 

    * ABC
    * PQR
    * XYZ

The Unordered list has 4 types to display li items
    * disc
    * circle
    * square
    * none

Ex. 
    .. code-block:: html
        :linenos:

        <!DOCTYPE>
        <html>  
        <body>  
            <ul type="square">  
                <li>ABC</li>  
                <li>PQR</li>  
                <li>XYZ</li>    
            </ul>
        </body>
        </html>


* **Default type of Unordered list is disc.**


3) Definition List
------------------

This list contains three tags :

    * <dl> tag - start of the list.
    * <dt> tag - defines a term.
    * <dd> tag - for term description.


Ex. 
    .. code-block:: html
        :linenos:

        <!DOCTYPE>
        <html>  
        <body>  
            <dl>
                <dt>ABC</dt>
                <dd>capital alphabets</dd>
                <dt>abc</dt>
                <dd>small alphabets</dd>
            </dl>  
        </body>
        </html>


**NOTE :**
    In HTML5 type attribute is not supported.

    Instead we can use css property of list-style-type

Ex.  
    .. code-block:: html
        :linenos:

        <!DOCTYPE>
        <html>  
        <body>  
            <ul style="list-style-type:square">  
                <li>ABC</li>  
                <li>PQR</li>      
            </ul>  
        </body>
        </html>
