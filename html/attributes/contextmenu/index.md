---
title: contextmenu
code_samples:
  - 'http://gist.github.com/11067829'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Used to associate the menu element in the DOM to the given element as its context menu.'
tags:
  - Markup
  - Attributes
  - HTML
  - JavaScript
uri: html/attributes/contextmenu

---
## <span>Summary</span>

Used to associate the menu element in the DOM to the given element as its context menu.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
html/elements/menu

</td>
</tr>
</table>
The contextmenu attribute allows a developer to modify the menu shown upon interacting with an element. Its value must be set to be the ID of a **menu** element contained within the DOM which has a type of context.

## <span>Examples</span>

``` html
<!doctype html>
<title>Demo for contextmenu attribute</title>
<!-- Setting the context menu for the image to be imageMenu. -->
<img src="http://www.webplatform.org/logo/logo-with-text.png" alt="WPD" width="500" height="500" contextmenu="imageMenu">

<!-- Declare the menu with a type of context and the proper ID that was set in the images attribute -->
<menu id="imageMenu" type="context">
    <!-- Since we are going to have multiple related options, let's set a menu item
            with a label to create a submenu -->
    <menu label="resize">
        <!-- Create the menu items -->
        <menuitem label="Increase" id="increaseImageSize">
        <menuitem label="Decrease" id="decreaseImageSize">
    </menu>
</menu>

<script>
// Lets create all the variables we will need right away.
// Get the menu items, the image, and then create some placeholders for functions.
var increaseItem = document.getElementById('increaseImageSize'),
    decreaseItem = document.getElementById('decreaseImageSize'),
    image = document.querySelector('[contextmenu="imageMenu"]'),
    increaseSize,
    decreaseSize;

    //Now let's define what happens when the items are clicked.
    //In this example, all we are doing is manipulating the height
    //and width attributes.
    increaseSize = function () {
        image.width = image.width + 100;
        image.height = image.height + 100;
    };
    decreaseSize = function () {
        image.width = image.width - 100;
        image.height = image.height - 100;
    };

    // Finally, let's listen for a click of the menu items
    // and then fire the appropriate function when a click occurs.
    increaseItem.addEventListener("click", increaseSize);
    decreaseItem.addEventListener("click", decreaseSize);
</script>
```

[View live example](http://code.webplatform.org/gist/11067829)

## <span>Usage</span>

     This feature may only work in Firefox currently. (Untested in IE and Safari.)

## <span>Related specifications</span>

[HTML5](http://www.w3.org/TR/html-markup/global-attributes.html#common.attrs.contextmenu)
:   Candidate Recommendation
