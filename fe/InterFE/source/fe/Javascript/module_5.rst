Module 5 : JAVASCRIPT - Datatype
================================

- In JavaScript we do not need to specify type of the variable because it is dynamically used by JavaScript engine.
- We can use var data type. It can hold any type of data like String, Number, Boolean, etc. 

Primitive Data Type
-------------------

- In JavaScript, primitive data types are basic values that represent single values.
- They are immutable (cannot be changed) and are copied by value.
- JavaScript has six primitive data types:

1. Number
^^^^^^^^^

- Represents both integer and floating-point numbers.
- Examples: 42, 3.14, -10.

Ex:

.. code-block:: javascript
   :linenos:

    var age = 25;
    console.log(age); // Outputs: 25

2. String
^^^^^^^^^

- Represents a sequence of characters.
- Examples: 'hello', "world", '123'.

Ex:

.. code-block:: javascript
   :linenos:

    var name = "Alice";
    console.log(name); // Outputs: Alice

3. Boolean
^^^^^^^^^^

- Represents a logical value, either true or false.

Ex:

.. code-block:: javascript
   :linenos:

    var isStudent = true;
    console.log(isStudent); // Outputs: true

4. Undefined
^^^^^^^^^^^^

- Represents a variable that has been declared but has not been assigned a value.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var a;	
                // Value not assigned Undefined
                document.write(a + "<br>");	
                
                // b doesnt exist undefined
                document.write(typeof(b) + "<br>");	

                // Undefined Error			
                document.write(b + "<br>");
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    undefined
    undefined

5. Null
^^^^^^^

- Represents the intentional absence of any value or object.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var a = null;	
                document.write(a + "<br>");	
                document.write(typeof(a) + "<br>");
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    null
    object

**Undefined Vs Null**

- Undefined means the value hasn't been set, whereas null means the value has been set to be empty.

6. Symbol (introduced in ECMAScript 6)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Represents a unique and immutable value used as an identifier for object properties.

Ex:

.. code-block:: javascript
   :linenos:

    // Symbol
    var sym1 = Symbol("description");
    var sym2 = Symbol("description");

    console.log(sym1 === sym2); // false, symbols are always unique

- It's important to note that primitive data types are compared by value.
- When you assign a primitive value to a variable or pass it as a function argument, a copy of that value is made.
- This means that changing the value of one variable won't affect the value of another variable that was assigned the same value.

Ex:

.. code-block:: javascript
   :linenos:

    var a = 10;
    var b = a;

    b = 20;

    console.log(a); // 10
    console.log(b); // 20


Non-Primitive Data type
-----------------------

- In JavaScript, non-primitive data types are more complex data structures that can hold multiple values and have methods and properties associated with them.
- Unlike primitive data types, non-primitive data types are mutable (can be changed) and are compared by reference.
- JavaScript has three primary non-primitive data types:

1. Object
^^^^^^^^^

- Objects are collections of key-value pairs, where each key is a string (or Symbol) that maps to a value.
- Objects can represent a wide range of data structures, including arrays, functions, and custom-defined objects.
- Objects are used to store and organize data in a structured manner.

Ex:

.. code-block:: javascript
   :linenos:

    var person = {
        firstName: "John",
        lastName: "Doe",
        age: 30
    };

    console.log(person.firstName); // Outputs: John

2. Array
^^^^^^^^

- Arrays are ordered lists of values, indexed by integers.
- They are used to store multiple values of any data type, and they have various built-in methods for manipulation and traversal.

Ex:

.. code-block:: javascript
   :linenos:

    var numbers = [1, 2, 3, 4, 5];
    console.log(numbers[2]); // Outputs: 3

3. Function
^^^^^^^^^^^

- Functions are blocks of reusable code that can be executed when invoked.
- In JavaScript, functions are considered first-class citizens, meaning they can be assigned to variables, passed as arguments, and returned from other functions.

Ex:

.. code-block:: javascript
   :linenos:

    function add(a, b) {
        return a + b;
    }

    var result = add(3, 5);
    console.log(result); // Outputs: 8

- Additionally, there are two specialized non-primitive data types introduced in ECMAScript 6:

4. Map
^^^^^^

- Maps are collections of key-value pairs, allowing any data type as keys, and preserving insertion order.

Ex:

.. code-block:: javascript
   :linenos:

    // Create a new Map
    var map = new Map();

    // Add key-value pairs
    map.set("name", "John");
    map.set("age", 30);

    // Access values using keys
    console.log(map.get("name")); // Outputs: John

    // Determine if a key exists
    console.log(map.has("age")); // Outputs: true

5. Set
^^^^^^

- Sets are collections of unique values of any data type.

Ex:

.. code-block:: javascript
   :linenos:

    // Create a new Set
    var set = new Set();

    // Add values
    set.add(42);
    set.add("hello");
    set.add(true);

    // Check if a value exists
    console.log(set.has("hello")); // Outputs: true

    // Delete a value
    set.delete(42);

- These non-primitive data types provide powerful tools for managing and manipulating complex data structures in JavaScript applications.

