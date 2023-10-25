Module 4 : JAVASCRIPT - Variables
=================================

- A variable is an identifier or a name which is used to refer a value.
- A variable is written with a combination of letters, numbers and special characters _ (underscore) and $ (dollar) with the first letter being an alphabet. 

Ex: c, fact, b33, total_amount etc.

**Rules**

- Variable can contain combination of letters, digits, underscores ( _ ), and dollar signs ( $ ).
- Must begin with a letter A-Z or a-z or underscore or dollar sign.
- A variable name cannot start with a number.
- Must not contain any space characters.
- JavaScript is case-sensitive.
- Can't use reserved keywords.

Declaring Variable
------------------

- A variable declared without a value will have the value undefined.

Ex:

1. var roll;
2. var name;
3. var price;

- These all are undefined.

Initializing Variable
---------------------

- Strings are written inside double or single quotes. 
- Numbers are written without quotes.
- If you put a number in quotes, it will be treated as a text string.
- There is so many ways to declare & initialize the variables.

Ex: 

1.

.. code-block:: javascript

    var roll;
    roll = 101;

2.

.. code-block:: javascript
    
    var name; 
    name = "techno dexterous";

3.

.. code-block:: javascript
    
    var price;
    price = 125.36;

- You can also declare & initialize the variable like below:

1. var roll = 101;
2. var name = "geeky shows";
3. var price = 125.36;

- One more way is there to declare & initialize the variable,

1. roll = 101;
2. name = "geeky shows";
3. price = 125.36;

- You can also declare & initialize variables with boolean values like below:

1. var ans = true;
2. var result = false;

- You can also declare & initialize multiple variables in one line like below:

1. var x = 10, y = 20, c = 30;
2. var fname = "techno", lname = "dexterous";
3. var name = "techno dexterous", roll = 101;

- You can also declare & initialize multiple variables like below:

.. code-block:: javascript
    
    var name = "techno dexterous",
        roll = 101,
        address = "Steel City";

Re-Declaring Variable
---------------------

- If you re-declare a JavaScript variable, it will not lose its value.

**Example:**

.. code-block:: javascript
    
    var name = "techno dexterous";
    var name;

    document.write(name);

**Output:**

.. code-block:: javascript
    
    techno dexterous

JavaScript Code Best Practices
------------------------------

- The statements are executed, one by one, in the same order as they are written.
- JavaScript programs (and JavaScript statements) are often called JavaScript code.
- Semicolons separate JavaScript statements.
- Ending statements with semicolon is not required, but highly recommended.
- JavaScript ignores multiple spaces.
- Use line Break (Enter Key).

