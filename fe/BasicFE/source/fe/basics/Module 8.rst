Module 8 : HTML-Table
=====================

It allows developers to arrange data into rows and columns.

Ex. :

    .. code-block:: html
        :linenos:

        <!DOCTYPE html>
        <html>
        <body>
            <table>
                <tr>
                    <th>Sr. No</th>
                    <th>First Name</th>
                    <th>Last Name</th>
                </tr>
                <tr>
                    <td>1</td>
                    <td>Your Name</td>
                    <td>Last Name</td>
                </tr>
            </table>
        </body>
        </html>


Tag Description :
#################

    +---------------+---------------------------------------------------------------------------+
    |   <table>	    |  Defines a table                                                          |
    +---------------+---------------------------------------------------------------------------+                                                         
    |   <th>	    |  Defines a header cell in a table                                         |
    +---------------+---------------------------------------------------------------------------+
    |   <tr>	    |  Defines a row in a table                                                 |
    +---------------+---------------------------------------------------------------------------+
    |   <td>	    |  Defines a cell in a table                                                |
    +---------------+---------------------------------------------------------------------------+
    | <caption>	    |  Defines a table caption                                                  |
    +---------------+---------------------------------------------------------------------------+
    | <colgroup>    |  Specifies a group of one or more columns in a table for formatting       |
    +---------------+---------------------------------------------------------------------------+
    |   <col>	    |  Specifies column properties for each column within a <colgroup> element  |
    +---------------+---------------------------------------------------------------------------+
    |   <thead>	    |  Groups the header content in a table                                     |
    +---------------+---------------------------------------------------------------------------+
    |   <tbody>	    |  Groups the body content in a table                                       |
    +---------------+---------------------------------------------------------------------------+
    |   <tfoot>	    |  Groups the footer content in a table                                     |
    +---------------+---------------------------------------------------------------------------+


Ex. :

    .. code-block:: html
        :linenos:

        <!DOCTYPE html>
        <html>
        <body>
           <table>
            <caption>This is caption</caption>
            <tr>
                <th>ABC</th>
                <th>XYZ</th>
            </tr>
            <tr>
                <td>123</td>
                <td>456</td>
            </tr>
        </table>
        </body>
        </html>
