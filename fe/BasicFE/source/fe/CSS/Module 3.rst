Module 14 : CSS-Selectors
=========================

1) ID Selectors
---------------

2) Class Selectors
------------------

3) Grouping Selectors
---------------------

4) Universal Selectors
----------------------

5) Attribute Selectors
----------------------

6) CSS - Pseudo Classes
-----------------------

- A Pseudo class is used to define a special state of an element.

For Ex:

* Style an element when user mouses over if.
* Style visited & unvisited links differently.
* Style an element when it gets focus.

Syntax :

.. code-block:: html
    :linenos:

    Selector : Pseudo-class {
                             property : value ;
                             }
    
Anchor Pseudo-classes
#####################

Ex :

.. code-block:: html
    :linenos:

    a : link { color : #ff0000 ; }
    a : visited { color : #00ff00 ; }
    a : hover { color : #ff00ff ; }
    a : active { color : #0000ff ; }

- a : hover must come after a : link & a : visited in the CSS definition in order to be effective!
- a : active must come after a : hover.

7) Simple Selectors
-------------------

- #id -> #example -> Selects the elements with id = "example".
- .class -> .classname -> Selects all elements with class = "classname".
- element.class -> p.classname -> Selects only <p> elements with class = "classname".
- *  -> * -> Selects all elements.
- element -> p -> Selects all <p> elements.
- element.element.... -> div,p,h1 -> Selects all <div> elements, <p> elements & <h1> elements.

8) Combinators Selectors
------------------------

*  Descendant Selector(Space)
*  Child Selector(>)
*  Adjacent Sibling Selector(+)
*  General Sibling Selector(~)

A) Descendant Selector(Space)
#############################

Ex :

.. code-block:: html
    :linenos:

    div p { background-color : yellow ; }

- This selects all <p> elements inside <div> elements.

B) Child Selector(>)
####################

Ex :

.. code-block:: html
    :linenos:

    div > p { background-color : yellow ; }

- This selects all <p> elements that are children of <div> element.

**Difference between Descendant & Child Selector**

Ex :

.. code-block:: html
    :linenos:

    <div>
        <p> para1 </p> // children & descendant
        <p> para2 </p> // children & descendant
        <section>
            <p> para3 </p> // descendant but not child
        <section>
    <div>

C) Adjacent Sibling Selector(+)
###############################

Ex :

.. code-block:: html
    :linenos:

    div + p { background-color : yellow ; }

- This example selects the first <p> element that are placed immediately after <div> element.

D) General Sibling Selector(~)
##############################

Ex :

.. code-block:: html
    :linenos:

    div ~ p { background-color : yellow ; }

- This selects all <p> elements that are next siblings of <div> elements.
