{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The script element enables dynamic script and data blocks to be included in documents.}}
{{Markup_Element
|DOM_interface=dom/HTMLScriptElement
|Content====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 18.2.1


===Members===
The '''script''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''script''' object has these events.
{{{!}} class="wikitable"
{{!}}-
!Event
!Description
{{!}}-
{{!}}[[dom/events/abort{{!}}'''onabort''']]
{{!}}Fires when the user aborts the download.
{{!}}-
{{!}}[[dom/events/afterupdate{{!}}'''onafterupdate''']]
{{!}}Fires on a databound object after successfully updating the associated data in the data source object.
{{!}}-
{{!}}[[dom/events/beforecopy{{!}}'''onbeforecopy''']]
{{!}}Fires on the source object before the selection is copied to the system clipboard.
{{!}}-
{{!}}[[dom/events/beforeupdate{{!}}'''onbeforeupdate''']]
{{!}}Fires on a databound object before updating the associated data in the data source object.
{{!}}-
{{!}}[[dom/events/cellchange{{!}}'''oncellchange''']]
{{!}}Fires when data changes in the data provider.
{{!}}-
{{!}}[[dom/events/change{{!}}'''onchange''']]
{{!}}Fires when the contents of the object or selection have changed.
{{!}}-
{{!}}[[dom/events/dataavailable{{!}}'''ondataavailable''']]
{{!}}Fires periodically as data arrives from data source objects that asynchronously transmit their data.
{{!}}-
{{!}}[[dom/events/datasetchanged{{!}}'''ondatasetchanged''']]
{{!}}Fires when the data set exposed by a data source object changes.
{{!}}-
{{!}}[[dom/events/datasetcomplete{{!}}'''ondatasetcomplete''']]
{{!}}Fires to indicate that all data is available from the data source object.
{{!}}-
{{!}}[[dom/events/error{{!}}'''onerror''']]
{{!}}Fires when an error occurs during object loading.
{{!}}-
{{!}}[[dom/events/errorupdate{{!}}'''onerrorupdate''']]
{{!}}Fires on a databound object when an error occurs while updating the associated data in the data source object.
{{!}}-
{{!}}[[dom/events/filterchange{{!}}'''onfilterchange''']]
{{!}}Fires when a visual filter changes state or completes a transition.
{{!}}-
{{!}}[[dom/events/input{{!}}'''oninput''']]
{{!}}Occurs when the text content of an element is changed through the user interface.
{{!}}-
{{!}}[[dom/events/layoutcomplete{{!}}'''onlayoutcomplete''']]
{{!}}Fires when the print or print preview layout process finishes filling the current LayoutRect object with content from the source document.
{{!}}-
{{!}}[[dom/events/load{{!}}'''onload''']]
{{!}}Fires immediately after the client loads the object.
{{!}}-
{{!}}[[dom/events/propertychange{{!}}'''onpropertychange''']]
{{!}}Fires when a property changes on the object.
{{!}}-
{{!}}[[dom/events/readystatechange{{!}}'''onreadystatechange''']]
{{!}}Fires when the state of the object has changed.
{{!}}-
{{!}}[[dom/events/reset{{!}}'''onreset''']]
{{!}}Fires when the user resets a form.
{{!}}-
{{!}}[[dom/events/resize{{!}}'''onresize''']]
{{!}}Fires when the size of the object is about to change.
{{!}}-
{{!}}[[dom/events/rowenter{{!}}'''onrowenter''']]
{{!}}Fires to indicate that the current row has changed in the data source and new data values are available on the object.
{{!}}-
{{!}}[[dom/events/rowexit{{!}}'''onrowexit''']]
{{!}}Fires just before the data source control changes the current row in the object.
{{!}}-
{{!}}[[dom/events/rowsdelete{{!}}'''onrowsdelete''']]
{{!}}Fires when rows are about to be deleted from the recordset.
{{!}}-
{{!}}[[dom/events/rowsinserted{{!}}'''onrowsinserted''']]
{{!}}Fires just after new rows are inserted in the current recordset.
{{!}}-
{{!}}[[dom/events/selectstart{{!}}'''onselect''']]
{{!}}Fires when the current selection changes.
{{!}}}
 

====Methods====
The '''script''' object has these methods.
{{{!}} class="wikitable"
{{!}}-
!Method
!Description
{{!}}-
{{!}}'''addBehavior'''
{{!}}Attaches a behavior to the element. 

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/methods/applyElement{{!}}'''applyElement''']]
{{!}}Makes the element either a child or parent of another element.
{{!}}-
{{!}}[[dom/methods/attachEvent{{!}}'''attachEvent''']]
{{!}}Binds the specified function to an event, so that the function gets called whenever the event fires on the object.
{{!}}-
{{!}}[[dom/methods/clearAttributes{{!}}'''clearAttributes''']]
{{!}}Removes all attributes and values from the object.
{{!}}-
{{!}}[[dom/methods/cloneNode{{!}}'''cloneNode''']]
{{!}}Copies a reference to the object from the document hierarchy.
{{!}}-
{{!}}[[dom/methods/componentFromPoint{{!}}'''componentFromPoint''']]
{{!}}Returns the component located at the specified coordinates via certain events.
{{!}}-
{{!}}[[dom/methods/detachEvent{{!}}'''detachEvent''']]
{{!}}Unbinds the specified function from the event, so that the function stops receiving notifications when the event fires.
{{!}}-
{{!}}[[dom/methods/doScroll{{!}}'''doScroll''']]
{{!}}Simulates a click on a scroll bar component.
{{!}}-
{{!}}[[dom/methods/dragDrop{{!}}'''dragDrop''']]
{{!}}Initiates a drag event.
{{!}}-
{{!}}[[dom/methods/fireEvent{{!}}'''fireEvent''']]
{{!}}Fires a specified event on the object.
{{!}}-
{{!}}[[dom/methods/getAdjacentText{{!}}'''getAdjacentText''']]
{{!}}Returns the adjacent text string.
{{!}}-
{{!}}[[dom/methods/getAttribute{{!}}'''getAttribute''']]
{{!}}Retrieves the value of the specified attribute.
{{!}}-
{{!}}[[dom/methods/getAttributeNode{{!}}'''getAttributeNode''']]
{{!}}Retrieves an [[dom/attributes{{!}}'''attribute''']] object referenced by the '''attribute'''.[[html/attributes/name{{!}}'''name''']] property.
{{!}}-
{{!}}[[dom/methods/getAttributeNodeNS{{!}}'''getAttributeNodeNS''']]
{{!}}Gets an [[dom/attributes{{!}}'''attribute''']] object that matches the specified namespace and name.
{{!}}-
{{!}}[[dom/methods/getAttributeNS{{!}}'''getAttributeNS''']]
{{!}}Gets the value of the specified attribute within the specified namespace.
{{!}}-
{{!}}[[dom/methods/getElementsByClassName{{!}}'''getElementsByClassName''']]
{{!}}Gets a collection of objects that are based on the value of the [[dom/properties/className{{!}}'''CLASS''']] attribute.
{{!}}-
{{!}}[[dom/methods/getElementsByTagName{{!}}'''getElementsByTagName''']]
{{!}}Retrieves a collection of objects based on the specified element name.
{{!}}-
{{!}}[[dom/methods/getElementsByTagNameNS{{!}}'''getElementsByTagNameNS''']]
{{!}}Gets a collection of objects that are based on the specified element names within a specified namespace.
{{!}}-
{{!}}[[dom/methods/hasAttribute{{!}}'''hasAttribute''']]
{{!}}Determines whether an attribute with the specified name exists.
{{!}}-
{{!}}[[dom/methods/hasAttributeNS{{!}}'''hasAttributeNS''']]
{{!}}Determines whether an attribute that has the specified namespace and name exists.
{{!}}-
{{!}}[[dom/methods/hasAttributes{{!}}'''hasAttributes''']]
{{!}}Determines whether one or more attributes exist for the object.
{{!}}-
{{!}}[[dom/methods/hasChildNodes{{!}}'''hasChildNodes''']]
{{!}}Returns a value that indicates whether the object has children.
{{!}}-
{{!}}[[dom/methods/insertAdjacentElement{{!}}'''insertAdjacentElement''']]
{{!}}Inserts an element at the specified location.
{{!}}-
{{!}}[[dom/methods/mergeAttributes{{!}}'''mergeAttributes''']]
{{!}}Copies all read/write attributes to the specified element.
{{!}}-
{{!}}[[dom/methods/matchesSelector{{!}}'''msMatchesSelector''']]
{{!}}Determines whether an object matches the specified selector.
{{!}}-
{{!}}[[dom/methods/normalize{{!}}'''normalize''']]
{{!}}Merges adjacent DOM objects to produce a normalized document object model.
{{!}}-
{{!}}[[dom/methods/removeAttribute{{!}}'''removeAttribute''']]
{{!}}Removes an attribute from an object.
{{!}}-
{{!}}[[dom/methods/removeAttributeNode{{!}}'''removeAttributeNode''']]
{{!}}Removes an [[dom/attributes{{!}}'''attribute''']] object from the object.
{{!}}-
{{!}}[[dom/methods/removeAttributeNS{{!}}'''removeAttributeNS''']]
{{!}}Removes the specified attribute from the object.
{{!}}-
{{!}}'''removeBehavior'''
{{!}}Detaches a behavior from the element.
{{!}}-
{{!}}[[dom/methods/removeNode{{!}}'''removeNode''']]
{{!}}Removes the object from the document hierarchy.
{{!}}-
{{!}}[[dom/methods/replaceAdjacentText{{!}}'''replaceAdjacentText''']]
{{!}}Replaces the text adjacent to the element.
{{!}}-
{{!}}[[dom/methods/replaceNode{{!}}'''replaceNode''']]
{{!}}Replaces the object with another element.
{{!}}-
{{!}}[[dom/methods/setActive{{!}}'''setActive''']]
{{!}}Sets the object as active without setting focus to the object.
{{!}}-
{{!}}[[dom/methods/setAttribute{{!}}'''setAttribute''']]
{{!}}Sets the value of the specified attribute.
{{!}}-
{{!}}[[dom/methods/setAttributeNode{{!}}'''setAttributeNode''']]
{{!}}Sets an [[dom/attributes{{!}}'''attribute''']] object node as part of the object.
{{!}}-
{{!}}[[dom/methods/setAttributeNodeNS{{!}}'''setAttributeNodeNS''']]
{{!}}Sets an [[dom/attributes{{!}}'''attribute''']] object as part of the object.
{{!}}-
{{!}}[[dom/methods/setAttributeNS{{!}}'''setAttributeNS''']]
{{!}}Sets the value of the specified attribute within the specified namespace.
{{!}}-
{{!}}[[dom/methods/setCapture{{!}}'''setCapture''']]
{{!}}Sets the mouse capture to the object that belongs to the current document.
{{!}}-
{{!}}[[dom/methods/swapNode{{!}}'''swapNode''']]
{{!}}Exchanges the location of two objects in the document hierarchy.
{{!}}}
 

