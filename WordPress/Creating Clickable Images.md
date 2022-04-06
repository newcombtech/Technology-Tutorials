# HTML Image Maps

Guide by Rosalind Kidwell for use by the Newcomb Digital Research
Interns <br><br>

An image map in HTML is an image with clickable areas and is defined by
using the \<map\> tag.

Different parts of the image perform different actions (typically
opening different links). This differentiates it from an image link.

The relationship between an image and a map tag is the usemap attribute
that you'll put in the img tag, which will be the name of the map
attribute, as you can see in the code below.<br><br>

## Code example

    <img src="workplace.jpg" alt="Workplace" usemap="#workmap">

    <map name="workmap">

    <area shape="rect" coords="34,44,270,350" alt="Computer" href="comput er.htm">

    <area shape="rect" coords="290,172,333,250" alt="Phone" href="phone.h tm">

    <area shape="circle" coords="337,300,44" alt="Coffee" href="coffee.ht m">

    </map>


<br><br>
Shape attribute for each area:

 rect - defines a rectangular region <br>
 circle - defines a circular region<br>
 poly - defines a polygonal region <br>
 default - defines the entire region <br><br>

Coords:

These are the coordinates that that area will cover. This is the
trickiest part of making image maps and are defined by the pixels from
the top left corner of the image. For example, (50, 20) would be 50
pixels from the left margin and 20 from the top. Therefore,

shape=\"rect\" coords=\"290,172,333,250\"

would create a rectangle stretching from one corner at (290, 172) to the
other at (333, 250) Circles are defined by 3 coordinates, so

shape=\"circle\" coords=\"337,300,44\"

would be a circle whose center is at (337, 300) with a radius of 44. <br><br>

href:

This is just the link that will happen on clicking the area defined.<br><br>

## How to make an image map:

The first step is of course to find the image and gather the links
desired. Then, you'll want to place the image how you wish it to be
displayed on your website and resize the image accordingly. **It is
important to do this resizing BEFORE you create the image map.**
Otherwise, nothing will line up in the right areas in the image is
resized after.

Luckily, making the map is quite easy with this online tool:

 [http://www.isdntek.com/tagbot/imap.htm](http://www.isdntek.com/tagbot/imap.htm)

It will let you upload the image, then drag boxes over the desired
"hotspots" and add the link it will activate. Then when you've created
each clickable spot you want, press the Make Code button and it will
generate the custom-HTML code for you! <br><br>

## Adding to a Word Press site:

To use clickable images, you'll need a site that lets you use custom
HTML elements. Simply create a new block, paste the code from the tool
above, and it will be ready to use! <br><br>

## Further resources:

[https://www.w3schools.com/html/html_images_imagemap.asp](https://www.w3schools.com/html/html_images_imagemap.asp)
