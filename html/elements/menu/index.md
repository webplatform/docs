---
title: 'menu'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/7284273'
compatibility:
  feature: menu
  topic: html
notes:
  - 'Add notes, compatibility.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLMenuElement](/dom/HTMLMenuElement)'
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'The menu element represents information as a list of items or commands.'
tags:
  - Markup
  - Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'html/event attributes'
uri: html/elements/menu

---
## Summary

The menu element represents information as a list of items or commands.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLMenuElement](/dom/HTMLMenuElement)

The menu element is used to define a list as a menu of commands. It can have event and global attributes in addition to two of its own.

The **menu** element has partial support in Firefox only for the context form.

### Attributes

-   *label* - Text for the label to display for the menu item.
-   *type* - How the menu should be displayed to the user. Possible values are:
    -   *context* - Display a series of entries triggered by another element. Like a dropdown for example.
    -   *list* - Default. The name could change to *toolbar* in HTML 5.1. Displays menu items that are always within view.

The **menu** element also accepts [global attributes](/html/global_attributes) and [event attributes](/w/index.php?title=html/event_attributes&action=edit&redlink=1).

## Examples

This is an example of the **menu** element using the *type* and *label* attributes as well as the **button** element.

``` html
<menu type="toolbar">
<li>
<menu label="File">
<button type="button" onclick="file_new()">New...</button>
<button type="button" onclick="file_open()">Open...</button>
<button type="button" onclick="file_save()">Save</button>
</menu>
</li>
<li>
<menu label="Edit">
<button type="button" onclick="edit_cut()">Cut</button>
<button type="button" onclick="edit_copy()">Copy</button>
<button type="button" onclick="edit_paste()">Paste</button>
</menu>
</li>
</menu>
```

[View live example](http://code.webplatform.org/gist/7284273)

## Usage

     The menu and ul both represent an unordered list of items. They differ in the way that the ul element only contains items to display while the menu element contains interactive items, to act on.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/interactive-elements.html#the-menu-element)
:   W3C Working Draft

## See also

### Other articles

-   [`dir`](/html/elements/dir)
-   [`ul`](/html/elements/ul)
-   [`ol`](/html/elements/ol)
-   [`li`](/html/elements/li)
-   [`dl`](/html/elements/dl)
-   [`dt`](/html/elements/dt)
-   [`dd`](/html/elements/dd)