====Properties====
The '''script''' object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}[[html/attributes/src (script){{!}}'''src''']]
{{!}}Retrieves the URL to an external file that contains the source code or data.
{{!}}-
{{!}}[[html/attributes/type (script element){{!}}'''type''']]
{{!}}Sets or retrieves the MIME type for the associated scripting engine.
{{!}}-
{{!}}[[html/attributes/language{{!}}'''language''']]
{{!}}Sets or retrieves the programming language for the associated scripting engine. Depracated, use type instead.
{{!}}-  
{{!}}[[html/attributes/defer{{!}}'''defer''']]
{{!}}Sets or retrieves the whether or not the script will be loaded asynchronously(but executed synchronously).
{{!}}-
{{!}}[[html/attributes/async{{!}}'''aync''']]
{{!}}Sets or retrieves the whether or not the script will be loaded asynchronously(but executed asynchronously). Non-standard.
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Code within the '''script''' block that is not contained within a function is executed immediately as the document is loaded. To keep scripts from being displayed, nest the '''script''' block within a '''comment''' block.
Script appearing after a '''frameSet''' element is ignored.
Whenever the [[html/attributes/language|'''language''']] attribute is not defined on the '''script''' object, then ''MSHTML'' attempts to select a suitable scripting engine. An error generally occurs if the wrong scripting engine is selected. When more than one '''script''' object is used in a document, it can be necessary to specify the ''language'' attribute for each '''script''' object, and doing so is always recommended. The order of the '''script''' objects in a document can also be important, especially if scripting event handlers are assigned to one or more elements in the document. XML is legitimate content for the '''script''' object, but XML is not a scripting language. Therefore, an error can occur if ''MSHTML'' selects an XML data island as the '''script''' object that contains an event handler function. This can happen because ''MSHTML'' selects the first '''script''' object that has the '''language''' attribute defined as the default script block for event handlers. For more information, see the examples.
Windows Internet Explorer 8 and later. The value of the [[html/attributes/src (script)|'''src''']] attribute depends on the current document compatibility mode.
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
*<code>XML Data Islands</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}