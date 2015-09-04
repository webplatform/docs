---
title: setting color in css
tags:
  - Tutorials
  - CSS
readiness: 'In Progress'
notes:
  - 'Needs screenshot, fix broken links'
summary: 'This article explains in detail the different ways you can specify color in CSS.'
uri: 'tutorials/setting color in css'
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'SVG color keywords'
    - Colors
    - 'CSS2 System Colors'

---
# Setting color in CSS

## Summary

This article explains in detail the different ways you can specify color in CSS.

## Information: Color

In this tutorial so far, you have used a limited number of named colors. CSS 2 supports 17 named colors in all. Some of the names might not be what you expect:

:   black

primaries
:   red

secondaries
:   yellow

:   maroon

### Further color keyword details

Your browser might support many more named colors, like:

<dl>
<dt>
dodgerblue

</dt>
<dd>
</dd>
</dl>
For details of this extended list, see: [SVG color keywords](/w/index.php?title=SVG_color_keywords&action=edit&redlink=1) in the CSS 3 Color Module. Beware of using color names that your reader's browsers might not support.

For a larger palette, specify the red, green and blue components of the color you want by using a number sign (hash) and three *hexadecimal* digits in the range 0 – 9, a – f. The letters a – f represent the values 10 – 15:

black
:
pure red
:
pure green
:
pure blue
:
white
:

For the full palette, specify two hexadecimal digits for each component:

black
:
pure red
:
pure green
:
pure blue
:
white
:

You can usually get these six-digit hexadecimal codes from your graphics program or some other tool.

### Further hex examples

With a little practice, you can adjust the three-digit colors manually for most purposes:

Start with pure red:
:
To make it paler, add some green and blue:
:
To make it more orange, add a little extra green:
:
To darken it, reduce all its components:
:
To reduce its saturation, make its components more equal:
:
If you make them exactly equal, you get gray:
:

For a pastel shade like pale blue:

Start with pure white:
:
Reduce the other components a little:
:

## RGB colors

You can also specify a color using decimal RGB values in the range 0 – 255, or percentages. For example, this is maroon (dark red):

    rgb(128, 0, 0)

For full details of how to specify colors, see: [Colors](/w/index.php?title=Colors&action=edit&redlink=1) in the CSS Specification. For information on matching system colors like Menu and ThreeDFace, see: [CSS2 System Colors](/w/index.php?title=CSS2_System_Colors&action=edit&redlink=1) in the CSS Specification.

### Color properties

You have already used the [color] property on text.You can also use the [background-color] property to change elements' backgrounds. Backgrounds can be set to `transparent` to explicitly remove any color, revealing the parent element's background.

``` {style="background-color: #fffff4;"}
background-color: #fffff4;
```

The **More details** boxes use this pale gray:

``` {style="background-color: #f4f4f4;"}
background-color: #f4f4f4;
```

## Action: Using color codes

1.  \<p\>Edit your CSS file; make the change shown here in bold, to give the initial letters a pale blue background. (The layout and comments in your file probably differ from the file shown here. Keep the layout and comments the way you prefer them.)\</p\>

        /*** CSS Tutorial: Color page ***/

        /* page font */
        body {font: 16px "Comic Sans MS", cursive;}

        /* paragraphs */
        p {color: blue;}
        #first {font-style: italic;}

        /* initial letters */
        strong {
          color: red;
          background-color: #ddf;
          font: 200% serif;
        }

        .carrot {color: red;}
        .spinach {color: green;}

2.  \<p\>Save the file and refresh your browser to see the result.\</li\>

    \</ol\>

    Need to add screenshot of the result?

    ## See also

    ### Other articles

    -   [color](/css/data_types/color)
    -   [Cascading Style Sheets Level 2 Revision 1 (CSS 2.1) Specification, 4 Syntax and basic data types, 4.3.6 Colors](http://www.w3.org/TR/CSS2/syndata.html#color-units)
    -   [CSS Color Module Level 3 , 4.3. Extended color keywords](http://www.w3.org/TR/css3-color/#svg-color)

    ### Exercise question

    In your CSS file, change all the color names to 3-digit color codes without affecting the result (this cannot be done exactly, but you can get close. To do it exactly you need 6-digit codes, and you need to look up the CSS Specification or use a graphics tool to match the colors.)

    ## Attribution

    *This article contains content originally from external sources, including ones licensed under the CC-BY-SA license.* [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)

    Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Color)

