Module 18 : JAVASCRIPT - Array Functions
========================================

1) Concat () Method
-------------------

- The concat() method is used to merge two or more arrays.
- This method does not change the existing arrays, but instead returns a new array.

Syntax-1:

.. code-block:: javascript

    new_array = old_array.concat(value1, value2, value_n);

Syntax-2:

.. code-block:: javascript

    new_array = old_array1.concat(old_array2, old_array_n);

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // concat method
                
                // Concat Values
                var techno1 = ["Rahul", "Sonam", "Sumit"];
                var new_techno = techno1.concat("Raj", "Rohit");
                document.write(new_techno + "<br>");
                
                // concat two arrays
                var techno1 = ["Rahul", "Sonam", "Sumit"];
                var techno2 = ["Raj", "Rohan"];
                var new_techno = techno1.concat(techno2);
                document.write(new_techno + "<br>");
                
                // concat Three arrays
                var techno1 = ["Rahul", "Sonam", "Sumit"];
                var techno2 = ["Raj", "Rohan"];
                var techno3 = ["Priya", "Komal"];
                var new_techno = techno1.concat(techno2, techno3);
                document.write(new_techno + "<br>");	
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_function.png
   :width: 800

2) Join () Method
-----------------

- The join() method joins the elements of an array into a string, and returns the string.
- The elements will be separated by a specified separator. The default separator is comma (,).

Syntax:

.. code-block:: javascript

    array_name.join(separator);

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // join method
                var techno = ["Rahul", "Sonam", "Sumit"];
                
                // separated by /
                var new_techno = techno.join(" / ");
                document.write(new_techno + "<br>");
                
                // separated by or
                var new_techno = techno.join(" or ");
                document.write(new_techno + "<br>");
                
                // separated by no space
                var new_techno = techno.join("");
                document.write(new_techno + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_function_1.png
   :width: 800

3) Reverse () Method
--------------------

- The reverse() method reverses the order of the elements in an array.

Syntax:

.. code-block:: javascript

    array_name.reverse( );

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // Reverse Method
                var techno = ["Rahul", "Sonam", "Sumit"];
                techno.reverse();
                document.write(techno);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_function_2.png
   :width: 800

4) Slice() Method
-----------------

- The slice() method returns a shallow copy of a portion of an array into a new array object selected from begin to end (end not included).
- The original array will not be modified.

Syntax:

.. code-block:: javascript

    array_name.slice(start, end)

**Start**

- If begin is undefined, slice begins from index 0.
- If begin is greater than the length of the sequence, an empty array is returned.
- A negative index can be used, indicating an offset from the end of the sequence. slice(-2) extracts the last two elements in the sequence.

**End**

- If end is omitted, slice extracts through the end of the sequence (arr.length).
- If end is greater than the length of the sequence, slice extracts through to the end of the sequence (arr.length).
- A negative index can be used, indicating an offset from the end of the sequence. slice(2,-1) extracts the third element through the second-to-last element in the sequence.
- slice extracts up to but not including end.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // Slice Method
                var techno = ["Rahul", "Sonam", "Sumit", "Raj", "Rohan"];
                var new_techno = techno.slice(1, 3);
                document.write(new_techno + "<br>");
                
                var new_techno = techno.slice(-3, -1);
                document.write(new_techno + "<br>");
                
                var new_techno = techno.slice(1, 9);
                document.write(new_techno + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_function_3.png
   :width: 800

5) toString() Method
--------------------

- The toString () Method returns a string containing the comma-separated values of the array.
- This method is invoked automatically when you print an array.
- It is equivalent to invoking join () method without any arguments.
- The returned string will separate the elements in the array with commas.

Syntax:

.. code-block:: javascript

    array_name.toString();

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var techno = ["Rahul", "Sonam", "Sumit", "Raj"];
                techno.toString();
                document.write(techno);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_function_4.png
   :width: 800

6) Array.isArray () Method
--------------------------

- The Array.isArray() method determines whether the passed value is an Array.
- This function returns true if the object is an array, and false if not. 

Syntax:

.. code-block:: javascript

    Array.isArray(value);

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var techno = ["Rahul", "Sonam", "Sumit", "Raj"];
                var result1 = Array.isArray(["Rose", "Khoj"]);
                var result2 = Array.isArray("IAmString");
                var result3 = Array.isArray(techno);
                document.write(result1 + "<br>");
                document.write(result2 + "<br>");
                document.write(result3 + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_function_5.png
   :width: 800

7) Splice () Method
-------------------

- The splice() method changes the contents of an array by removing existing elements and/or adding new elements.
- This method changes the original array.

Syntax:

.. code-block:: javascript

    array_name.splice (start, deletecount, replacevalues);

**Start** - The first argument start specifies at what position to add/remove items, use negative values to specify the position from the end of the array.

**Deletecount** - The second argument deletecount, is the number of elements to delete beginning with index start. 

