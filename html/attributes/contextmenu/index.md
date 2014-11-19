{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Used to associate the [[html/elements/menu|menu element]] in the DOM to the given element as its context menu.}}
{{Markup_Attribute
|Applies_to=html/elements/menu
|Property_applies_to=
|Content=The contextmenu attribute allows a developer to modify the menu shown upon interacting with an element. Its value must be set to be the ID of a [[html/elements/menu|menu]] element contained within the DOM which has a type of context.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=
|Code=<!doctype html>
<title>Demo for contextmenu attribute</title>
&lt;!-- Setting the context menu for the image to be imageMenu. -->
<img src="http://www.webplatform.org/logo/logo-with-text.png" alt="WPD" width="500" height="500" contextmenu="imageMenu">

&lt;!-- Declare the menu with a type of context and the proper ID that was set in the images attribute -->
<menu id="imageMenu" type="context">
    &lt;!-- Since we are going to have multiple related options, let's set a menu item
            with a label to create a submenu -->
    <menu label="resize">
        &lt;!-- Create the menu items -->
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
|LiveURL=http://code.webplatform.org/gist/11067829
}}
}}
{{Notes_Section
|Usage=This feature may only work in Firefox currently. (Untested in IE and Safari.)
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html-markup/global-attributes.html#common.attrs.contextmenu
|Status=Candidate Recommendation
|Relevant_changes=Initial specification of the attribute
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|HTML, JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}