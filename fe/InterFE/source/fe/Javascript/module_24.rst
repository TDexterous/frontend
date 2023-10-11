Module 24 : JAVASCRIPT - Date
=============================

Date
----

- The Date object provides a sophisticated set of methods for manipulating dates and times.
- It reads client machine date and time so if the client's date or time is incorrect, your script will reflect this fact.
- Days of week and months of the year are enumerated beginning with zero.
- 0 - Sunday, 1 - Monday and so on
- 0 - January, 1 - February and so on
- Days of month begins with One.

Creating Date Object
--------------------

- Date objects are created with the new Date() constructor. Date Objects created by programmers are static. They do not contain a ticking clock.

Syntax:

.. code-block:: javascript

    new Date( );
    new Date(milliseconds);
    new Date(year, month, day, hours, minutes, seconds, milliseconds)
    new Date(dateString);

1. Create Date Object using Date () 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- **new Date():** It creates a new date object with the current date and time.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var tarikh = new Date();
                document.write(tarikh);
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/date.png
   :width: 800

2. Create Date Object using Date(millisecond)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- **new Date(milliseconds):** It creates a new date object as January 1, 1970, 00:00:00 Universal Time (UTC).

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var tarikh1 = new Date(1530867166586);
                var tarikh2 = new Date(8640000);
                document.write(tarikh1 + "<br>");
                document.write(tarikh2 + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/date_1.png
   :width: 800

3. Create Date Object using Date(year, month, day, hours, minutes, seconds, milliseconds)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- **new Date(year, month, day, hours, minutes, seconds, milliseconds):** It creates object with the date specified by the integer values for the year, month, day, hours, minutes, second, milliseconds. You can omit some of the arguments.

================ ===================================================
No. of arguments Description (in order)                             
================ ===================================================
7                year, month, day, hour, minute, second, millisecond
6                year, month, day, hour, minute, second
5                year, month, day, hour, minute
4                year, month, day, hour
3                year, month, day
2                year and month
1                millisecond
================ ===================================================

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
            // 0 - Sunday, 1 - Monday and so on
            // 0 - January 1 - Feb and So on
            var tarikh1 = new Date(2018, 4, 25, 9, 45, 35, 0);
            var tarikh2 = new Date(2018, 4, 25, 9, 45, 35);
            var tarikh3 = new Date(2018, 4, 25, 9, 45);
            var tarikh4 = new Date(2018, 4, 25, 9);
            var tarikh5 = new Date(2018, 4, 25);
            var tarikh6 = new Date(2018, 4);
            document.write(tarikh1 + "<br>");
            document.write(tarikh2 + "<br>");
            document.write(tarikh3 + "<br>");
            document.write(tarikh4 + "<br>");
            document.write(tarikh5 + "<br>");
            document.write(tarikh6 + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/date_2.png
   :width: 800

4. Create Date Object using Date(dateString)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- **new Date(dateString):** It creates a new date object from a date string.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
            // 0 - Sunday, 1 - Monday and so on
            // 0 - January 1 - Feb and So on
            var tarikh1 = new Date("May 12, 2018 10:16:05");

            document.write(tarikh1 + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/date_3.png
   :width: 800


For better understanding of above date objects we have following datatypes:

========== =========== =========================================
Date Type  Format      Example                                  
========== =========== =========================================
ISO Date   YYYY-MM-DD  "2018-06-21" (The International Standard)
Short Date MM/DD/YYYY  "06/21/2018"                             
Long Date  MMM DD YYYY "June 21 2018" or "21 June 2018"          
========== =========== =========================================

ISO Date
--------

- ISO 8601 is the international standard for the representation of dates and times.

============== ========================= =========================
Description    Format                    Example                  
============== ========================= =========================
Year and Month YYYY-MM                   2018-06                  
Only Year      YYYY                      2018                     
Date and Time  YYYY-MM-DDTHH:MM:SSZ      2018-06-21T12:00:00Z     
Date and Time  YYYY-MM-DDTHH:MM:SS+HH:MM 2018-06-21T12:00:00+06:30
Date and Time  YYYY-MM-DDTHH:MM:SS-HH:MM 2018-06-21T12:00:00-06:30 
============== ========================= =========================

- Date and Time is separated with a capital **T**.
- UTC time is defined with a capital letter **Z**.
- If you want to modify the time relative to UTC, remove the Z and add +HH:MM or -HH:MM instead.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
            var tarikh = new Date("2018-06");
            document.write(tarikh + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/date_4.png
   :width: 800

Short Date
----------

- Short dates are written with an "MM/DD/YYYY" format.
- In some browsers, months or days with no leading zeroes may produce an error.
- The behavior of "YYYY/MM/DD" is undefined. Some browsers will try to guess the format. Some will return NaN.
- The behavior of  "DD-MM-YYYY" is also undefined. Some browsers will try to guess the format. Some will return NaN.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
            var tarikh = new Date("06-25-2018");
            document.write(tarikh + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/date_5.png
   :width: 800

Long Date
---------

- Long dates are most often written with a "MMM DD YYYY" format.
- Month and day can be in any order.
- Month can be written in full (January), or abbreviated (Jan).
- If you write “June, 21, 2018” Commas are ignored and Names are case insensitive.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
            // var tarikh = new Date("Mar 25 2018");
            var tarikh = new Date("March 25 2018");
            document.write(tarikh + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/date_6.png
   :width: 800

Date Methods
------------

- **getDate():** Returns the day of the month (from 1-31)
- **getDay():** Returns the day of the week (from 0-6)
- **getFullYear():** Returns the year
- **getHours():** Returns the hour (from 0-23)
- **getMilliseconds():** Returns the milliseconds (from 0-999)
- **getMinutes():** Returns the minutes (from 0-59)
- **getMonth():** Returns the month (from 0-11)
- **getSeconds():** Returns the seconds (from 0-59)
- **getTime():** Returns the number of milliseconds since midnight Jan 1, 1970
- **getTimezoneOffset():** Returns the time difference between UTC time and local time, in minutes
- **getUTCDate():** Returns the day of the month, according to universal time (from 1-31)
- **getUTCDay():** Returns the day of the week, according to universal time (from 0-6)
- **getUTCFullYear():** Returns the year, according to universal time
- **getUTCHours():** Returns the hour, according to universal time (from 0-23)
- **getUTCMilliseconds():** Returns the milliseconds, according to universal time (from 0-999)
- **getUTCMinutes():** Returns the minutes, according to universal time (from 0-59)
- **getUTCMonth():** Returns the month, according to universal time (from 0-11)
- **getUTCSeconds():** Returns the seconds, according to universal time (from 0-59)
- **now():** Returns the number of milliseconds since midnight Jan 1, 1970
- **parse():** Parses a date string and returns the number of milliseconds since January 1, 1970
- **setDate():** Sets the day of the month of a date object
- **setFullYear():** Sets the year of a date object
- **setHours():** Sets the hour of a date object
- **setMilliseconds():** Sets the milliseconds of a date object
- **setMinutes():** Set the minutes of a date object
- **setMonth():** Sets the month of a date object
- **setSeconds():** Sets the seconds of a date object
- **setTime():** Sets a date to a specified number of milliseconds after/before January 1, 1970
- **setUTCDate():** Sets the day of the month of a date object, according to universal time
- **setUTCFullYear():** Sets the year of a date object, according to universal time
- **setUTCHours():** Sets the hour of a date object, according to universal time
- **setUTCMilliseconds():** Sets the milliseconds of a date object, according to universal time
- **setUTCMinutes():** Set the minutes of a date object, according to universal time
- **setUTCMonth():** Sets the month of a date object, according to universal time
- **setUTCSeconds():** Set the seconds of a date object, according to universal time
- **toDateString():** Converts the date portion of a Date object into a readable string
- **toISOString():** Returns the date as a string, using the ISO standard
- **toJSON():** Returns the date as a string, formatted as a JSON date
- **toLocaleDateString():** Returns the date portion of a Date object as a string, using locale conventions
- **toLocaleTimeString():** Returns the time portion of a Date object as a string, using locale conventions
- **toLocaleString():** Converts a Date object to a string, using locale conventions
- **toString():** Converts a Date object to a string
- **toTimeString():** Converts the time portion of a Date object to a string
- **toUTCString():** Converts a Date object to a string, according to universal time
- **UTC():** Returns the number of milliseconds in a date since midnight of January 1, 1970, according to UTC time
- **valueOf():** Returns the primitive value of a Date object

Set Date Methods
^^^^^^^^^^^^^^^^

- **setDate():** Set the day as a number (1-31)
- **setFullYear():** Set the year (optionally month and day)
- **setHours():** Set the hour (0-23)
- **setMilliseconds():** Set the milliseconds (0-999)
- **setMinutes():** Set the minutes (0-59)
- **setMonth():** Set the month (0-11)
- **setSeconds():** Set the seconds (0-59)
- **setTime():** Set the time (milliseconds since January 1, 1970)

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // Day as Number 1 - 31 
                // Hours as Number 0 - 23
                // Month as Number 0 - 11 Ex- 0 = Jan
                // Week Day as Number 0 - 6 Ex- 0 = Sun
                var tarikh = new Date();
                document.write(tarikh + "<br>");
                
                tarikh.setHours(22);
                document.write(tarikh + "<br>");
                
                tarikh.setMinutes(56);
                document.write(tarikh + "<br>");
                
                tarikh.setSeconds(40);
                document.write(tarikh + "<br>");
                
                tarikh.setDate(26);
                document.write(tarikh + "<br>");
                
                tarikh.setMonth(11);
                document.write(tarikh + "<br>");
                
                tarikh.setFullYear(2022);
                document.write(tarikh + "<br>");
                
                tarikh.setFullYear(2022, 3, 15);
                document.write(tarikh + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/date_7.png
   :width: 800

Get Date Methods
^^^^^^^^^^^^^^^^

- **getFullYear():** Get the year as a four-digit number (yyyy)
- **getMonth():** Get the month as a number (0-11)
- **getDate():** Get the day as a number (1-31)
- **getHours():** Get the hour (0-23)
- **getMinutes():** Get the minute (0-59)
- **getSeconds():** Get the second (0-59)
- **getMilliseconds():** Get the millisecond (0-999)
- **getTime():** Get the time (milliseconds since January 1, 1970)
- **getDay():** Get the weekday as a number (0-6)

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // Day as Number 1 - 31 
                // Hours as Number 0 - 23
                // Month as Number 0 - 11 Ex- 0 = Jan
                // Week Day as Number 0 - 6 Ex- 0 = Sun
                var tarikh = new Date();
                document.write(tarikh + "<br>");
                
                document.write("Hours: "+ tarikh.getHours() + "<br>");

                document.write("Minutes: " + tarikh.getMinutes() + "<br>");
                
                document.write("Second: " + tarikh.getSeconds() + "<br>");

                document.write("Date: " + tarikh.getDate() + "<br>");

                document.write("Month: " + tarikh.getMonth() + "<br>");
                
                document.write("Year: " + tarikh.getFullYear() + "<br>");

                document.write("Day: " + tarikh.getDay() + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/date_8.png
   :width: 800

Retrieve Month Name & Day Name
------------------------------

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // Day as Number 1 - 31 
                // Hours as Number 0 - 23
                // Month as Number 0 - 11 Ex- 0 = Jan
                // Week Day as Number 0 - 6 Ex- 0 = Sun
                var tarikh = new Date();
                var month = tarikh.getMonth();
                var day = tarikh.getDay();
                document.write(getMonthName(month) + "<br>");
                document.write(getDayName(day) + "<br>");
                
                function getMonthName(monthnumber){
                    var monthname = ["January","February","March","April","May","June","July","August","September","October","November","December"];
                    return monthname[monthnumber];
                }
                
                function getDayName(daynumber){
                    var dayname = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
                    return dayname[daynumber];
                }
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/date_9.png
   :width: 800

How to Format Date & Time
-------------------------

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                // Day as Number 1 - 31 
                // Hours as Number 0 - 23
                // Month as Number 0 - 11 Ex- 0 = Jan
                // Week Day as Number 0 - 6 Ex- 0 = Sun
                var tarikh = new Date();
                document.write(formatDate(tarikh) + "<br>");
                document.write(formatTime(tarikh) + "<br>");
                
                function formatDate(pd){
                    var date = pd.getDate();
                    var month = pd.getMonth();
                        month++;
                    var year = pd.getFullYear();
                    return date + " - " + month + " - " + year; 
                }

                function formatTime(pd){
                    var hour = pd.getHours();
                    var minutes = pd.getMinutes();
                        minutes++;
                    var seconds = pd.getSeconds();
                    return hour + " - " + minutes + " - " + seconds; 
                }
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/date_10.png
   :width: 800

Converting Dates to String
--------------------------

If you want to create a string in a standard format, Date provides three methods:

- toString( )
- toUTCString( )
- toGMTString( )

toUTCString ( ) & toGMTString ( ) format the string according to Internet (GMT) standards, whereas toString ( ) creates the string according to Local Time.

Ex:

.. code-block:: HTML
   :linenos:

    <!DOCTYPE html>
    <html>
        <head><title>Techno Dexterous</title>
        </head>
        <body>
            <script> 
                var tarikh = new Date();
                document.write(tarikh.toString() + "<br>");
                document.write(tarikh.toUTCString() + "<br>");
                document.write(tarikh.toGMTString() + "<br>");
            </script>
        </body>
    </html>

Output:

.. image:: D:/Courses/Javascript_images/date_11.png
   :width: 800

