{{Page_Title|The <body> element}}
{{Flags
|High-level issues=Data Not Semantic, Unreviewed Import
|Content=Cleanup
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''body''' element (&lt;body&gt;) represents the main content of the document.}}
{{Markup_Element
|DOM_interface=dom/HTMLBodyElement
|Content==== HTML information ===

{{{!}} class="wikitable"
{{!}}-
!Closing Tag
{{!}}not required
{{!}}-
!CSS Display
{{!}}block
{{!}}}

You can access the <code><body></code> element from script through the document object.

The window object for the <code><body></code> element can host event handlers for the <code>onblur</code>, <code>onfocus</code>, <code>onload</code>, or <code>onunload</code> events.


=== HTML Event Handler Content Attributes ===

{{{!}} class="wikitable"
{{!}}-
!Event
!Description
{{!}}-
{{!}}<code>onafterprint</code> 
{{!}}User printed current document.
{{!}}-
{{!}}<code>onbeforeprint</code> 
{{!}}User requested printing of current document.
{{!}}-
{{!}}<code>onbeforeunload</code> 
{{!}}Document is about to be unloaded.
{{!}}-
{{!}}<code>onblur</code> 
{{!}}Document lost focus.
{{!}}-
{{!}}<code>onerror</code> 
{{!}}Document failed to load properly.
{{!}}-
{{!}}<code>onfocus</code> 
{{!}}Document received focus.
{{!}}-
{{!}}<code>onhashchange</code> 
{{!}}Fragment identifier part of the document’s current address changed.
{{!}}-
{{!}}<code>onload</code> 
{{!}}Document finished loading.
{{!}}-
{{!}}<code>onmessage</code> 
{{!}}Document received a message.
{{!}}-
{{!}}<code>onoffline</code> 
{{!}}Network connections failed.
{{!}}-
{{!}}<code>ononline</code> 
{{!}}Network connections returned.
{{!}}-
{{!}}<code>onpopstate</code> 
{{!}}User navigated session history.
{{!}}-
{{!}}<code>onredo</code> 
{{!}}User went forward in undo transaction history.
{{!}}-
{{!}}<code>onresize</code> 
{{!}}Document view was resized.
{{!}}-
{{!}}<code>onstorage</code> 
{{!}}Storage area changed.
{{!}}-
{{!}}<code>onundo</code> 
{{!}}User went backward in undo transaction history.
{{!}}-
{{!}}<code>onunload</code> 
{{!}}Document is going away.
{{!}}}

The following attributes are obsolete, and must not be used by authors: <code>alink</code>, <code>bgcolor</code>, <code>link</code>, <code>marginbottom</code>, <code>marginheight</code>, <code>marginleft</code>, <code>marginright</code>, <code>margintop</code>, <code>marginwidth</code>, <code>text</code>, <code>vlink</code>.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The <code><body></code> element follows the <code><head></code> element and is contained by the <code><html></code> element.
|Code=<syntaxhighlight lang="html5">
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
</syntaxhighlight>
|LiveURL=http://test.w3.org/html/examples/elements/body/body01.html
}}{{Single Example
|Language=JavaScript
|Description=This example exposes the <code><body></code> element in javascript.
|Code=<syntaxhighlight lang="javascript">var oBody = document.body;</syntaxhighlight>
}}
}}
{{Notes_Section
|Import_Notes====Members===
The <code><body></code> object has these types of members:
*[[#Events|Events]]
*[[#Methods|Methods]]
*[[#Properties|Properties]]


====Events====
The <code><body></code> object has these events.
{{{!}} class="wikitable"
{{!}}-
!Event
!Description
{{!}}-
{{!}}[[dom/events/abort|<code>onabort</code>]]
{{!}}Fires when the user aborts the download.
{{!}}-
{{!}}[[dom/events/activate|<code>onactivate</code>]]
{{!}}Fires when the object is set as the [[dom/properties/activeElement|<code>active element</code>]].
{{!}}-
{{!}}[[dom/events/afterprint|<code>onafterprint</code>]]
{{!}}Fires on the object immediately after its associated document prints or previews for printing.
{{!}}-
{{!}}[[dom/events/afterupdate|<code>onafterupdate</code>]]
{{!}}Fires on a databound object after successfully updating the associated data in the data source object.
{{!}}-
{{!}}[[dom/events/beforeactivate|<code>onbeforeactivate</code>]]
{{!}}Fires immediately before the object is set as the [[dom/properties/activeElement|<code>active element</code>]].
{{!}}-
{{!}}[[dom/events/beforecopy|<code>onbeforecopy</code>]]
{{!}}Fires on the source object before the selection is copied to the system clipboard.
{{!}}-
{{!}}[[dom/events/beforecut|<code>onbeforecut</code>]]
{{!}}Fires on the source object before the selection is deleted from the document.
{{!}}-
{{!}}[[dom/events/beforedeactivate|<code>onbeforedeactivate</code>]]
{{!}}Fires immediately before the [[dom/properties/activeElement|<code>activeElement</code>]] is changed from the current object to another object in the parent document.
{{!}}-
{{!}}[[dom/events/beforeeditfocus|<code>onbeforeeditfocus</code>]]
{{!}}Fires before an object contained in an editable element enters a ''UI Activation'' state or when an editable container object is ''control selection''.
{{!}}-
{{!}}[[dom/events/beforepaste|<code>onbeforepaste</code>]]
{{!}}Fires on the target object before the selection is pasted from the system clipboard to the document.
{{!}}-
{{!}}[[dom/events/beforeprint|<code>onbeforeprint</code>]]
{{!}}Fires on the object before its associated document prints or previews for printing.
{{!}}-
{{!}}[[dom/events/beforeunload|<code>onbeforeunload</code>]]
{{!}}Fires prior to a document being unloaded.
{{!}}-
{{!}}[[dom/events/beforeupdate|<code>onbeforeupdate</code>]]
{{!}}Fires on a databound object before updating the associated data in the data source object.
{{!}}-
{{!}}[[dom/events/cellchange|<code>oncellchange</code>]]
{{!}}Fires when data changes in the data provider.
{{!}}-
{{!}}[[dom/events/change|<code>onchange</code>]]
{{!}}Fires when the contents of the object or selection have changed.
{{!}}-
{{!}}[[dom/events/click|<code>onclick</code>]]
{{!}}Fires when the user clicks the left mouse button on the object.
{{!}}-
{{!}}[[dom/events/contextmenu|<code>oncontextmenu</code>]]
{{!}}Fires when the user clicks the right mouse button in the client area, opening the context menu.
{{!}}-
{{!}}[[dom/events/controlselect|<code>oncontrolselect</code>]]
{{!}}Fires when the user is about to make a ''control selection'' of the object.
{{!}}-
{{!}}[[dom/events/cut|<code>oncut</code>]]
{{!}}Fires on the source element when the object or selection is removed from the document and added to the system clipboard.
{{!}}-
{{!}}[[dom/events/dataavailable|<code>ondataavailable</code>]]
{{!}}Fires periodically as data arrives from data source objects that asynchronously transmit their data.
{{!}}-
{{!}}[[dom/events/datasetchanged|<code>ondatasetchanged</code>]]
{{!}}Fires when the data set exposed by a data source object changes.
{{!}}-
{{!}}[[dom/events/datasetcomplete|<code>ondatasetcomplete</code>]]
{{!}}Fires to indicate that all data is available from the data source object.
{{!}}-
{{!}}[[dom/events/dblclick|<code>ondblclick</code>]]
{{!}}Fires when the user double-clicks the object.
{{!}}-
{{!}}[[dom/events/deactivate|<code>ondeactivate</code>]]
{{!}}Fires when the [[dom/properties/activeElement|<code>activeElement</code>]] is changed from the current object to another object in the parent document.
{{!}}-
{{!}}[[dom/events/drag|<code>ondrag</code>]]
{{!}}Fires on the source object continuously during a drag operation.
{{!}}-
{{!}}[[dom/events/dragend|<code>ondragend</code>]]
{{!}}Fires on the source object when the user releases the mouse at the close of a drag operation.
{{!}}-
{{!}}[[dom/events/dragenter|<code>ondragenter</code>]]
{{!}}Fires on the target element when the user drags the object to a valid drop target.
{{!}}-
{{!}}[[dom/events/dragleave|<code>ondragleave</code>]]
{{!}}Fires on the target object when the user moves the mouse out of a valid drop target during a drag operation.
{{!}}-
{{!}}[[dom/events/dragover|<code>ondragover</code>]]
{{!}}Fires on the target element continuously while the user drags the object over a valid drop target.
{{!}}-
{{!}}[[dom/events/dragstart|<code>ondragstart</code>]]
{{!}}Fires on the source object when the user starts to drag a text selection or selected object.
{{!}}-
{{!}}[[dom/events/drop|<code>ondrop</code>]]
{{!}}Fires on the target object when the mouse button is released during a drag-and-drop operation.
{{!}}-
{{!}}[[dom/events/error|<code>onerror</code>]]
{{!}}Fires when an error occurs during object loading.
{{!}}-
{{!}}[[dom/events/errorupdate|<code>onerrorupdate</code>]]
{{!}}Fires on a databound object when an error occurs while updating the associated data in the data source object.
{{!}}-
{{!}}[[dom/events/filterchange|<code>onfilterchange</code>]]
{{!}}Fires when a visual filter changes state or completes a transition.
{{!}}-
{{!}}[[dom/events/focusin|<code>onfocusin</code>]]
{{!}}Fires for an element just prior to setting focus on that element.
{{!}}-
{{!}}[[dom/events/focusout|<code>onfocusout</code>]]
{{!}}Fires for the current element with focus immediately after moving focus to another element.
{{!}}-
{{!}}[[dom/events/hashchange|<code>onhashchange</code>]]
{{!}}Raised when there are changes to the portion of a
URL that follows the number sign (#).


This event is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/events/input|<code>oninput</code>]]
{{!}}Occurs when the text content of an element is changed through the user interface.
{{!}}-
{{!}}[[dom/events/keydown|<code>onkeydown</code>]]
{{!}}Fires when the user presses a key.
{{!}}-
{{!}}[[dom/events/keypress|<code>onkeypress</code>]]
{{!}}Fires when the user presses an alphanumeric key.
{{!}}-
{{!}}[[dom/events/keyup|<code>onkeyup</code>]]
{{!}}Fires when the user releases a key.
{{!}}-
{{!}}[[dom/events/layoutcomplete|<code>onlayoutcomplete</code>]]
{{!}}Fires when the print or print preview layout process finishes filling the current LayoutRect object with content from the source document.
{{!}}-
{{!}}[[dom/events/load|<code>onload</code>]]
{{!}}Fires immediately after the client loads the object.
{{!}}-
{{!}}[[dom/events/losecapture|<code>onlosecapture</code>]]
{{!}}Fires when the object loses the mouse capture.
{{!}}-
{{!}}[[dom/events/mousedown|<code>onmousedown</code>]]
{{!}}Fires when the user clicks the object with either mouse button.
{{!}}-
{{!}}[[dom/events/mouseenter|<code>onmouseenter</code>]]
{{!}}Fires when the user moves the mouse pointer into the object.
{{!}}-
{{!}}[[dom/events/mouseleave|<code>onmouseleave</code>]]
{{!}}Fires when the user moves the mouse pointer outside the boundaries of the object.
{{!}}-
{{!}}[[dom/events/mousemove|<code>onmousemove</code>]]
{{!}}Fires when the user moves the mouse over the object.
{{!}}-
{{!}}[[dom/events/mouseout|<code>onmouseout</code>]]
{{!}}Fires when the user moves the mouse pointer outside the boundaries of the object.
{{!}}-
{{!}}[[dom/events/mouseover|<code>onmouseover</code>]]
{{!}}Fires when the user moves the mouse pointer into the object.
{{!}}-
{{!}}[[dom/events/mouseup|<code>onmouseup</code>]]
{{!}}Fires when the user releases a mouse button while the mouse is over the object.
{{!}}-
{{!}}[[dom/events/mousewheel|<code>onmousewheel</code>]]
{{!}}Fires when the wheel button is rotated.
{{!}}-
{{!}}[[dom/events/move|<code>onmove</code>]]
{{!}}Fires when the object moves.
{{!}}-
{{!}}[[dom/events/moveend|<code>onmoveend</code>]]
{{!}}Fires when the object stops moving.
{{!}}-
{{!}}[[dom/events/movestart|<code>onmovestart</code>]]
{{!}}Fires when the object starts to move.
{{!}}-
{{!}}[[dom/events/offline|<code>onoffline</code>]]
{{!}}Raised when Internet Explorer is working offline.

This event is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/events/online|<code>ononline</code>]]
{{!}}Raised when Internet Explorer is working online.

This event is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/events/paste|<code>onpaste</code>]]
{{!}}Fires on the target object when the user pastes data, transferring the data from the system clipboard to the document.
{{!}}-
{{!}}[[dom/events/propertychange|<code>onpropertychange</code>]]
{{!}}Fires when a property changes on the object.
{{!}}-
{{!}}[[dom/events/readystatechange|<code>onreadystatechange</code>]]
{{!}}Fires when the state of the object has changed.
{{!}}-
{{!}}[[dom/events/reset|<code>onreset</code>]]
{{!}}Fires when the user resets a form.
{{!}}-
{{!}}[[dom/events/resize|<code>onresize</code>]]
{{!}}Fires when the size of the object is about to change.
{{!}}-
{{!}}[[dom/events/resizeend|<code>onresizeend</code>]]
{{!}}Fires when the user finishes changing the dimensions of the object in a ''control selection''.
{{!}}-
{{!}}[[dom/events/resizestart|<code>onresizestart</code>]]
{{!}}Fires when the user begins to change the dimensions of the object in a ''control selection''.
{{!}}-
{{!}}[[dom/events/rowenter|<code>onrowenter</code>]]
{{!}}Fires to indicate that the current row has changed in the data source and new data values are available on the object.
{{!}}-
{{!}}[[dom/events/rowexit|<code>onrowexit</code>]]
{{!}}Fires just before the data source control changes the current row in the object.
{{!}}-
{{!}}[[dom/events/rowsdelete|<code>onrowsdelete</code>]]
{{!}}Fires when rows are about to be deleted from the recordset.
{{!}}-
{{!}}[[dom/events/rowsinserted|<code>onrowsinserted</code>]]
{{!}}Fires just after new rows are inserted in the current recordset.
{{!}}-
{{!}}[[dom/events/scroll|<code>onscroll</code>]]
{{!}}Fires when the user repositions the scroll box in the scroll bar on the object.
{{!}}-
{{!}}[[dom/events/selectstart|<code>onselect</code>]]
{{!}}Fires when the current selection changes.
{{!}}-
{{!}}[[dom/events/select|<code>onselectstart</code>]]
{{!}}Fires when the object is being selected.
{{!}}-
{{!}}[[dom/events/unload|<code>onunload</code>]]
{{!}}Fires immediately before the object is unloaded.
{{!}}}
 

====Methods====
The  <code><body></code> object has these methods.
{{{!}} class="wikitable"
{{!}}-
!Method
!Description
{{!}}-
{{!}}<code>addBehavior</code>
{{!}}Attaches a behavior to the element.

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/methods/appendChild|<code>appendChild</code>]]
{{!}}Appends an element as a child to the object.
{{!}}-
{{!}}[[dom/methods/applyElement|<code>applyElement</code>]]
{{!}}Makes the element either a child or parent of another element.
{{!}}-
{{!}}[[dom/methods/attachEvent|<code>attachEvent</code>]]
{{!}}Binds the specified function to an event, so that the function gets called whenever the event fires on the object.
{{!}}-
{{!}}[[dom/methods/blur|<code>blur</code>]]
{{!}}Causes the element to lose focus and fires the [[dom/events/blur|<code>onblur</code>]] event.
{{!}}-
{{!}}[[dom/methods/clearAttributes|<code>clearAttributes</code>]]
{{!}}Removes all attributes and values from the object.
{{!}}-
{{!}}[[dom/methods/click|<code>click</code>]]
{{!}}Simulates a click by causing the [[dom/events/click|<code>onclick</code>]] event to fire.
{{!}}-
{{!}}[[dom/methods/cloneNode|<code>cloneNode</code>]]
{{!}}Copies a reference to the object from the document hierarchy.
{{!}}-
{{!}}[[dom/methods/componentFromPoint|<code>componentFromPoint</code>]]
{{!}}Returns the component located at the specified coordinates via certain events.
{{!}}-
{{!}}<code>contains</code>
{{!}}Checks whether the given element is contained within the object.
{{!}}-
{{!}}[[dom/traversal/methods/createControlRange|<code>createControlRange</code>]]
{{!}}Creates a [[dom/properties/controlRange|<code>controlRange</code>]] collection of nontext elements.
{{!}}-
{{!}}[[dom/traversal/methods/createTextRange|<code>createTextRange</code>]]
{{!}}Creates a [[dom/traversal/TextRange|<code>TextRange</code>]] object for the element.
{{!}}-
{{!}}[[dom/methods/detachEvent|<code>detachEvent</code>]]
{{!}}Unbinds the specified function from the event, so that the function stops receiving notifications when the event fires.
{{!}}-
{{!}}[[dom/methods/doScroll|<code>doScroll</code>]]
{{!}}Simulates a click on a scroll bar component.
{{!}}-
{{!}}[[dom/methods/dragDrop|<code>dragDrop</code>]]
{{!}}Initiates a drag event.
{{!}}-
{{!}}[[dom/methods/fireEvent|<code>fireEvent</code>]]
{{!}}Fires a specified event on the object.
{{!}}-
{{!}}[[dom/methods/focus|<code>focus</code>]]
{{!}}Causes the element to receive the focus and executes the code specified by the [[dom/events/focus|<code>onfocus</code>]] event.
{{!}}-
{{!}}[[dom/methods/getAdjacentText|<code>getAdjacentText</code>]]
{{!}}Returns the adjacent text string.
{{!}}-
{{!}}[[dom/methods/getAttribute|<code>getAttribute</code>]]
{{!}}Retrieves the value of the specified attribute.
{{!}}-
{{!}}[[dom/methods/getAttributeNode|<code>getAttributeNode</code>]]
{{!}}Retrieves an [[dom/attributes|<code>attribute</code>]] object referenced by the <code>attribute</code>.[[html/attributes/name|<code>name</code>]] property.
{{!}}-
{{!}}[[dom/methods/getAttributeNodeNS|<code>getAttributeNodeNS</code>]]
{{!}}Gets an [[dom/attributes|<code>attribute</code>]] object that matches the specified namespace and name.
{{!}}-
{{!}}[[dom/methods/getAttributeNS|<code>getAttributeNS</code>]]
{{!}}Gets the value of the specified attribute within the specified namespace.
{{!}}-
{{!}}[[dom/methods/getBoundingClientRect|<code>getBoundingClientRect</code>]]
{{!}}Retrieves an object that specifies the bounds of a collection of [[dom/TextRectangle|<code>TextRectangle</code>]] objects.
{{!}}-
{{!}}[[dom/methods/getClientRects|<code>getClientRects</code>]]
{{!}}Retrieves a collection of rectangles that describes the layout of the contents of an object or range within the client. Each rectangle describes a single line.
{{!}}-
{{!}}[[dom/methods/getElementsByClassName|<code>getElementsByClassName</code>]]
{{!}}Gets a collection of objects that are based on the value of the [[dom/properties/className|<code>CLASS</code>]] attribute.
{{!}}-
{{!}}[[dom/methods/getElementsByTagName|<code>getElementsByTagName</code>]]
{{!}}Retrieves a collection of objects based on the specified element name.
{{!}}-
{{!}}[[dom/methods/getElementsByTagNameNS|<code>getElementsByTagNameNS</code>]]
{{!}}Gets a collection of objects that are based on the specified element names within a specified namespace.
{{!}}-
{{!}}[[dom/methods/hasAttribute|<code>hasAttribute</code>]]
{{!}}Determines whether an attribute with the specified name exists.
{{!}}-
{{!}}[[dom/methods/hasAttributeNS|<code>hasAttributeNS</code>]]
{{!}}Determines whether an attribute that has the specified namespace and name exists.
{{!}}-
{{!}}[[dom/methods/hasAttributes|<code>hasAttributes</code>]]
{{!}}Determines whether one or more attributes exist for the object.
{{!}}-
{{!}}[[dom/methods/hasChildNodes|<code>hasChildNodes</code>]]
{{!}}Returns a value that indicates whether the object has children.
{{!}}-
{{!}}[[dom/methods/insertAdjacentElement|<code>insertAdjacentElement</code>]]
{{!}}Inserts an element at the specified location.
{{!}}-
{{!}}[[dom/methods/insertAdjacentHTML|<code>insertAdjacentHTML</code>]]
{{!}}Inserts the given HTML text into the element at the location.
{{!}}-
{{!}}[[dom/methods/insertAdjacentText|<code>insertAdjacentText</code>]]
{{!}}Inserts the given text into the element at the specified location.
{{!}}-
{{!}}[[dom/methods/insertBefore|<code>insertBefore</code>]]
{{!}}Inserts an element into the document hierarchy as a child node of a parent object.
{{!}}-
{{!}}[[dom/methods/mergeAttributes|<code>mergeAttributes</code>]]
{{!}}Copies all read/write attributes to the specified element.
{{!}}-
{{!}}[[dom/methods/matchesSelector|<code>msMatchesSelector</code>]]
{{!}}Determines whether an object matches the specified selector.
{{!}}-
{{!}}[[dom/methods/normalize|<code>normalize</code>]]
{{!}}Merges adjacent DOM objects to produce a normalized document object model.
{{!}}-
{{!}}[[css/selectors api/querySelector|<code>querySelector</code>]]
{{!}}Retrieves the first DOM
element node from descendants of the starting element node
that match any selector within the supplied selector string.
{{!}}-
{{!}}[[css/selectors api/querySelectorAll|<code>querySelectorAll</code>]]
{{!}}Retrieves all DOM
element nodes from descendants of the starting element node
that match any selector within the supplied selector strings.
{{!}}-
{{!}}[[dom/methods/releaseCapture|<code>releaseCapture</code>]]
{{!}}Removes mouse capture from the object in the current document.
{{!}}-
{{!}}[[dom/methods/removeAttribute|<code>removeAttribute</code>]]
{{!}}Removes an attribute from an object.
{{!}}-
{{!}}[[dom/methods/removeAttributeNode|<code>removeAttributeNode</code>]]
{{!}}Removes an [[dom/attributes|<code>attribute</code>]] object from the object.
{{!}}-
{{!}}[[dom/methods/removeAttributeNS|<code>removeAttributeNS</code>]]
{{!}}Removes the specified attribute from the object.
{{!}}-
{{!}}<code>removeBehavior</code>
{{!}}Detaches a behavior from the element.
{{!}}-
{{!}}[[dom/methods/removeChild|<code>removeChild</code>]]
{{!}}Removes a child node from the object.
{{!}}-
{{!}}[[dom/methods/removeNode|<code>removeNode</code>]]
{{!}}Removes the object from the document hierarchy.
{{!}}-
{{!}}[[dom/methods/replaceAdjacentText|<code>replaceAdjacentText</code>]]
{{!}}Replaces the text adjacent to the element.
{{!}}-
{{!}}[[dom/methods/replaceChild|<code>replaceChild</code>]]
{{!}}Replaces an existing child element with a new child element.
{{!}}-
{{!}}[[dom/methods/replaceNode|<code>replaceNode</code>]]
{{!}}Replaces the object with another element.
{{!}}-
{{!}}[[dom/methods/setActive|<code>setActive</code>]]
{{!}}Sets the object as active without setting focus to the object.
{{!}}-
{{!}}[[dom/methods/setAttribute|<code>setAttribute</code>]]
{{!}}Sets the value of the specified attribute.
{{!}}-
{{!}}[[dom/methods/setAttributeNode|<code>setAttributeNode</code>]]
{{!}}Sets an [[dom/attributes|<code>attribute</code>]] object node as part of the object.
{{!}}-
{{!}}[[dom/methods/setAttributeNodeNS|<code>setAttributeNodeNS</code>]]
{{!}}Sets an [[dom/attributes|<code>attribute</code>]] object as part of the object.
{{!}}-
{{!}}[[dom/methods/setAttributeNS|<code>setAttributeNS</code>]]
{{!}}Sets the value of the specified attribute within the specified namespace.
{{!}}-
{{!}}[[dom/methods/setCapture|<code>setCapture</code>]]
{{!}}Sets the mouse capture to the object that belongs to the current document.
{{!}}-
{{!}}[[dom/methods/swapNode|<code>swapNode</code>]]
{{!}}Exchanges the location of two objects in the document hierarchy.
{{!}}}
 

====Properties====
The <code><body></code> object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}[[html/attributes/accessKey|<code>accessKey</code>]]
{{!}}Sets or retrieves the access key for the object.
{{!}}-
{{!}}[[html/attributes/alinkColor|<code>aLink</code>]]
{{!}}Sets or gets the color of all active links in the element.
{{!}}-
{{!}}[[html/attributes/ATOMICSELECTION html_attribute|<code>ATOMICSELECTION</code>]]
{{!}}Specifies whether the element and its contents must be selected as a whole, indivisible unit.
{{!}}-
{{!}}[[dom/properties/attributes|<code>attributes</code>]]
{{!}}Retrieves a collection of attributes of the object.
{{!}}-
{{!}}[[html/attributes/background (Body element)|<code>background</code>]]
{{!}}Sets or retrieves the background picture tiled behind the text and graphics on the page.
{{!}}-
{{!}}[[html/attributes/bgColor|<code>bgColor</code>]]
{{!}}Deprecated. Sets or retrieves the background color behind the object.
{{!}}-
{{!}}[[html/attributes/bgProperties|<code>bgProperties</code>]]
{{!}}Sets or gets the properties of the background picture.
{{!}}-
{{!}}[[css/cssom/styleSheet/blockDirection|<code>blockDirection</code>]]
{{!}}Gets a string value that indicates whether the content in the block element flows from left to right, or from right to left.
{{!}}-
{{!}}[[dom/properties/body|<code>body</code>]]
{{!}}Gets an interface pointer to the document <code>body</code> object.
{{!}}-
{{!}}[[html/attributes/bottomMargin|<code>bottomMargin</code>]]
{{!}}Sets or gets the bottom margin of the entire body of the document.
{{!}}-
{{!}}[[dom/properties/canHaveChildren|<code>canHaveChildren</code>]]
{{!}}Gets a value indicating whether the object can contain child objects.
{{!}}-
{{!}}[[dom/properties/canHavedom/canHaveHTML|<code>canHaveHTML</code>]]
{{!}}Retrieves the value indicating whether the object can contain rich HTML markup.
{{!}}-
{{!}}[[dom/traversal/properties/childElementCount|<code>childElementCount</code>]]
{{!}}Retrieves the number of immediate child nodes of the current element or a zero if the element does not contain any child nodes. [[dom/traversal/properties/childElementCount|<code>childElementCount</code>]] does not return all child nodes, only child nodes that are [[dom/properties/nodeType|<code>nodeType</code>]] {{=}}1, or element nodes.
{{!}}-
{{!}}[[dom/properties/className|<code>className</code>]]
{{!}}Sets or retrieves the class of the object.
{{!}}-
{{!}}[[dom/properties/clientHeight|<code>clientHeight</code>]]
{{!}}Retrieves the height of the object including padding, but not including margin, border, or scroll bar.
{{!}}-
{{!}}[[dom/properties/clientLeft|<code>clientLeft</code>]]
{{!}}Retrieves the distance between the [[dom/properties/offsetLeft|<code>offsetLeft</code>]] property and the true left side of the client area.
{{!}}-
{{!}}[[dom/properties/clientTop|<code>clientTop</code>]]
{{!}}Retrieves the distance between the [[dom/properties/offsetTop|<code>offsetTop</code>]] property and the true top of the client area.
{{!}}-
{{!}}[[dom/properties/clientWidth|<code>clientWidth</code>]]
{{!}}Retrieves the width of the object including padding, but not including margin, border, or scroll bar.
{{!}}-
{{!}}[[dom/properties/constructor|<code>constructor</code>]]
{{!}}Returns a reference to the constructor of an object.
{{!}}-
{{!}}[[html/attributes/contentEditable|<code>contentEditable</code>]]
{{!}}Sets or retrieves the string that indicates whether the user can edit the content of the object.
{{!}}-
{{!}}[[html/attributes/dir|<code>dir</code>]]
{{!}}Sets or retrieves the reading order of the object.
{{!}}-
{{!}}[[dom/properties/disabled (redundant)|<code>disabled</code>]]
{{!}}Sets or gets the value that indicates whether the user can interact with the object.
{{!}}-
{{!}}[[dom/properties/firstChild|<code>firstChild</code>]]
{{!}}Gets a reference to the first child in the [[dom/properties/childNodes|<code>childNodes</code>]] collection of the object.
{{!}}-
{{!}}[[dom/traversal/properties/firstElementChild|<code>firstElementChild</code>]]
{{!}}Retrieves a reference to the first child element, or NULL if there are no child elements.
{{!}}-
{{!}}[[html/attributes/hideFocus|<code>hideFocus</code>]]
{{!}}Sets or gets the value that indicates whether the object visibly shows that it has focus.
{{!}}-
{{!}}[[html/attributes/id|<code>id</code>]]
{{!}}Sets or retrieves the string identifying the object.
{{!}}-
{{!}}[[dom/properties/innerdom/innerHTML|<code>innerHTML</code>]]
{{!}}Sets or retrieves the HTML between the start and end tags of the object.
{{!}}-
{{!}}[[dom/properties/innerText|<code>innerText</code>]]
{{!}}Sets or retrieves the text between the start and end tags of the object.
{{!}}-
{{!}}[[dom/properties/isContentEditable|<code>isContentEditable</code>]]
{{!}}Gets the value that indicates whether the user can edit the contents of the object.
{{!}}-
{{!}}[[dom/properties/isDisabled|<code>isDisabled</code>]]
{{!}}Gets the value that indicates whether the user can interact with the object.
{{!}}-
{{!}}[[dom/properties/isMultiLine|<code>isMultiLine</code>]]
{{!}}Retrieves the value indicating whether the content of the object contains one or more lines.
{{!}}-
{{!}}[[dom/traversal/properties/isTextEdit|<code>isTextEdit</code>]]
{{!}}Retrieves whether a [[dom/traversal/TextRange|<code>TextRange</code>]] object can be created using the object.
{{!}}-
{{!}}[[html/attributes/lang|<code>lang</code>]]
{{!}}Sets or retrieves the language to use.
{{!}}-
{{!}}[[html/attributes/language|<code>language</code>]]
{{!}}Sets or retrieves the language in which the current script is written.
{{!}}-
{{!}}[[dom/properties/lastChild|<code>lastChild</code>]]
{{!}}Gets a reference to the last child in the [[dom/properties/childNodes|<code>childNodes</code>]] collection of an object.
{{!}}-
{{!}}[[dom/traversal/properties/lastElementChild|<code>lastElementChild</code>]]
{{!}}Retrieves a reference to the last child element or NULL if there are no child elements.
{{!}}-
{{!}}[[html/attributes/leftMargin|<code>leftMargin</code>]]
{{!}}Sets or gets the left margin for the entire body of the document, which overrides the default margin.
{{!}}-
{{!}}[[html/attributes/link|<code>link</code>]]
{{!}}Sets or gets the color of the document links for the object.
{{!}}-
{{!}}[[dom/traversal/properties/nextElementSibling|<code>nextElementSibling</code>]]
{{!}}Retrieves a reference to the sibling element that immediately follows or NULL if the element does not have any sibling elements that follow it.
{{!}}-
{{!}}[[dom/properties/nextSibling|<code>nextSibling</code>]]
{{!}}Retrieves a reference to the next child of the parent for the object.
{{!}}-
{{!}}[[dom/properties/nodeName|<code>nodeName</code>]]
{{!}}Gets the name of a particular type of node.
{{!}}-
{{!}}[[dom/properties/nodeType|<code>nodeType</code>]]
{{!}}Retrieves the type of the requested node.
{{!}}-
{{!}}[[dom/properties/nodeValue|<code>nodeValue</code>]]
{{!}}Gets or sets the value of a node.
{{!}}-
{{!}}[[html/attributes/noWrap|<code>noWrap</code>]]
{{!}}Sets or retrieves whether the browser automatically performs wordwrap.
{{!}}-
{{!}}[[dom/properties/offsetHeight|<code>offsetHeight</code>]]
{{!}}Retrieves the height of the object relative to the layout or coordinate parent, as specified by the [[dom/properties/offsetParent|<code>offsetParent</code>]] property.
{{!}}-
{{!}}[[dom/properties/offsetLeft|<code>offsetLeft</code>]]
{{!}}Retrieves the calculated left position of the object relative to the layout or coordinate parent, as specified by the [[dom/properties/offsetParent|<code>offsetParent</code>]] property.
{{!}}-
{{!}}[[dom/properties/offsetParent|<code>offsetParent</code>]]
{{!}}Retrieves a reference to the container object that defines the [[dom/properties/offsetTop|<code>offsetTop</code>]] and [[dom/properties/offsetLeft|<code>offsetLeft</code>]] properties of the object.
{{!}}-
{{!}}[[dom/properties/offsetTop|<code>offsetTop</code>]]
{{!}}Retrieves the calculated top position of the object relative to the layout or coordinate parent, as specified by the [[dom/properties/offsetParent|<code>offsetParent</code>]] property.
{{!}}-
{{!}}[[dom/properties/offsetWidth|<code>offsetWidth</code>]]
{{!}}Retrieves the width of the object relative to the layout or coordinate parent, as specified by the [[dom/properties/offsetParent|<code>offsetParent</code>]] property.
{{!}}-
{{!}}[[dom/properties/outerdom/outerHTML|<code>outerHTML</code>]]
{{!}}Sets or retrieves the object and its content in HTML.
{{!}}-
{{!}}[[dom/properties/outerText|<code>outerText</code>]]
{{!}}Sets or retrieves the text of the object.
{{!}}-
{{!}}[[dom/properties/ownerDocument|<code>ownerDocument</code>]]
{{!}}Retrieves the [[dom/document|<code>document</code>]] object associated with the node.
{{!}}-
{{!}}[[dom/traversal/properties/parentElement|<code>parentElement</code>]]
{{!}}Retrieves the parent object in the object hierarchy.
{{!}}-
{{!}}[[dom/properties/parentNode|<code>parentNode</code>]]
{{!}}Retrieves the parent object in the document hierarchy.
{{!}}-
{{!}}[[dom/traversal/properties/parentTextEdit|<code>parentTextEdit</code>]]
{{!}}Retrieves the container object in the document hierarchy that can be used to create a [[dom/traversal/TextRange|<code>TextRange</code>]] containing the original object.
{{!}}-
{{!}}[[dom/traversal/properties/previousElementSibling|<code>previousElementSibling</code>]]
{{!}}Retrieves a reference to the immediately preceding sibling element or NULL if the element does not have any preceding siblings.
{{!}}-
{{!}}[[dom/properties/previousSibling|<code>previousSibling</code>]]
{{!}}Gets a reference to the previous child of the parent for the object.
{{!}}-
{{!}}[[dom/properties/readyState|<code>readyState</code>]]
{{!}}Retrieves the current state of the object.
{{!}}-
{{!}}<code>recordNumber</code>
{{!}}Retrieves the ordinal record from the data set that generated the object.
{{!}}-
{{!}}[[html/attributes/rightMargin|<code>rightMargin</code>]]
{{!}}Sets or gets the right margin for the entire body of the document.
{{!}}-
{{!}}[[html/attributes/role|<code>role</code>]]
{{!}}Sets or retrieves the role for this element.
{{!}}-
{{!}}<code>scopeName</code>
{{!}}Gets the namespace defined for the element.

This property is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[html/attributes/scroll|<code>scroll</code>]]
{{!}}Sets or gets a value that indicates whether the scroll bars are turned on or off.
{{!}}-
{{!}}[[dom/properties/scrollHeight|<code>scrollHeight</code>]]
{{!}}Retrieves the scrolling height of the object.
{{!}}-
{{!}}[[dom/properties/scrollLeft|<code>scrollLeft</code>]]
{{!}}Sets or retrieves the distance between the left edge of the object and the leftmost portion of the content currently visible in the window.
{{!}}-
{{!}}[[dom/properties/scrollTop|<code>scrollTop</code>]]
{{!}}Sets or retrieves the distance between the top of the object and the topmost portion of the content currently visible in the window.
{{!}}-
{{!}}[[dom/properties/scrollWidth|<code>scrollWidth</code>]]
{{!}}Retrieves the scrolling width of the object.
{{!}}-
{{!}}[[dom/properties/sourceIndex|<code>sourceIndex</code>]]
{{!}}Retrieves the ordinal position of the object, in source order, as the object appears in the document's [[dom/properties/all|<code>all</code>]] collection.
{{!}}-
{{!}}[[html/attributes/STYLE html_attribute|<code>STYLE</code>]]
{{!}}Sets an inline style for the element.
{{!}}-
{{!}}[[html/attributes/tabIndex|<code>tabIndex</code>]]
{{!}}Sets or retrieves the index that defines the tab order for the object.
{{!}}-
{{!}}[[dom/properties/tagName|<code>tagName</code>]]
{{!}}Retrieves the tag name of the object.
{{!}}-
{{!}}[[dom/properties/tagUrn|<code>tagUrn</code>]]
{{!}}Sets or gets the URN specified in the namespace declaration.

This property is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[html/attributes/text (body element)|<code>text</code>]]
{{!}}Sets or gets the text (foreground) color for the document body.
{{!}}-
{{!}}[[html/attributes/title|<code>title</code>]]
{{!}}Sets or retrieves advisory information (a ToolTip) for the object.
{{!}}-
{{!}}[[html/attributes/topMargin|<code>topMargin</code>]]
{{!}}Sets or gets the margin for the top of the document.
{{!}}-
{{!}}[[dom/properties/uniqueID|<code>uniqueID</code>]]
{{!}}Retrieves an autogenerated, unique identifier for the object.
{{!}}-
{{!}}[[dom/properties/uniqueNumber|<code>uniqueNumber</code>]]
{{!}}Retrieves the element's unique number.
{{!}}-
{{!}}[[html/attributes/vLink|<code>vLink</code>]]
{{!}}Sets or gets the color of links in the object that have already been visited.
{{!}}}
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/the-body-element.html
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/global.html#edef-BODY
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer (Windows)
|Version=8+
|Note=The value of the <code>background</code> attribute depends on the current document compatibility mode.
}}{{Compatibility Notes Row
|Browser=Internet Explorer (Windows)
|Version=6
|Note=When you use the <code>!DOCTYPE</code> declaration to specify standards-compliant mode, this object no longer represents the entire surface onto which a document's contents can be rendered. The object can obtain its size from its content, or you can set its size explicitly like a <code>div</code> object.
}}{{Compatibility Notes Row
|Browser=Internet Explorer (Windows)
|Version=6+
|Note=As of Microsoft Internet Explorer 6, when you use the <code>!DOCTYPE</code> declaration to specify standards-compliant mode, the <code><body></code> object can obtain its size from its content, or you can set its size explicitly—like a <code>div</code> object, for example. In standards-compliant mode, the <code><html></code> element represents the entire surface onto which a document's contents can be rendered. When the <code>!DOCTYPE</code> declaration does not specify standards-compliant mode, and with earlier versions of Windows Internet Explorer, the <code><body></code> object represents the entire surface onto which a document's contents can be rendered. The size of the <code><body></code> object cannot be changed and is equal to the size of the window. Margins you set on this object are rendered inside the border and scrollbars of the object.
}}
}}
{{See_Also_Section
|Topic_clusters=Document Structure
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}