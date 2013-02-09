{{Page_Title}}
{{Flags
|High-level issues=Move Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Editorial notes=There is no such thing as a "comment" element. Comments are a part of the HTML syntax. This page should be moved out of the html/elements tree.
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The comment syntax indicates text within an HTML document that is not displayed on the rendered page in the browser.
A comment starts with &lt;!-- and ends with --&gt;.
}}
{{Markup_Element
|DOM_interface=dom/Comment
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;!-- This is a comment. Comments are not displayed in the browser --&gt;
}}
}}
{{Notes_Section
|Notes=The '''COMMENT''' element is treated as a no-scope element and does not expose any [[dom/properties/children (document)+B416|'''children''']].
The '''comment'''.[[dom/properties/length|'''length''']] property returns the number of characters in the object.
|Import_Notes====Additional Members (MSDN)===
The '''comment''' object has these types of members:
*[[#Additional_Events|Additional Events]]
*[[#Additional_Methods|Additional Methods]]
*[[#Additional_Properties|Additional Properties]]


====Additional Events====
The '''comment''' object has these events.
{{{!}} class="wikitable"
{{!}}-
!Event
!Description
{{!}}-
{{!}}[[dom/events/abort|'''onabort''']]
{{!}}Fires when the user aborts the download.
{{!}}-
{{!}}[[dom/events/afterupdate|'''onafterupdate''']]
{{!}}Fires on a databound object after successfully updating the associated data in the data source object.
{{!}}-
{{!}}[[dom/events/beforecopy|'''onbeforecopy''']]
{{!}}Fires on the source object before the selection is copied to the system clipboard.
{{!}}-
{{!}}[[dom/events/beforeupdate|'''onbeforeupdate''']]
{{!}}Fires on a databound object before updating the associated data in the data source object.
{{!}}-
{{!}}[[dom/events/cellchange|'''oncellchange''']]
{{!}}Fires when data changes in the data provider.
{{!}}-
{{!}}[[dom/events/change|'''onchange''']]
{{!}}Fires when the contents of the object or selection have changed.
{{!}}-
{{!}}[[dom/events/dataavailable|'''ondataavailable''']]
{{!}}Fires periodically as data arrives from data source objects that asynchronously transmit their data.
{{!}}-
{{!}}[[dom/events/datasetchanged|'''ondatasetchanged''']]
{{!}}Fires when the data set exposed by a data source object changes.
{{!}}-
{{!}}[[dom/events/datasetcomplete|'''ondatasetcomplete''']]
{{!}}Fires to indicate that all data is available from the data source object.
{{!}}-
{{!}}[[dom/events/error|'''onerror''']]
{{!}}Fires when an error occurs during object loading.
{{!}}-
{{!}}[[dom/events/errorupdate|'''onerrorupdate''']]
{{!}}Fires on a databound object when an error occurs while updating the associated data in the data source object.
{{!}}-
{{!}}[[dom/events/filterchange|'''onfilterchange''']]
{{!}}Fires when a visual filter changes state or completes a transition.
{{!}}-
{{!}}[[dom/events/input|'''oninput''']]
{{!}}Occurs when the text content of an element is changed through the user interface.
{{!}}-
{{!}}[[dom/events/layoutcomplete|'''onlayoutcomplete''']]
{{!}}Fires when the print or print preview layout process finishes filling the current LayoutRect object with content from the source document.
{{!}}-
{{!}}[[dom/events/load|'''onload''']]
{{!}}Fires immediately after the client loads the object.
{{!}}-
{{!}}[[dom/events/propertychange|'''onpropertychange''']]
{{!}}Fires when a property changes on the object.
{{!}}-
{{!}}[[dom/events/readystatechange|'''onreadystatechange''']]
{{!}}Fires when the state of the object has changed.
{{!}}-
{{!}}[[dom/events/reset|'''onreset''']]
{{!}}Fires when the user resets a form.
{{!}}-
{{!}}[[dom/events/resize|'''onresize''']]
{{!}}Fires when the size of the object is about to change.
{{!}}-
{{!}}[[dom/events/rowenter|'''onrowenter''']]
{{!}}Fires to indicate that the current row has changed in the data source and new data values are available on the object.
{{!}}-
{{!}}[[dom/events/rowexit|'''onrowexit''']]
{{!}}Fires just before the data source control changes the current row in the object.
{{!}}-
{{!}}[[dom/events/rowsdelete|'''onrowsdelete''']]
{{!}}Fires when rows are about to be deleted from the recordset.
{{!}}-
{{!}}[[dom/events/rowsinserted|'''onrowsinserted''']]
{{!}}Fires just after new rows are inserted in the current recordset.
{{!}}-
{{!}}[[dom/events/selectstart|'''onselect''']]
{{!}}Fires when the current selection changes.
{{!}}}
 

====Additional Methods====
The '''comment''' object has these methods.
{{{!}} class="wikitable"
{{!}}-
!Method
!Description
{{!}}-
{{!}}'''addBehavior'''
{{!}}Attaches a behavior to the element.
{{!}}-
{{!}}[[dom/methods/appendChild|'''appendChild''']]
{{!}}Appends an element as a child to the object.
{{!}}-
{{!}}[[dom/methods/appendData|'''appendData''']]
{{!}}Adds a new character string to the end of the object.
{{!}}-
{{!}}[[dom/methods/applyElement|'''applyElement''']]
{{!}}Makes the element either a child or parent of another element.
{{!}}-
{{!}}[[dom/methods/attachEvent|'''attachEvent''']]
{{!}}Binds the specified function to an event, so that the function gets called whenever the event fires on the object.
{{!}}-
{{!}}[[dom/methods/clearAttributes|'''clearAttributes''']]
{{!}}Removes all attributes and values from the object.
{{!}}-
{{!}}[[dom/methods/cloneNode|'''cloneNode''']]
{{!}}Copies a reference to the object from the document hierarchy.
{{!}}-
{{!}}[[dom/methods/componentFromPoint|'''componentFromPoint''']]
{{!}}Returns the component located at the specified coordinates via certain events.
{{!}}-
{{!}}[[dom/methods/deleteData|'''deleteData''']]
{{!}}Removes a specified range of characters from the object.
{{!}}-
{{!}}[[dom/methods/detachEvent|'''detachEvent''']]
{{!}}Unbinds the specified function from the event, so that the function stops receiving notifications when the event fires.
{{!}}-
{{!}}[[dom/methods/doScroll|'''doScroll''']]
{{!}}Simulates a click on a scroll bar component.
{{!}}-
{{!}}[[dom/methods/dragDrop|'''dragDrop''']]
{{!}}Initiates a drag event.
{{!}}-
{{!}}[[dom/methods/fireEvent|'''fireEvent''']]
{{!}}Fires a specified event on the object.
{{!}}-
{{!}}[[dom/methods/getAdjacentText|'''getAdjacentText''']]
{{!}}Returns the adjacent text string.
{{!}}-
{{!}}[[dom/methods/getAttribute|'''getAttribute''']]
{{!}}Retrieves the value of the specified attribute.
{{!}}-
{{!}}[[dom/methods/getAttributeNode|'''getAttributeNode''']]
{{!}}Retrieves an [[dom/attributes|'''attribute''']] object referenced by the '''attribute'''.[[html/attributes/name|'''name''']] property.
{{!}}-
{{!}}[[dom/methods/getAttributeNodeNS|'''getAttributeNodeNS''']]
{{!}}Gets an [[dom/attributes|'''attribute''']] object that matches the specified namespace and name.
{{!}}-
{{!}}[[dom/methods/getAttributeNS|'''getAttributeNS''']]
{{!}}Gets the value of the specified attribute within the specified namespace.
{{!}}-
{{!}}[[dom/methods/getBoundingClientRect|'''getBoundingClientRect''']]
{{!}}Retrieves an object that specifies the bounds of a collection of [[dom/TextRectangle|'''TextRectangle''']] objects.
{{!}}-
{{!}}[[dom/methods/getClientRects|'''getClientRects''']]
{{!}}Retrieves a collection of rectangles that describes the layout of the contents of an object or range within the client. Each rectangle describes a single line.
{{!}}-
{{!}}[[dom/methods/getElementsByClassName|'''getElementsByClassName''']]
{{!}}Gets a collection of objects that are based on the value of the [[dom/properties/className|'''CLASS''']] attribute.
{{!}}-
{{!}}[[dom/methods/getElementsByTagNameNS|'''getElementsByTagNameNS''']]
{{!}}Gets a collection of objects that are based on the specified element names within a specified namespace.
{{!}}-
{{!}}[[dom/methods/hasAttribute|'''hasAttribute''']]
{{!}}Determines whether an attribute with the specified name exists.
{{!}}-
{{!}}[[dom/methods/hasAttributeNS|'''hasAttributeNS''']]
{{!}}Determines whether an attribute that has the specified namespace and name exists.
{{!}}-
{{!}}[[dom/methods/hasAttributes|'''hasAttributes''']]
{{!}}Determines whether one or more attributes exist for the object.
{{!}}-
{{!}}[[dom/methods/hasChildNodes|'''hasChildNodes''']]
{{!}}Returns a value that indicates whether the object has children.
{{!}}-
{{!}}[[dom/methods/insertAdjacentElement|'''insertAdjacentElement''']]
{{!}}Inserts an element at the specified location.
{{!}}-
{{!}}[[dom/methods/insertBefore|'''insertBefore''']]
{{!}}Inserts an element into the document hierarchy as a child node of a parent object.
{{!}}-
{{!}}[[dom/methods/insertData|'''insertData''']]
{{!}}Inserts a new character string in the object at a specified offset.
{{!}}-
{{!}}[[dom/methods/mergeAttributes|'''mergeAttributes''']]
{{!}}Copies all read/write attributes to the specified element.
{{!}}-
{{!}}[[dom/methods/matchesSelector|'''msMatchesSelector''']]
{{!}}Determines whether an object matches the specified selector.
{{!}}-
{{!}}[[dom/methods/normalize|'''normalize''']]
{{!}}Merges adjacent DOM objects to produce a normalized document object model.
{{!}}-
{{!}}[[dom/methods/removeAttribute|'''removeAttribute''']]
{{!}}Removes an attribute from an object.
{{!}}-
{{!}}[[dom/methods/removeAttributeNode|'''removeAttributeNode''']]
{{!}}Removes an [[dom/attributes|'''attribute''']] object from the object.
{{!}}-
{{!}}[[dom/methods/removeAttributeNS|'''removeAttributeNS''']]
{{!}}Removes the specified attribute from the object.
{{!}}-
{{!}}'''removeBehavior'''
{{!}}Detaches a behavior from the element.
{{!}}-
{{!}}[[dom/methods/removeChild|'''removeChild''']]
{{!}}Removes a child node from the object.
{{!}}-
{{!}}[[dom/methods/removeNode|'''removeNode''']]
{{!}}Removes the object from the document hierarchy.
{{!}}-
{{!}}[[dom/methods/replaceAdjacentText|'''replaceAdjacentText''']]
{{!}}Replaces the text adjacent to the element.
{{!}}-
{{!}}[[dom/methods/replaceChild|'''replaceChild''']]
{{!}}Replaces an existing child element with a new child element.
{{!}}-
{{!}}[[dom/methods/replaceData|'''replaceData''']]
{{!}}Replaces a specified range of characters in the object with a new character string.
{{!}}-
{{!}}[[dom/methods/replaceNode|'''replaceNode''']]
{{!}}Replaces the object with another element.
{{!}}-
{{!}}[[dom/traversal/methods/scrollIntoView|'''scrollIntoView''']]
{{!}}Causes the object to scroll into view, aligning it either at the top or bottom of the window.
{{!}}-
{{!}}[[dom/methods/setActive|'''setActive''']]
{{!}}Sets the object as active without setting focus to the object.
{{!}}-
{{!}}[[dom/methods/setAttribute|'''setAttribute''']]
{{!}}Sets the value of the specified attribute.
{{!}}-
{{!}}[[dom/methods/setAttributeNode|'''setAttributeNode''']]
{{!}}Sets an [[dom/attributes|'''attribute''']] object node as part of the object.
{{!}}-
{{!}}[[dom/methods/setAttributeNodeNS|'''setAttributeNodeNS''']]
{{!}}Sets an [[dom/attributes|'''attribute''']] object as part of the object.
{{!}}-
{{!}}[[dom/methods/setAttributeNS|'''setAttributeNS''']]
{{!}}Sets the value of the specified attribute within the specified namespace.
{{!}}-
{{!}}[[dom/methods/setCapture|'''setCapture''']]
{{!}}Sets the mouse capture to the object that belongs to the current document.
{{!}}-
{{!}}[[dom/methods/substringData|'''substringData''']]
{{!}}Extracts a range of characters from the object.
{{!}}-
{{!}}[[dom/methods/swapNode|'''swapNode''']]
{{!}}Exchanges the location of two objects in the document hierarchy.
{{!}}}
 

====Additional Properties====
The '''comment''' object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}[[dom/properties/attributes|'''attributes''']]
{{!}}Retrieves a collection of attributes of the object.
{{!}}-
{{!}}[[dom/properties/canHaveChildren|'''canHaveChildren''']]
{{!}}Gets a value indicating whether the object can contain child objects.
{{!}}-
{{!}}[[dom/properties/canHavedom/canHaveHTML|'''canHaveHTML''']]
{{!}}Retrieves the value indicating whether the object can contain rich HTML markup.
{{!}}-
{{!}}[[dom/traversal/properties/childElementCount|'''childElementCount''']]
{{!}}Retrieves the number of immediate child nodes of the current element or a zero if the element does not contain any child nodes. [[dom/traversal/properties/childElementCount|'''childElementCount''']] does not return all child nodes, only child nodes that are [[dom/properties/nodeType|'''nodeType''']] {{=}}1, or element nodes.
{{!}}-
{{!}}[[dom/properties/constructor|'''constructor''']]
{{!}}Returns a reference to the constructor of an object.
{{!}}-
{{!}}[[html/attributes/data|'''data''']]
{{!}}Sets or retrieves the URL that references the data of the object.
{{!}}-
{{!}}[[dom/properties/firstChild|'''firstChild''']]
{{!}}Gets a reference to the first child in the [[dom/properties/childNodes|'''childNodes''']] collection of the object.
{{!}}-
{{!}}[[dom/traversal/properties/firstElementChild|'''firstElementChild''']]
{{!}}Retrieves a reference to the first child element, or null if there are no child elements.
{{!}}-
{{!}}[[html/attributes/id|'''id''']]
{{!}}Sets or retrieves the string identifying the object.
{{!}}-
{{!}}[[dom/properties/isContentEditable|'''isContentEditable''']]
{{!}}Gets the value that indicates whether the user can edit the contents of the object.
{{!}}-
{{!}}[[dom/properties/isDisabled|'''isDisabled''']]
{{!}}Gets the value that indicates whether the user can interact with the object.
{{!}}-
{{!}}[[dom/properties/isMultiLine|'''isMultiLine''']]
{{!}}Retrieves the value indicating whether the content of the object contains one or more lines.
{{!}}-
{{!}}[[dom/properties/lastChild|'''lastChild''']]
{{!}}Gets a reference to the last child in the [[dom/properties/childNodes|'''childNodes''']] collection of an object.
{{!}}-
{{!}}[[dom/traversal/properties/lastElementChild|'''lastElementChild''']]
{{!}}Retrieves a reference to the last child element or null if there are no child elements.
{{!}}-
{{!}}[[dom/properties/length|'''length''']]
{{!}}Sets or retrieves the number of objects in a collection.
{{!}}-
{{!}}[[dom/traversal/properties/nextElementSibling|'''nextElementSibling''']]
{{!}}Retrieves a reference to the sibling element that immediately follows or null if the element does not have any sibling elements that follow it.
{{!}}-
{{!}}[[dom/properties/nextSibling|'''nextSibling''']]
{{!}}Retrieves a reference to the next child of the parent for the object.
{{!}}-
{{!}}[[dom/properties/nodeName|'''nodeName''']]
{{!}}Gets the name of a particular type of node.
{{!}}-
{{!}}[[dom/properties/nodeType|'''nodeType''']]
{{!}}Retrieves the type of the requested node.
{{!}}-
{{!}}[[dom/properties/nodeValue|'''nodeValue''']]
{{!}}Gets or sets the value of a node.
{{!}}-
{{!}}[[dom/properties/ownerDocument|'''ownerDocument''']]
{{!}}Retrieves the [[dom/document|'''document''']] object associated with the node.
{{!}}-
{{!}}[[dom/properties/parentNode|'''parentNode''']]
{{!}}Retrieves the parent object in the document hierarchy.
{{!}}-
{{!}}[[dom/traversal/properties/previousElementSibling|'''previousElementSibling''']]
{{!}}Retrieves a reference to the immediately preceding sibling element or null if the element does not have any preceding siblings.
{{!}}-
{{!}}[[dom/properties/previousSibling|'''previousSibling''']]
{{!}}Gets a reference to the previous child of the parent for the object.
{{!}}-
{{!}}[[dom/properties/readyState|'''readyState''']]
{{!}}Retrieves the current state of the object.
{{!}}-
{{!}}[[html/attributes/role|'''role''']]
{{!}}Sets or retrieves the role for this element.
{{!}}-
{{!}}'''scopeName'''
{{!}}Gets the namespace defined for the element. 

This property is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/properties/tagUrn|'''tagUrn''']]
{{!}}Sets or gets the URN specified in the namespace declaration. 

This property is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/properties/text|'''text''']]
{{!}}Retrieves or sets the text of the object as a string.
{{!}}-
{{!}}[[dom/properties/uniqueID|'''uniqueID''']]
{{!}}Retrieves an autogenerated, unique identifier for the object.
{{!}}}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>HTML Comment Element</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}