**Replacevalues** - replacevalues are inserted in place of the deleted elements. If more than one separate it by comma. 

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // Splice Method
                var techno = ["Rahul", "Sonam", "Sumit", "Raj", "Rohan"];
        
                // Remove All elements from index 2 (including index 2)
                techno.splice(2);
                document.write(techno);
        /*
                // Remove 1 element from index 2
                // it will remove index 2 element
                techno.splice(2, 1);
                document.write(techno);
                
                // Remove 2 element from index 2
                // it will remove index 2 and 3, element
                techno.splice(2, 2);
                document.write(techno);
        
                // Remove 0 element from index 2 and insert "Dell"
                // it will not remove anything but will insert "Dell" at position 2
                techno.splice(2, 0, "Dell");
                document.write(techno);

                // Remove 2 element from index 2 and insert "Dell" and "HP"
                techno.splice(2, 2, "Dell", "HP");
                document.write(techno);
        */		
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_function_6.png
   :width: 800

8) IndexOf () Method
--------------------

This method allows to easily find the occurrence of an item in an array.

- If the item not found, it returns -1.
- The search will start at the specified position, or at the beginning if no start position is specified, and end the search at the end of the array.
- If the item is present more than once, the indexOf method returns the position of the first occurrence.

Syntax:

.. code-block:: javascript

    var position = array_name.indexOf(item, start);

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var techno = ["Rahul", "Sonam", "Raj", "Sumit", "Raj"];
                var position1 = techno.indexOf("Raj");
                var position2 = techno.indexOf("Raj", 3);
                var position3 = techno.indexOf("Priti");
                document.write(position1 + "<br>");
                document.write(position2 + "<br>");
                document.write(position3 + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_function_7.png
   :width: 800

9) Fill () Method
-----------------

- The fill() method fills all the elements in an array with a static value.

Syntax:

.. code-block:: javascript

    array_name.fill(value, start, end)

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var techno = ["Rahul", "Sonam", "Raj", "Sumit"];
                
                // All elements Don
                techno.fill("Don");	
                document.write(techno);
            /*	
                // fill Don start with Index 1 to 3 (3 not included)
                techno.fill("Don", 1, 3);
                document.write(techno);
            
                // Creating empty array length 3 and fill it with Jay
                var new_arr = new Array(3).fill("Jay");
                document.write(new_arr);
            */
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_function_8.png
   :width: 800

10) unshift () Method
---------------------

- The unshift() method adds one or more elements to the beginning of an array and returns the new length of the array.
- This method changes the length of an array.

Syntax:

.. code-block:: javascript

    Array_name.unshift(value1, value2, value_n);

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var techno = ["Rahul", "Sonam", "Raj", "Sumit"];
                // it will add two new elements at the beginning as well return new length of array
                var techno_length = techno.unshift("Dell", "HP");
                document.write(techno + "<br>");
                document.write(techno_length);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_function_9.png
   :width: 800

11) Push () Method
------------------

- The push() method adds one or more elements to the end of an array and returns the new length of the array.
- The new item will be added at the end of the array.
- This method changes the length of the array.

Syntax:

.. code-block:: javascript

    Array_name.push(value1, value2, value_n);

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var techno = ["Rahul", "Sonam", "Raj", "Sumit"];
                // it will add two new elements at the end as well return new length of array
                var techno_length = techno.push("Dell", "HP");
                document.write(techno + "<br>");
                document.write(techno_length);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_function_10.png
   :width: 800

12) Shift() Method
------------------

- The shift() method removes the first element from an array and returns that removed element.
- This method changes the length of the array.

Syntax:

.. code-block:: javascript

    array_name.shift( );

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var techno = ["Rahul", "Sonam", "Raj", "Sumit"];
                // it will remove element from the beginning as well return removed element
                var techno_removed = techno.shift();
                document.write(techno + "<br>");
                
                // removed element
                document.write(techno_removed);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_function_11.png
   :width: 800

13) pop() Method
----------------

- The pop() method removes the last element from an array and returns that removed element.
- This method changes the length of the array.

Syntax:

.. code-block:: javascript

    array_name.pop( );

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var techno = ["Rahul", "Sonam", "Raj", "Sumit"];
                // it will remove last element and return removed element
                var techno_removed = techno.pop();
                document.write(techno + "<br>");
                
                // removed element
                document.write(techno_removed);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_function_12.png
   :width: 800

14) Map () Method
-----------------

- The map() method creates a new array with the results of calling a provided function on every element in the calling array.
- The map() method calls the provided function once for each element in an array, in order.
- map() does not execute the function for array elements without values.
- map() does not change the original array.

Syntax:

.. code-block:: javascript

    array_name.map(function(currentValue, index, array)
    {

    }, thisValue)

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
    <head>
        <title>Techno Dexterous</title>
    </head>
    <body>
        <script>
            var techno = ["Rahul", "Sonam", "Raj", "Sumit"];

            // Use the map method to create a new array with the names in uppercase
            var technoUpperCase = techno.map(function(name) {
                return name.toUpperCase();
            });

            document.write("Original Array: " + techno + "<br>");
            document.write("Array with Uppercase Names: " + technoUpperCase + "<br>");
        </script>
    </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/array_function_13.png
   :width: 800

