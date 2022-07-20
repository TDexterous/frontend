Module 6 : HTML-Images
======================

1) Images
---------

* Images play a very important role sometimes on our website and it improves the design and the appearance of a web page.
* **<img>** tag is used to embed an image in a web page and it creates space to hold that image.
* **<img>** tag is empty and it does not have a closing tag.

* It has two required attributes :

    1) src
    2) alt

1) src - Specifies the path to the image
2) alt - Specifies an alternate text to that image



.. code-block:: html
        :linenos:

        <img src="url" alt="alternative">


Ex. :
    .. code-block:: html
        :linenos:

        <!DOCTYPE html>
        <html>
        <body>
            <img src="myPhoto.jpg" alt="myPhoto">
        </body>
        </html>

**NOTE : If a browser cannot find an image then it will display alt value.**

Image width, height or style
############################


Ex. :

    .. code-block:: html
        :linenos:

        <!DOCTYPE html>
        <html>
        <body>
            <img src="myPhoto.jpg" alt="Photo" width="500" height="600">
        </body>
        </html>


Ex. :

    .. code-block:: html
        :linenos:

        <!DOCTYPE html>
        <html>
        <head>
            <style>
                img {
                    width: 100%;
                    }
            </style>
        </head>
        <body>
            <img src="Photo.jpg" alt="Photo" width="128" height="128">
            <img src="Photo.jpg" alt="Photo" style="width:128px;height:128px;">
        </body>
        </html>

Images in another folder
########################

Ex. :

    .. code-block:: html
        :linenos:

        <!DOCTYPE html>
        <html>
        <body>
            <img src="/images/Photo.jpg" alt="Photo" style="width:128px;height:128px;">
        </body>
        </html>


2) HTML Image Maps
------------------

* It is nothing but clickable image.
* It can create clickable areas on your image.
* **<map>** tag is used for image map and **<area>** tag is used to define one or more clickable areas.

Ex. :

    .. code-block:: html
        :linenos:

        <!DOCTYPE html>
        <html>
        <body>
            <img src="work.jpg" alt="Work" usemap="#work">
            <map name="work">
                <area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.html">
                <area shape="circle" coords="337,300,44" alt="Smily" href="Smily.html">
            </map>
        </body>
        </html>


* You must add the usemap attribute to image tag. It creates relation between the <img> and <map>.