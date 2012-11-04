{{Page_Title|The <head> element}}
{{Flags
|High-level issues=Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Cleanup
}}
{{Standardization_Status|De Facto Standard}}
{{API_Name}}
{{Summary_Section|The <code><head></code> element represents a collection of metadata for the document.}}
{{Markup_Element
|DOM_interface=dom/HTMLHeadElement
|Content=The <code>head</code> element provides information that does not affect the rendering of the document but could be of use to the application. 

The following tags are valid in this element:
*<code>base</code>
*<code>basefont</code>
*<code>bgsound</code>
*<code>link</code>
*<code>meta</code>
*[[html/elements/nextID|<code>nextID</code>]]
*<code>script</code>
*<code>style</code>
*<code>title</code>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The <code><head></code> element is contained by the <code><html></code> element and contains the <code><title></code> element.
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
|LiveURL=http://test.w3.org/html/examples/elements/head/head01.html
}}
}}
{{Notes_Section
|Import_Notes====Members===
The <code>head</code> object has these types of members:
*[[#Events|Events]]
*[[#Methods|Methods]]
*[[#Properties|Properties]]


====Events====
The <code>head</code> object has these events.
{{{!}} class="wikitable"
{{!}}-
!Event
!Description
{{!}}-
{{!}}[[dom/events/abort|<code>onabort</code>]]
{{!}}Fires when the user aborts the download.
{{!}}-
{{!}}[[dom/events/afterupdate|<code>onafterupdate</code>]]
{{!}}Fires on a databound object after successfully updating the associated data in the data source object.
{{!}}-
{{!}}[[dom/events/beforecopy|<code>onbeforecopy</code>]]
{{!}}Fires on the source object before the selection is copied to the system clipboard.
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
{{!}}[[dom/events/dataavailable|<code>ondataavailable</code>]]
{{!}}Fires periodically as data arrives from data source objects that asynchronously transmit their data.
{{!}}-
{{!}}[[dom/events/datasetchanged|<code>ondatasetchanged</code>]]
{{!}}Fires when the data set exposed by a data source object changes.
{{!}}-
{{!}}[[dom/events/datasetcomplete|<code>ondatasetcomplete</code>]]
{{!}}Fires to indicate that all data is available from the data source object.
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
{{!}}[[dom/events/input|<code>oninput</code>]]
{{!}}Occurs when the text content of an element is changed through the user interface.
{{!}}-
{{!}}[[dom/events/layoutcomplete|<code>onlayoutcomplete</code>]]
{{!}}Fires when the print or print preview layout process finishes filling the current LayoutRect object with content from the source document.
{{!}}-
{{!}}[[dom/events/load|<code>onload</code>]]
{{!}}Fires immediately after the client loads the object.
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
{{!}}[[dom/events/selectstart|<code>onselect</code>]]
{{!}}Fires when the current selection changes.
{{!}}}
 

====Methods====
The <code>head</code> object has these methods.
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
{{!}}[[dom/methods/getAdjacentText|<code>getAdjacentText</code>]]
{{!}}Returns the adjacent text string.
{{!}}-
{{!}}[[dom/methods/getAttribute|<code>getAttribute</code>]]
{{!}}Retrieves the value of the specified attribute.
{{!}}-
{{!}}[[dom/methods/getAttributeNode|<code>getAttributeNode</code>]]
{{!}}Retrieves an [[dom/attributes|<code>attribute</code>]] object referenced by the <code>attribute<code>.[[html/attributes/name|<code>name</code>]] property.
{{!}}-
{{!}}[[dom/methods/getAttributeNodeNS|<code>getAttributeNodeNS</code>]]
{{!}}Gets an [[dom/attributes|<code>attribute</code>]] object that matches the specified namespace and name.
{{!}}-
{{!}}[[dom/methods/getAttributeNS|<code>getAttributeNS</code>]]
{{!}}Gets the value of the specified attribute within the specified namespace.
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
The <code>head</code> object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}[[dom/properties/attributes|<code>attributes</code>]]
{{!}}Retrieves a collection of attributes of the object.
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
{{!}}[[dom/properties/constructor|<code>constructor</code>]]
{{!}}Returns a reference to the constructor of an object.
{{!}}-
{{!}}[[dom/properties/firstChild|<code>firstChild</code>]]
{{!}}Gets a reference to the first child in the [[dom/properties/childNodes|<code>childNodes</code>]] collection of the object.
{{!}}-
{{!}}[[dom/traversal/properties/firstElementChild|<code>firstElementChild</code>]]
{{!}}Retrieves a reference to the first child element, or null if there are no child elements.
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
{{!}}Retrieves a reference to the last child element or null if there are no child elements.
{{!}}-
{{!}}[[dom/traversal/properties/nextElementSibling|<code>nextElementSibling</code>]]
{{!}}Retrieves a reference to the sibling element that immediately follows or null if the element does not have any sibling elements that follow it.
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
{{!}}[[dom/properties/offsetHeight|<code>offsetHeight</code>]]
{{!}}Retrieves the height of the object relative to the layout or coordinate parent, as specified by the [[dom/properties/offsetParent|<code>offsetParent</code>]] property.
{{!}}-
{{!}}[[dom/properties/offsetParent|<code>offsetParent</code>]]
{{!}}Retrieves a reference to the container object that defines the [[dom/properties/offsetTop|<code>offsetTop</code>]] and [[dom/properties/offsetLeft|<code>offsetLeft</code>]] properties of the object.
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
{{!}}Retrieves a reference to the immediately preceding sibling element or null if the element does not have any preceding siblings.
{{!}}-
{{!}}[[dom/properties/previousSibling|<code>previousSibling</code>]]
{{!}}Gets a reference to the previous child of the parent for the object.
{{!}}-
{{!}}<code>profile</code>
{{!}}Sets or retrieves  one or more URIs in which the object properties and legal values for those properties are defined.
{{!}}-
{{!}}[[dom/properties/readyState|<code>readyState</code>]]
{{!}}Retrieves the current state of the object.
{{!}}-
{{!}}<code>recordNumber</code>
{{!}}Retrieves the ordinal record from the data set that generated the object.
{{!}}-
{{!}}[[html/attributes/role|<code>role</code>]]
{{!}}Sets or retrieves the role for this element.
{{!}}-
{{!}}<code>scopeName</code>
{{!}}Gets the namespace defined for the element. 

This property is not supported for Metro style apps using JavaScript.
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
{{!}}[[dom/properties/tagName|<code>tagName</code>]]
{{!}}Retrieves the tag name of the object.
{{!}}-
{{!}}[[dom/properties/tagUrn|<code>tagUrn</code>]]
{{!}}Sets or gets the URN specified in the namespace declaration. 

This property is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[html/attributes/title|<code>title</code>]]
{{!}}Sets or retrieves advisory information (a ToolTip) for the object.
{{!}}-
{{!}}[[dom/properties/uniqueID|<code>uniqueID</code>]]
{{!}}Retrieves an autogenerated, unique identifier for the object.
{{!}}-
{{!}}[[dom/properties/uniqueNumber|<code>uniqueNumber</code>]]
{{!}}Retrieves the element's unique number.
{{!}}}
 
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/the-head-element.html#the-head-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/global.html#edef-HEAD
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
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
|Notes_rows=
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