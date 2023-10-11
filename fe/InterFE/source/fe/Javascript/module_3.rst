Module 3 : JAVASCRIPT - Keywords
================================

- **Keywords** in JavaScript are reserved words that can not be used as a variable name, function name or any other identifier.
- There are **46 keywords** present in JavaScript.

1. **await**
2. **break**
3. **case**
4. **catch**
5. **class**

6. **const**

- This declaration creates a constant whose scope can be either global or local to the block in which it is declared.
- Global constants do not become properties of the window object, unlike var variables.
- An initializer for a constant is required; that is, you must specify its value in the same statement in which it's declared which can't be changed later.

7. **continue**
8. **debugger**
9. **default**
10. **delete**
11. **do**
12. **else**
13. **enum**
14. **export**
15. **extends**
16. **false**
17. **finally**
18. **for**
19. **function**
20. **if**
21. **implements**
22. **import**
23. **in**
24. **instanceof**
25. **interface**

26. **let**

- let allows you to declare variables that are limited in scope to the block, statement, or expression on which it is used.

27. **new**
28. **null**
29. **package**
30. **private**
31. **protected**
32.	**public**
33.	**return**
34.	**super**
35.	**switch**
36. **static**
37.	**this**
38.	**throw**
39.	**try**
40.	**true**

41. **typeof**

- The typeof operator is used to get the data type (returns a string) of its operand.
- The operand can be either a literal or a data structure such as a variable, a function, or an object.

Syntax:

.. code-block:: javascript

    typeof operand
    typeof(operand)

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script>
                var	a = 13;	
                document.write(typeof(a) + "<br>");	
                document.write(typeof("Hello") + "<br>");	
            </script>
        </body>
    </html>

Output:

.. code-block:: HTML

    number
    string

42.	**var**

- The scope of a variable declared with var is its current execution context, which is either the enclosing function or, for variables declared outside any function, global.

43.	**void**
44.	**while**
45.	**with**
46. **yield**

