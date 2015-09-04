---
title: head
tags:
  - Markup
  - Elements
  - HTML
readiness: 'In Progress'
notes:
  - 'Add Category, Parent, Children and Compatibility information. Delete HTML information sub section.'
summary: 'The head element (<head>) represents a collection of metadata for the document.'
code_samples:
  - 'http://test.w3.org/html/examples/elements/head/head01.html'
uri: html/elements/head
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/events/abort
    - dom/events/afterupdate
    - dom/events/beforecopy
    - dom/events/beforeupdate
    - dom/events/cellchange
    - dom/events/change
    - dom/events/dataavailable
    - dom/events/datasetchanged
    - dom/events/datasetcomplete
    - dom/events/error
    - dom/events/errorupdate
    - dom/events/filterchange
    - dom/events/input
    - dom/events/layoutcomplete
    - dom/events/readystatechange
    - dom/events/reset
    - dom/events/resize
    - dom/events/rowenter
    - dom/events/rowexit
    - dom/events/rowsdelete
    - dom/events/rowsinserted
    - dom/events/selectstart
    - dom/methods/appendChild
    - dom/methods/applyElement
    - dom/methods/attachEvent
    - dom/methods/clearAttributes
    - dom/methods/click
    - dom/events/click
    - dom/methods/cloneNode
    - dom/methods/componentFromPoint
    - dom/methods/detachEvent
    - dom/methods/doScroll
    - dom/methods/dragDrop
    - dom/methods/fireEvent
    - dom/methods/getAdjacentText
    - dom/methods/getAttribute
    - dom/methods/getAttributeNode
    - dom/attributes
    - dom/methods/getAttributeNodeNS
    - dom/methods/getAttributeNS
    - dom/methods/getElementsByClassName
    - dom/properties/className
    - dom/methods/getElementsByTagName
    - dom/methods/getElementsByTagNameNS
    - dom/methods/hasAttribute
    - dom/methods/hasAttributeNS
    - dom/methods/hasAttributes
    - dom/methods/hasChildNodes
    - dom/methods/insertAdjacentElement
    - dom/methods/insertAdjacentHTML
    - dom/methods/insertAdjacentText
    - dom/methods/insertBefore
    - dom/methods/mergeAttributes
    - dom/methods/matchesSelector
    - dom/methods/normalize
    - dom/methods/removeAttribute
    - dom/methods/removeAttributeNode
    - dom/methods/removeAttributeNS
    - dom/methods/removeChild
    - dom/methods/removeNode
    - dom/methods/replaceAdjacentText
    - dom/methods/replaceChild
    - dom/methods/replaceNode
    - dom/methods/setActive
    - dom/methods/setAttribute
    - dom/methods/setAttributeNode
    - dom/methods/setAttributeNodeNS
    - dom/methods/setAttributeNS
    - dom/methods/setCapture
    - dom/methods/swapNode
    - dom/properties/attributes
    - dom/properties/canHaveChildren
    - dom/properties/canHavedom/canHaveHTML
    - dom/traversal/properties/childElementCount
    - dom/properties/nodeType
    - dom/properties/constructor
    - dom/properties/firstChild
    - dom/properties/childNodes
    - dom/traversal/properties/firstElementChild
    - dom/properties/innerdom/innerHTML
    - dom/properties/innerText
    - dom/properties/isContentEditable
    - dom/properties/isDisabled
    - dom/properties/isMultiLine
    - dom/traversal/properties/isTextEdit
    - dom/traversal/TextRange
    - dom/properties/lastChild
    - dom/traversal/properties/lastElementChild
    - dom/traversal/properties/nextElementSibling
    - dom/properties/nextSibling
    - dom/properties/nodeName
    - dom/properties/nodeValue
    - dom/properties/offsetHeight
    - dom/properties/offsetParent
    - dom/properties/offsetTop
    - dom/properties/offsetLeft
    - dom/properties/offsetWidth
    - dom/properties/outerdom/outerHTML
    - dom/properties/outerText
    - dom/properties/ownerDocument
    - dom/traversal/properties/parentElement
    - dom/properties/parentNode
    - dom/traversal/properties/parentTextEdit
    - dom/traversal/properties/previousElementSibling
    - dom/properties/previousSibling
    - dom/properties/readyState
    - dom/properties/scrollHeight
    - dom/properties/scrollLeft
    - dom/properties/scrollTop
    - dom/properties/scrollWidth
    - dom/properties/sourceIndex
    - dom/properties/all
    - dom/properties/tagName
    - dom/properties/tagUrn
    - dom/properties/uniqueID
    - dom/properties/uniqueNumber

