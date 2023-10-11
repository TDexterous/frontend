Module 2 : JAVASCRIPT - Display
===============================

- We have seen some functions earlier. These are some types of functions below:

1. document.write( )
2. window.alert( )
3. console.log( )
4. innerHTML

- We will see them one by one.

1) document.write( )
--------------------

- This function is used to write arbitrary HTML and content into page.
- If we use this function after an HTML document is fully loaded, will delete all existing HTML.
- It is used only for testing purpose.

Ex:

1. document.write("Hello World");
2. document.write(variable);
3. document.write(4+2);
4. document.write("Hello World.<br>");
5. document.write("Hello World.<br>" + variable + "<br>");

2) window.alert( )
------------------

- This function is used to display data in alert dialog box.
- Alert really should be used only when you truly want to stop everything and let the user know something.

Ex:

1. window.alert("Hello World");
2. window.alert(variable);
3. window.alert(4+2);
4. window.alert("Hello World" + variable);

3) console.log( )
-----------------

- This function is used to display data in console.
- This is used for debugging purpose. We can identify our code's error.

Ex:

1. console.log("Hello World");
2. console.log(variable);
3. console.log(4+2);
4. console.log("Hello World" + variable);

4) innerHTML
------------

- To access an HTML element, JavaScript can use the document.getElementById(id) method.
- The id attribute defines the HTML element.
- The innerHTML property defines the HTML content:

Ex:

1. document.getElementById("demo").innerHTML = 5 + 6;
2. document.getElementById("demo").innerHTML = "Hello, World!";
3. document.getElementById("demo").innerHTML = '<a href="https://www.techno-dexterous.com/">Visit techno-dexterous Website</a>';
4. document.getElementById("demo").innerHTML = '<h2>Title</h2><p>This is a paragraph.</p>';

Identifier
----------

- An identifier is a name having a few letters, numbers and special characters _ (underscore).
- It is used to identify a variable, function, symbolic constant and so on.

Ex: 
	
1. X2
2. PI
3. Sigma
4. matadd

Comments
--------

- There is 2 types of Comments shown below:

1. Single Line Comment
2. Multi Line Comment

- Let's see them one by one:

1. Single Line Comment
^^^^^^^^^^^^^^^^^^^^^^

- Single line comments start with //.
- Text between // and the end of the line will be ignored by JavaScript. 

Ex:

.. code-block:: HTML
   :linenos:

   // you can assign any type of value
   var imvalue = 101;

.. code-block:: HTML
   :linenos:

   var imvalue = 101;    // assign any type of value

2. Multi Line Comment
^^^^^^^^^^^^^^^^^^^^^

- Multi-line comments start with ``/*`` and end with ``*/``.
- Any text between ``/*`` and ``*/`` will be ignored by JavaScript.

Ex:

.. code-block:: HTML
   :linenos:
   
   /* Comment Here */

- Adding // in front of a code line changes the code lines from an executable line to a comment.

.. code-block:: HTML
   :linenos:
   
   var imvalue = 101;
   // var imvalue = 101;