---
# head

## Summary

The head element (\<head\>) represents a collection of metadata for the document.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLHeadElement](/dom/HTMLHeadElement)

The `head` element provides information that does not affect the rendering of the document but could be of use to the application, such as: title of the document displayed in the tab of the web browser (\<title\>) and meta information useful for search engines (\<meta\>).

The following tags are valid in this element:

-   [`base`](/html/elements/base)
-   [`link`](/html/elements/link)
-   [`meta`](/html/elements/meta)
-   [`script`](/html/elements/script)
-   [`style`](/html/elements/style)
-   [`title`](/html/elements/title)

## Examples

The `<head>` element is contained by the `<html>` element and contains the `<title>` element.

``` {.html}


<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>The HTML Document</title>
</head>
<body>
<p>The HTML content</p>
</body>
</html>
```

</pre>
[View live example](http://test.w3.org/html/examples/elements/head/head01.html)

### Members

The `head` object has these types of members:

-   [Events](#Events)
-   [Methods](#Methods)
-   [Properties](#Properties)

#### Events

The `head` object has these events.

Event
:   Description
[`onabort`](/w/index.php?title=dom/events/abort&action=edit&redlink=1)
:   Fires when the user aborts the download.
[`onafterupdate`](/w/index.php?title=dom/events/afterupdate&action=edit&redlink=1)
:   Fires on a databound object after successfully updating the associated data in the data source object.
[`onbeforecopy`](/w/index.php?title=dom/events/beforecopy&action=edit&redlink=1)
:   Fires on the source object before the selection is copied to the system clipboard.
[`onbeforeupdate`](/w/index.php?title=dom/events/beforeupdate&action=edit&redlink=1)
:   Fires on a databound object before updating the associated data in the data source object.
[`oncellchange`](/w/index.php?title=dom/events/cellchange&action=edit&redlink=1)
:   Fires when data changes in the data provider.
[`onchange`](/w/index.php?title=dom/events/change&action=edit&redlink=1)
:   Fires when the contents of the object or selection have changed.
[`ondataavailable`](/w/index.php?title=dom/events/dataavailable&action=edit&redlink=1)
:   Fires periodically as data arrives from data source objects that asynchronously transmit their data.
[`ondatasetchanged`](/w/index.php?title=dom/events/datasetchanged&action=edit&redlink=1)
:   Fires when the data set exposed by a data source object changes.
[`ondatasetcomplete`](/w/index.php?title=dom/events/datasetcomplete&action=edit&redlink=1)
:   Fires to indicate that all data is available from the data source object.
[`onerror`](/w/index.php?title=dom/events/error&action=edit&redlink=1)
:   Fires when an error occurs during object loading.
[`onerrorupdate`](/w/index.php?title=dom/events/errorupdate&action=edit&redlink=1)
:   Fires on a databound object when an error occurs while updating the associated data in the data source object.
[`onfilterchange`](/w/index.php?title=dom/events/filterchange&action=edit&redlink=1)
:   Fires when a visual filter changes state or completes a transition.
[`oninput`](/w/index.php?title=dom/events/input&action=edit&redlink=1)
:   Occurs when the text content of an element is changed through the user interface.
[`onlayoutcomplete`](/w/index.php?title=dom/events/layoutcomplete&action=edit&redlink=1)
:   Fires when the print or print preview layout process finishes filling the current LayoutRect object with content from the source document.
[`onload`](/dom/events/load)
:   Fires immediately after the client loads the object.
[`onreadystatechange`](/w/index.php?title=dom/events/readystatechange&action=edit&redlink=1)
:   Fires when the state of the object has changed.
[`onreset`](/w/index.php?title=dom/events/reset&action=edit&redlink=1)
:   Fires when the user resets a form.
[`onresize`](/w/index.php?title=dom/events/resize&action=edit&redlink=1)
:   Fires when the size of the object is about to change.
[`onrowenter`](/w/index.php?title=dom/events/rowenter&action=edit&redlink=1)
:   Fires to indicate that the current row has changed in the data source and new data values are available on the object.
[`onrowexit`](/w/index.php?title=dom/events/rowexit&action=edit&redlink=1)
:   Fires just before the data source control changes the current row in the object.
[`onrowsdelete`](/w/index.php?title=dom/events/rowsdelete&action=edit&redlink=1)
:   Fires when rows are about to be deleted from the recordset.
[`onrowsinserted`](/w/index.php?title=dom/events/rowsinserted&action=edit&redlink=1)
:   Fires just after new rows are inserted in the current recordset.
[`onselect`](/w/index.php?title=dom/events/selectstart&action=edit&redlink=1)
:   Fires when the current selection changes.

Â

#### Methods

The `head` object has these methods.

Method
:   Description
`addBehavior`
:   Attaches a behavior to the element.

    This method is not supported for Metro style apps using JavaScript.

[`appendChild`](/w/index.php?title=dom/methods/appendChild&action=edit&redlink=1)
:   Appends an element as a child to the object.
[`applyElement`](/w/index.php?title=dom/methods/applyElement&action=edit&redlink=1)
:   Makes the element either a child or parent of another element.
[`attachEvent`](/w/index.php?title=dom/methods/attachEvent&action=edit&redlink=1)
:   Binds the specified function to an event, so that the function gets called whenever the event fires on the object.
[`clearAttributes`](/w/index.php?title=dom/methods/clearAttributes&action=edit&redlink=1)
:   Removes all attributes and values from the object.
[`click`](/w/index.php?title=dom/methods/click&action=edit&redlink=1)
:   Simulates a click by causing the [`onclick`](/w/index.php?title=dom/events/click&action=edit&redlink=1) event to fire.
[`cloneNode`](/w/index.php?title=dom/methods/cloneNode&action=edit&redlink=1)
:   Copies a reference to the object from the document hierarchy.
[`componentFromPoint`](/w/index.php?title=dom/methods/componentFromPoint&action=edit&redlink=1)
:   Returns the component located at the specified coordinates via certain events.
`contains`
:   Checks whether the given element is contained within the object.
[`detachEvent`](/w/index.php?title=dom/methods/detachEvent&action=edit&redlink=1)
:   Unbinds the specified function from the event, so that the function stops receiving notifications when the event fires.
[`doScroll`](/w/index.php?title=dom/methods/doScroll&action=edit&redlink=1)
:   Simulates a click on a scroll bar component.
[`dragDrop`](/w/index.php?title=dom/methods/dragDrop&action=edit&redlink=1)
:   Initiates a drag event.
[`fireEvent`](/w/index.php?title=dom/methods/fireEvent&action=edit&redlink=1)
:   Fires a specified event on the object.
[`getAdjacentText`](/w/index.php?title=dom/methods/getAdjacentText&action=edit&redlink=1)
:   Returns the adjacent text string.
[`getAttribute`](/w/index.php?title=dom/methods/getAttribute&action=edit&redlink=1)
:   Retrieves the value of the specified attribute.
[`getAttributeNode`](/w/index.php?title=dom/methods/getAttributeNode&action=edit&redlink=1)
:   Retrieves an [`attribute`](/w/index.php?title=dom/attributes&action=edit&redlink=1) objectÂ referenced by the `attribute<code>.<code>name`Â property.
[`getAttributeNodeNS`](/w/index.php?title=dom/methods/getAttributeNodeNS&action=edit&redlink=1)
:   Gets an [`attribute`](/w/index.php?title=dom/attributes&action=edit&redlink=1) object that matches the specified namespace and name.
[`getAttributeNS`](/w/index.php?title=dom/methods/getAttributeNS&action=edit&redlink=1)
:   Gets the value of the specified attribute within the specified namespace.
[`getElementsByClassName`](/w/index.php?title=dom/methods/getElementsByClassName&action=edit&redlink=1)
:   Gets a collection of objects that are based on the value of the [`CLASS`](/w/index.php?title=dom/properties/className&action=edit&redlink=1) attribute.
[`getElementsByTagName`](/w/index.php?title=dom/methods/getElementsByTagName&action=edit&redlink=1)
:   Retrieves a collection of objects based on the specified element name.
[`getElementsByTagNameNS`](/w/index.php?title=dom/methods/getElementsByTagNameNS&action=edit&redlink=1)
:   Gets a collection of objects that are based on the specified element names within a specified namespace.
[`hasAttribute`](/w/index.php?title=dom/methods/hasAttribute&action=edit&redlink=1)
:   Determines whether an attribute with the specified name exists.
[`hasAttributeNS`](/w/index.php?title=dom/methods/hasAttributeNS&action=edit&redlink=1)
:   Determines whether an attribute that has the specified namespace and name exists.
[`hasAttributes`](/w/index.php?title=dom/methods/hasAttributes&action=edit&redlink=1)
:   Determines whether one or more attributes exist for the object.
[`hasChildNodes`](/w/index.php?title=dom/methods/hasChildNodes&action=edit&redlink=1)
:   Returns a value that indicates whether the object has children.
[`insertAdjacentElement`](/w/index.php?title=dom/methods/insertAdjacentElement&action=edit&redlink=1)
:   Inserts an element at the specified location.
[`insertAdjacentHTML`](/w/index.php?title=dom/methods/insertAdjacentHTML&action=edit&redlink=1)
:   Inserts the given HTML text into the element at the location.
[`insertAdjacentText`](/w/index.php?title=dom/methods/insertAdjacentText&action=edit&redlink=1)
:   Inserts the given text into the element at the specified location.
[`insertBefore`](/w/index.php?title=dom/methods/insertBefore&action=edit&redlink=1)
:   Inserts an element into the document hierarchy as a child node of a parent object.
[`mergeAttributes`](/w/index.php?title=dom/methods/mergeAttributes&action=edit&redlink=1)
:   Copies all read/write attributes to the specified element.
[`msMatchesSelector`](/w/index.php?title=dom/methods/matchesSelector&action=edit&redlink=1)
:   Determines whether an object matches the specified selector.
[`normalize`](/w/index.php?title=dom/methods/normalize&action=edit&redlink=1)
:   Merges adjacent DOM objects to produce a normalized document object model.
[`removeAttribute`](/w/index.php?title=dom/methods/removeAttribute&action=edit&redlink=1)
:   Removes an attribute from an object.
[`removeAttributeNode`](/w/index.php?title=dom/methods/removeAttributeNode&action=edit&redlink=1)
:   Removes an [`attribute`](/w/index.php?title=dom/attributes&action=edit&redlink=1) objectÂ from the object.
[`removeAttributeNS`](/w/index.php?title=dom/methods/removeAttributeNS&action=edit&redlink=1)
:   Removes the specified attribute from the object.
`removeBehavior`
:   Detaches a behavior from the element.
[`removeChild`](/w/index.php?title=dom/methods/removeChild&action=edit&redlink=1)
:   Removes a child node from the object.
[`removeNode`](/w/index.php?title=dom/methods/removeNode&action=edit&redlink=1)
:   Removes the object from the document hierarchy.
[`replaceAdjacentText`](/w/index.php?title=dom/methods/replaceAdjacentText&action=edit&redlink=1)
:   Replaces the text adjacent to the element.
[`replaceChild`](/w/index.php?title=dom/methods/replaceChild&action=edit&redlink=1)
:   Replaces an existing child element with a new child element.
[`replaceNode`](/w/index.php?title=dom/methods/replaceNode&action=edit&redlink=1)
:   Replaces the object with another element.
[`setActive`](/w/index.php?title=dom/methods/setActive&action=edit&redlink=1)
:   Sets the object as active without setting focus to the object.
[`setAttribute`](/w/index.php?title=dom/methods/setAttribute&action=edit&redlink=1)
:   Sets the value of the specified attribute.
[`setAttributeNode`](/w/index.php?title=dom/methods/setAttributeNode&action=edit&redlink=1)
:   Sets an [`attribute`](/w/index.php?title=dom/attributes&action=edit&redlink=1) objectÂ node as part of the object.
[`setAttributeNodeNS`](/w/index.php?title=dom/methods/setAttributeNodeNS&action=edit&redlink=1)
:   Sets an [`attribute`](/w/index.php?title=dom/attributes&action=edit&redlink=1) object as part of the object.
[`setAttributeNS`](/w/index.php?title=dom/methods/setAttributeNS&action=edit&redlink=1)
:   Sets the value of the specified attribute within the specified namespace.
[`setCapture`](/w/index.php?title=dom/methods/setCapture&action=edit&redlink=1)
:   Sets the mouse capture to the object that belongs to the current document.
[`swapNode`](/w/index.php?title=dom/methods/swapNode&action=edit&redlink=1)
:   Exchanges the location of two objects in the document hierarchy.

Â

#### Properties

The `head` object has these properties.

Property
:   Description
[`attributes`](/w/index.php?title=dom/properties/attributes&action=edit&redlink=1)
:   Retrieves a collection of attributes of the object.
[`canHaveChildren`](/w/index.php?title=dom/properties/canHaveChildren&action=edit&redlink=1)
:   Gets a value indicating whether the object can contain child objects.
[`canHaveHTML`](/w/index.php?title=dom/properties/canHavedom/canHaveHTML&action=edit&redlink=1)
:   Retrieves the value indicating whether the object can contain rich HTML markup.
[`childElementCount`](/w/index.php?title=dom/traversal/properties/childElementCount&action=edit&redlink=1)
:   Retrieves the number of immediate child nodes of the current element or a zero if the element does not contain any child nodes. [`childElementCount`](/w/index.php?title=dom/traversal/properties/childElementCount&action=edit&redlink=1) does not return all child nodes, only child nodes that are [`nodeType`](/w/index.php?title=dom/properties/nodeType&action=edit&redlink=1) =1, or element nodes.
[`className`](/w/index.php?title=dom/properties/className&action=edit&redlink=1)
:   Sets or retrieves the class of the object.
[`constructor`](/w/index.php?title=dom/properties/constructor&action=edit&redlink=1)
:   Returns a reference to the constructor of an object.
[`firstChild`](/w/index.php?title=dom/properties/firstChild&action=edit&redlink=1)
:   Gets a reference to the first child in the [`childNodes`](/w/index.php?title=dom/properties/childNodes&action=edit&redlink=1) collection of the object.
[`firstElementChild`](/w/index.php?title=dom/traversal/properties/firstElementChild&action=edit&redlink=1)
:   Retrieves a reference to the first child element, or null if there are no child elements.
[`id`](/html/attributes/id)
:   Sets or retrieves the string identifying the object.
[`innerHTML`](/w/index.php?title=dom/properties/innerdom/innerHTML&action=edit&redlink=1)
:   Sets or retrieves the HTML between the start and end tags of the object.
[`innerText`](/w/index.php?title=dom/properties/innerText&action=edit&redlink=1)
:   Sets or retrieves the text between the start and end tags of the object.
[`isContentEditable`](/w/index.php?title=dom/properties/isContentEditable&action=edit&redlink=1)
:   Gets the value that indicates whether the user can edit the contents of the object.
[`isDisabled`](/w/index.php?title=dom/properties/isDisabled&action=edit&redlink=1)
:   Gets the value that indicates whether the user can interact with the object.
[`isMultiLine`](/w/index.php?title=dom/properties/isMultiLine&action=edit&redlink=1)
:   Retrieves the value indicating whether the content of the object contains one or more lines.
[`isTextEdit`](/w/index.php?title=dom/traversal/properties/isTextEdit&action=edit&redlink=1)
:   Retrieves whether a [`TextRange`](/w/index.php?title=dom/traversal/TextRange&action=edit&redlink=1) object can be created using the object.
[`lang`](/html/attributes/lang)
:   Sets or retrieves the language to use.
[`language`](/html/attributes/language)
:   Sets or retrieves the language in which the current script is written.
[`lastChild`](/w/index.php?title=dom/properties/lastChild&action=edit&redlink=1)
:   Gets a reference to the last child in the [`childNodes`](/w/index.php?title=dom/properties/childNodes&action=edit&redlink=1) collection of an object.
[`lastElementChild`](/w/index.php?title=dom/traversal/properties/lastElementChild&action=edit&redlink=1)
:   Retrieves a reference to the last child element or null if there are no child elements.
[`nextElementSibling`](/w/index.php?title=dom/traversal/properties/nextElementSibling&action=edit&redlink=1)
:   Retrieves a reference to the sibling element that immediately follows or null if the element does not have any sibling elements that follow it.
[`nextSibling`](/w/index.php?title=dom/properties/nextSibling&action=edit&redlink=1)
:   Retrieves a reference to the next child of the parent for the object.
[`nodeName`](/w/index.php?title=dom/properties/nodeName&action=edit&redlink=1)
:   Gets the name of a particular type of node.
[`nodeType`](/w/index.php?title=dom/properties/nodeType&action=edit&redlink=1)
:   Retrieves the type of the requested node.
[`nodeValue`](/w/index.php?title=dom/properties/nodeValue&action=edit&redlink=1)
:   Gets or sets the value of a node.
[`offsetHeight`](/w/index.php?title=dom/properties/offsetHeight&action=edit&redlink=1)
:   Retrieves the height of the object relative to the layout or coordinate parent, as specified by the [`offsetParent`](/w/index.php?title=dom/properties/offsetParent&action=edit&redlink=1) property.
[`offsetParent`](/w/index.php?title=dom/properties/offsetParent&action=edit&redlink=1)
:   Retrieves a reference to the container object that defines the [`offsetTop`](/w/index.php?title=dom/properties/offsetTop&action=edit&redlink=1) and [`offsetLeft`](/w/index.php?title=dom/properties/offsetLeft&action=edit&redlink=1) properties of the object.
[`offsetWidth`](/w/index.php?title=dom/properties/offsetWidth&action=edit&redlink=1)
:   Retrieves the width of the object relative to the layout or coordinate parent, as specified by the [`offsetParent`](/w/index.php?title=dom/properties/offsetParent&action=edit&redlink=1) property.
[`outerHTML`](/w/index.php?title=dom/properties/outerdom/outerHTML&action=edit&redlink=1)
:   Sets or retrieves the object and its content in HTML.
[`outerText`](/w/index.php?title=dom/properties/outerText&action=edit&redlink=1)
:   Sets or retrieves the text of the object.
[`ownerDocument`](/w/index.php?title=dom/properties/ownerDocument&action=edit&redlink=1)
:   Retrieves the [`Document`](/dom/Document) object associated with the node.
[`parentElement`](/w/index.php?title=dom/traversal/properties/parentElement&action=edit&redlink=1)
:   Retrieves the parent object in the object hierarchy.
[`parentNode`](/w/index.php?title=dom/properties/parentNode&action=edit&redlink=1)
:   Retrieves the parent object in the document hierarchy.
[`parentTextEdit`](/w/index.php?title=dom/traversal/properties/parentTextEdit&action=edit&redlink=1)
:   Retrieves the container object in the document hierarchy that can be used to create a [`TextRange`](/w/index.php?title=dom/traversal/TextRange&action=edit&redlink=1) containing the original object.
[`previousElementSibling`](/w/index.php?title=dom/traversal/properties/previousElementSibling&action=edit&redlink=1)
:   Retrieves a reference to the immediately preceding sibling element or null if the element does not have any preceding siblings.
[`previousSibling`](/w/index.php?title=dom/properties/previousSibling&action=edit&redlink=1)
:   Gets a reference to the previous child of the parent for the object.
`profile`
:   Sets or retrieves one or more URIs in which the object properties and legal values for those properties are defined.
[`readyState`](/w/index.php?title=dom/properties/readyState&action=edit&redlink=1)
:   Retrieves the current state of the object.
`recordNumber`
:   Retrieves the ordinal record from the data set that generated the object.
[`role`](/html/attributes/role)
:   Sets or retrieves the role for this element.
`scopeName`
:   Gets the namespace defined for the element.

    This property is not supported for Metro style apps using JavaScript.

[`scrollHeight`](/w/index.php?title=dom/properties/scrollHeight&action=edit&redlink=1)
:   Retrieves the scrolling height of the object.
[`scrollLeft`](/w/index.php?title=dom/properties/scrollLeft&action=edit&redlink=1)
:   Sets or retrieves the distance between the left edge of the object and the leftmost portion of the content currently visible in the window.
[`scrollTop`](/w/index.php?title=dom/properties/scrollTop&action=edit&redlink=1)
:   Sets or retrieves the distance between the top of the object and the topmost portion of the content currently visible in the window.
[`scrollWidth`](/w/index.php?title=dom/properties/scrollWidth&action=edit&redlink=1)
:   Retrieves the scrolling width of the object.
[`sourceIndex`](/w/index.php?title=dom/properties/sourceIndex&action=edit&redlink=1)
:   Retrieves the ordinal position of the object, in source order, as the object appears in the document's [`all`](/w/index.php?title=dom/properties/all&action=edit&redlink=1) collection.
[`tagName`](/w/index.php?title=dom/properties/tagName&action=edit&redlink=1)
:   Retrieves the tag name of the object.
[`tagUrn`](/w/index.php?title=dom/properties/tagUrn&action=edit&redlink=1)
:   Sets or gets the URN specified in the namespace declaration.

    This property is not supported for Metro style apps using JavaScript.

[`title`](/html/attributes/title)
:   Sets or retrieves advisory information (a ToolTip) for the object.
[`uniqueID`](/w/index.php?title=dom/properties/uniqueID&action=edit&redlink=1)
:   Retrieves an autogenerated, unique identifier for the object.
[`uniqueNumber`](/w/index.php?title=dom/properties/uniqueNumber&action=edit&redlink=1)
:   Retrieves the element's unique number.

Â

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/document-metadata.html#the-head-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/document-metadata.html#the-head-element)
:   W3C Recommendation
[HTML 4.01](http://www.w3.org/TR/html401/struct/global.html#edef-HEAD)
:   W3C Recommendation

## See also

### Related articles

#### Document Structure

-   [button](/html/elements/button)

-   [button](/html/elements/button/ja)

-   [footer](/html/elements/footer)

-   **head**

-   [main](/html/elements/main)

-   [nav](/html/elements/nav)

-   [p](/html/elements/p)

-   [section](/html/elements/section)

#### HTML

-   [user-modify](/css/properties/user-modify)

-   [HTMLAudioElement](/dom/HTMLAudioElement)

-   [textLength](/dom/HTMLTextAreaElement/textLength)

-   [value](/dom/HTMLTextAreaElement/value)

-   [accept](/html/attributes/accept)

-   [action](/html/attributes/action)

-   [alt](/html/attributes/alt)

-   [autocomplete](/html/attributes/autocomplete)

-   [autofocus](/html/attributes/autofocus)

-   [checked](/html/attributes/checked)

-   [crossorigin](/html/attributes/crossorigin)

-   [form](/html/attributes/form)

-   [formEnctype](/html/attributes/formEnctype)

-   [height](/html/attributes/height)

-   [list](/html/attributes/list)

-   [max (HTMLInputElement)](/html/attributes/max_(HTMLInputElement))

-   [maxLength](/html/attributes/maxLength)

-   [min](/html/attributes/min)

-   [multiple](/html/attributes/multiple)

-   [readonly](/html/attributes/readonly)

-   [size](/html/attributes/size)

-   [standby](/html/attributes/standby)

-   [step](/html/attributes/step)

-   [HTML Elements](/html/elements)

-   [!DOCTYPE](/html/elements/!DOCTYPE)

-   [!DOCTYPE](/html/elements/!DOCTYPE/ja)

-   [acronym](/html/elements/acronym)

-   [b](/html/elements/b)

-   [b](/html/elements/b/ja)

-   [br](/html/elements/br)

-   [br](/html/elements/br/ja)

-   [button](/html/elements/button)

-   [button](/html/elements/button/ja)

-   [caption](/html/elements/caption)

-   [cite](/html/elements/cite)

-   [code](/html/elements/code)

-   [col](/html/elements/col)

-   [colgroup](/html/elements/colgroup)

-   [datalist](/html/elements/datalist)

-   [del](/html/elements/del)

-   [dfn](/html/elements/dfn)

-   [div](/html/elements/div)

-   [em](/html/elements/em)

-   [EMBED](/html/elements/embed)

-   [fieldset](/html/elements/fieldset)

-   [font](/html/elements/font)

-   [footer](/html/elements/footer)

-   **head**

-   [hn](/html/elements/hn)

-   [hr](/html/elements/hr)

<!-- -->

    â€¦ further results

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

