{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Indicates that the enclosed text should not be broken across lines; use the CSS property white-space instead.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''NOBR''' element to prevent text lines from breaking.
|Code=&lt;NOBR&gt;Here's a line of text I don't want to be broken . . . 
here's the end of the line.&lt;/NOBR&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification]


===Members===
The '''noBR''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''noBR''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[dom/events/abort|'''onabort''']]
|Fires when the user aborts the download.
|-
|[[dom/events/afterupdate|'''onafterupdate''']]
|Fires on a databound object after successfully updating the associated data in the data source object.
|-
|[[dom/events/beforeactivate|'''onbeforeactivate''']]
|Fires immediately before the object is set as the [[dom/properties/activeElement|'''active element''']].
|-
|[[dom/events/beforecopy|'''onbeforecopy''']]
|Fires on the source object before the selection is copied to the system clipboard.
|-
|[[dom/events/beforecut|'''onbeforecut''']]
|Fires on the source object before the selection is deleted from the document.
|-
|[[dom/events/beforeeditfocus|'''onbeforeeditfocus''']]
|Fires before an object contained in an editable element enters a ''UI Activation'' state or when an editable container object is ''control selection''.
|-
|[[dom/events/beforepaste|'''onbeforepaste''']]
|Fires on the target object before the selection is pasted from the system clipboard to the document.
|-
|[[dom/events/beforeupdate|'''onbeforeupdate''']]
|Fires on a databound object before updating the associated data in the data source object.
|-
|[[dom/events/cellchange|'''oncellchange''']]
|Fires when data changes in the data provider.
|-
|[[dom/events/change|'''onchange''']]
|Fires when the contents of the object or selection have changed.
|-
|[[dom/events/click|'''onclick''']]
|Fires when the user clicks the left mouse button on the object.
|-
|[[dom/events/contextmenu|'''oncontextmenu''']]
|Fires when the user clicks the right mouse button in the client area, opening the context menu.
|-
|[[dom/events/cut|'''oncut''']]
|Fires on the source element when the object or selection is removed from the document and added to the system clipboard.
|-
|[[dom/events/dataavailable|'''ondataavailable''']]
|Fires periodically as data arrives from data source objects that asynchronously transmit their data.
|-
|[[dom/events/datasetchanged|'''ondatasetchanged''']]
|Fires when the data set exposed by a data source object changes.
|-
|[[dom/events/datasetcomplete|'''ondatasetcomplete''']]
|Fires to indicate that all data is available from the data source object.
|-
|[[dom/events/dblclick|'''ondblclick''']]
|Fires when the user double-clicks the object.
|-
|[[dom/events/drag|'''ondrag''']]
|Fires on the source object continuously during a drag operation.
|-
|[[dom/events/dragend|'''ondragend''']]
|Fires on the source object when the user releases the mouse at the close of a drag operation.
|-
|[[dom/events/dragenter|'''ondragenter''']]
|Fires on the target element when the user drags the object to a valid drop target.
|-
|[[dom/events/dragleave|'''ondragleave''']]
|Fires on the target object when the user moves the mouse out of a valid drop target during a drag operation.
|-
|[[dom/events/dragover|'''ondragover''']]
|Fires on the target element continuously while the user drags the object over a valid drop target.
|-
|[[dom/events/dragstart|'''ondragstart''']]
|Fires on the source object when the user starts to drag a text selection or selected object.
|-
|[[dom/events/drop|'''ondrop''']]
|Fires on the target object when the mouse button is released during a drag-and-drop operation.
|-
|[[dom/events/error|'''onerror''']]
|Fires when an error occurs during object loading.
|-
|[[dom/events/errorupdate|'''onerrorupdate''']]
|Fires on a databound object when an error occurs while updating the associated data in the data source object.
|-
|[[dom/events/filterchange|'''onfilterchange''']]
|Fires when a visual filter changes state or completes a transition.
|-
|[[dom/events/focusin|'''onfocusin''']]
|Fires for an element just prior to setting focus on that element.
|-
|[[dom/events/focusout|'''onfocusout''']]
|Fires for the current element with focus immediately after moving focus to another element.
|-
|[[dom/events/help|'''onhelp''']]
|Fires when the user presses the F1 key while the client is the active window.
|-
|[[dom/events/input|'''oninput''']]
|Occurs when the text content of an element is changed through the user interface.
|-
|[[dom/events/keydown|'''onkeydown''']]
|Fires when the user presses a key.
|-
|[[dom/events/keypress|'''onkeypress''']]
|Fires when the user presses an alphanumeric key.
|-
|[[dom/events/keyup|'''onkeyup''']]
|Fires when the user releases a key.
|-
|[[dom/events/layoutcomplete|'''onlayoutcomplete''']]
|Fires when the print or print preview layout process finishes filling the current LayoutRect object with content from the source document.
|-
|[[dom/events/load|'''onload''']]
|Fires immediately after the client loads the object.
|-
|[[dom/events/losecapture|'''onlosecapture''']]
|Fires when the object loses the mouse capture.
|-
|[[dom/events/mousedown|'''onmousedown''']]
|Fires when the user clicks the object with either mouse button.
|-
|[[dom/events/mouseenter|'''onmouseenter''']]
|Fires when the user moves the mouse pointer into the object.
|-
|[[dom/events/mouseleave|'''onmouseleave''']]
|Fires when the user moves the mouse pointer outside the boundaries of the object.
|-
|[[dom/events/mousemove|'''onmousemove''']]
|Fires when the user moves the mouse over the object.
|-
|[[dom/events/mouseout|'''onmouseout''']]
|Fires when the user moves the mouse pointer outside the boundaries of the object.
|-
|[[dom/events/mouseover|'''onmouseover''']]
|Fires when the user moves the mouse pointer into the object.
|-
|[[dom/events/mouseup|'''onmouseup''']]
|Fires when the user releases a mouse button while the mouse is over the object.
|-
|[[dom/events/mousewheel|'''onmousewheel''']]
|Fires when the wheel button is rotated.
|-
|[[dom/events/paste|'''onpaste''']]
|Fires on the target object when the user pastes data, transferring the data from the system clipboard to the document.
|-
|[[dom/events/propertychange|'''onpropertychange''']]
|Fires when a property changes on the object.
|-
|[[dom/events/readystatechange|'''onreadystatechange''']]
|Fires when the state of the object has changed.
|-
|[[dom/events/reset|'''onreset''']]
|Fires when the user resets a form.
|-
|[[dom/events/resize|'''onresize''']]
|Fires when the size of the object is about to change.
|-
|[[dom/events/rowenter|'''onrowenter''']]
|Fires to indicate that the current row has changed in the data source and new data values are available on the object.
|-
|[[dom/events/rowexit|'''onrowexit''']]
|Fires just before the data source control changes the current row in the object.
|-
|[[dom/events/rowsdelete|'''onrowsdelete''']]
|Fires when rows are about to be deleted from the recordset.
|-
|[[dom/events/rowsinserted|'''onrowsinserted''']]
|Fires just after new rows are inserted in the current recordset.
|-
|[[dom/events/selectstart|'''onselect''']]
|Fires when the current selection changes.
|-
|[[dom/events/select|'''onselectstart''']]
|Fires when the object is being selected.
|}
 

====Methods====
The '''noBR''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|'''addBehavior'''
|Attaches a behavior to the element. 

This method is not supported for Metro style apps using JavaScript.
|-
|[[dom/methods/applyElement|'''applyElement''']]
|Makes the element either a child or parent of another element.
|-
|[[dom/methods/attachEvent|'''attachEvent''']]
|Binds the specified function to an event, so that the function gets called whenever the event fires on the object.
|-
|[[dom/methods/clearAttributes|'''clearAttributes''']]
|Removes all attributes and values from the object.
|-
|[[dom/methods/click|'''click''']]
|Simulates a click by causing the [[dom/events/click|'''onclick''']] event to fire.
|-
|[[dom/methods/componentFromPoint|'''componentFromPoint''']]
|Returns the component located at the specified coordinates via certain events.
|-
|'''contains'''
|Checks whether the given element is contained within the object.
|-
|[[dom/methods/detachEvent|'''detachEvent''']]
|Unbinds the specified function from the event, so that the function stops receiving notifications when the event fires.
|-
|[[dom/methods/doScroll|'''doScroll''']]
|Simulates a click on a scroll bar component.
|-
|[[dom/methods/fireEvent|'''fireEvent''']]
|Fires a specified event on the object.
|-
|[[dom/methods/getAttribute|'''getAttribute''']]
|Retrieves the value of the specified attribute.
|-
|[[dom/methods/getAttributeNode|'''getAttributeNode''']]
|Retrieves an [[dom/attributes|'''attribute''']] object referenced by the '''attribute'''.[[html/attributes/name|'''name''']] property.
|-
|[[dom/methods/getAttributeNodeNS|'''getAttributeNodeNS''']]
|Gets an [[dom/attributes|'''attribute''']] object that matches the specified namespace and name.
|-
|[[dom/methods/getAttributeNS|'''getAttributeNS''']]
|Gets the value of the specified attribute within the specified namespace.
|-
|[[dom/methods/getBoundingClientRect|'''getBoundingClientRect''']]
|Retrieves an object that specifies the bounds of a collection of [[dom/TextRectangle|'''TextRectangle''']] objects.
|-
|[[dom/methods/getClientRects|'''getClientRects''']]
|Retrieves a collection of rectangles that describes the layout of the contents of an object or range within the client. Each rectangle describes a single line.
|-
|[[dom/methods/getElementsByClassName|'''getElementsByClassName''']]
|Gets a collection of objects that are based on the value of the [[dom/properties/className|'''CLASS''']] attribute.
|-
|[[dom/methods/getElementsByTagNameNS|'''getElementsByTagNameNS''']]
|Gets a collection of objects that are based on the specified element names within a specified namespace.
|-
|[[dom/methods/hasAttribute|'''hasAttribute''']]
|Determines whether an attribute with the specified name exists.
|-
|[[dom/methods/hasAttributeNS|'''hasAttributeNS''']]
|Determines whether an attribute that has the specified namespace and name exists.
|-
|[[dom/methods/hasAttributes|'''hasAttributes''']]
|Determines whether one or more attributes exist for the object.
|-
|[[dom/methods/insertAdjacentHTML|'''insertAdjacentHTML''']]
|Inserts the given HTML text into the element at the location.
|-
|[[dom/methods/insertAdjacentText|'''insertAdjacentText''']]
|Inserts the given text into the element at the specified location.
|-
|[[dom/methods/matchesSelector|'''msMatchesSelector''']]
|Determines whether an object matches the specified selector.
|-
|[[dom/methods/normalize|'''normalize''']]
|Merges adjacent DOM objects to produce a normalized document object model.
|-
|[[css/selectors api/querySelector|'''querySelector''']]
|Retrieves the first DOM 
element node from descendants of the starting element node
that match any selector within the supplied selector string.
|-
|[[css/selectors api/querySelectorAll|'''querySelectorAll''']]
|Retrieves all DOM 
element nodes from descendants of the starting element node 
that match any selector within the supplied selector strings.
|-
|[[dom/methods/releaseCapture|'''releaseCapture''']]
|Removes mouse capture from the object in the current document.
|-
|[[dom/methods/removeAttribute|'''removeAttribute''']]
|Removes an attribute from an object.
|-
|[[dom/methods/removeAttributeNode|'''removeAttributeNode''']]
|Removes an [[dom/attributes|'''attribute''']] object from the object.
|-
|[[dom/methods/removeAttributeNS|'''removeAttributeNS''']]
|Removes the specified attribute from the object.
|-
|'''removeBehavior'''
|Detaches a behavior from the element.
|-
|[[dom/methods/replaceAdjacentText|'''replaceAdjacentText''']]
|Replaces the text adjacent to the element.
|-
|[[dom/traversal/methods/scrollIntoView|'''scrollIntoView''']]
|Causes the object to scroll into view, aligning it either at the top or bottom of the window.
|-
|[[dom/methods/setActive|'''setActive''']]
|Sets the object as active without setting focus to the object.
|-
|[[dom/methods/setAttribute|'''setAttribute''']]
|Sets the value of the specified attribute.
|-
|[[dom/methods/setAttributeNode|'''setAttributeNode''']]
|Sets an [[dom/attributes|'''attribute''']] object node as part of the object.
|-
|[[dom/methods/setAttributeNodeNS|'''setAttributeNodeNS''']]
|Sets an [[dom/attributes|'''attribute''']] object as part of the object.
|-
|[[dom/methods/setAttributeNS|'''setAttributeNS''']]
|Sets the value of the specified attribute within the specified namespace.
|-
|[[dom/methods/setCapture|'''setCapture''']]
|Sets the mouse capture to the object that belongs to the current document.
|}
 

====Properties====
The '''noBR''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[html/attributes/ATOMICSELECTION html_attribute|'''ATOMICSELECTION''']]
|Specifies whether the element and its contents must be selected as a whole, indivisible unit.
|-
|[[dom/properties/attributes|'''attributes''']]
|Retrieves a collection of attributes of the object.
|-
|[[dom/properties/canHaveChildren|'''canHaveChildren''']]
|Gets a value indicating whether the object can contain child objects.
|-
|[[dom/properties/canHavedom/canHaveHTML|'''canHaveHTML''']]
|Retrieves the value indicating whether the object can contain rich HTML markup.
|-
|[[dom/properties/className|'''className''']]
|Sets or retrieves the class of the object.
|-
|[[dom/properties/clientHeight|'''clientHeight''']]
|Retrieves the height of the object including padding, but not including margin, border, or scroll bar.
|-
|[[dom/properties/clientLeft|'''clientLeft''']]
|Retrieves the distance between the [[dom/properties/offsetLeft|'''offsetLeft''']] property and the true left side of the client area.
|-
|[[dom/properties/clientTop|'''clientTop''']]
|Retrieves the distance between the [[dom/properties/offsetTop|'''offsetTop''']] property and the true top of the client area.
|-
|[[dom/properties/clientWidth|'''clientWidth''']]
|Retrieves the width of the object including padding, but not including margin, border, or scroll bar.
|-
|[[html/attributes/contentEditable|'''contentEditable''']]
|Sets or retrieves the string that indicates whether the user can edit the content of the object.
|-
|[[html/attributes/dir|'''dir''']]
|Sets or retrieves the reading order of the object.
|-
|[[html/attributes/height|'''height''']]
|Sets or retrieves the height of the object.
|-
|[[html/attributes/id|'''id''']]
|Sets or retrieves the string identifying the object.
|-
|[[dom/properties/innerdom/innerHTML|'''innerHTML''']]
|Sets or retrieves the HTML between the start and end tags of the object.
|-
|[[dom/properties/innerText|'''innerText''']]
|Sets or retrieves the text between the start and end tags of the object.
|-
|[[dom/properties/isContentEditable|'''isContentEditable''']]
|Gets the value that indicates whether the user can edit the contents of the object.
|-
|[[dom/properties/isDisabled|'''isDisabled''']]
|Gets the value that indicates whether the user can interact with the object.
|-
|[[dom/properties/isMultiLine|'''isMultiLine''']]
|Retrieves the value indicating whether the content of the object contains one or more lines.
|-
|[[dom/traversal/properties/isTextEdit|'''isTextEdit''']]
|Retrieves whether a [[dom/traversal/TextRange|'''TextRange''']] object can be created using the object.
|-
|[[html/attributes/lang|'''lang''']]
|Sets or retrieves the language to use.
|-
|[[html/attributes/language|'''language''']]
|Sets or retrieves the language in which the current script is written.
|-
|[[dom/properties/offsetHeight|'''offsetHeight''']]
|Retrieves the height of the object relative to the layout or coordinate parent, as specified by the [[dom/properties/offsetParent|'''offsetParent''']] property.
|-
|[[dom/properties/offsetLeft|'''offsetLeft''']]
|Retrieves the calculated left position of the object relative to the layout or coordinate parent, as specified by the [[dom/properties/offsetParent|'''offsetParent''']] property.
|-
|[[dom/properties/offsetParent|'''offsetParent''']]
|Retrieves a reference to the container object that defines the [[dom/properties/offsetTop|'''offsetTop''']] and [[dom/properties/offsetLeft|'''offsetLeft''']] properties of the object.
|-
|[[dom/properties/offsetTop|'''offsetTop''']]
|Retrieves the calculated top position of the object relative to the layout or coordinate parent, as specified by the [[dom/properties/offsetParent|'''offsetParent''']] property.
|-
|[[dom/properties/offsetWidth|'''offsetWidth''']]
|Retrieves the width of the object relative to the layout or coordinate parent, as specified by the [[dom/properties/offsetParent|'''offsetParent''']] property.
|-
|[[dom/properties/outerdom/outerHTML|'''outerHTML''']]
|Sets or retrieves the object and its content in HTML.
|-
|[[dom/properties/outerText|'''outerText''']]
|Sets or retrieves the text of the object.
|-
|[[dom/traversal/properties/parentElement|'''parentElement''']]
|Retrieves the parent object in the object hierarchy.
|-
|[[dom/traversal/properties/parentTextEdit|'''parentTextEdit''']]
|Retrieves the container object in the document hierarchy that can be used to create a [[dom/traversal/TextRange|'''TextRange''']] containing the original object.
|-
|[[dom/properties/readyState|'''readyState''']]
|Retrieves the current state of the object.
|-
|'''recordNumber'''
|Retrieves the ordinal record from the data set that generated the object.
|-
|[[html/attributes/role|'''role''']]
|Sets or retrieves the role for this element.
|-
|'''scopeName'''
|Gets the namespace defined for the element. 

This property is not supported for Metro style apps using JavaScript.
|-
|[[dom/properties/scrollHeight|'''scrollHeight''']]
|Retrieves the scrolling height of the object.
|-
|[[dom/properties/scrollLeft|'''scrollLeft''']]
|Sets or retrieves the distance between the left edge of the object and the leftmost portion of the content currently visible in the window.
|-
|[[dom/properties/scrollTop|'''scrollTop''']]
|Sets or retrieves the distance between the top of the object and the topmost portion of the content currently visible in the window.
|-
|[[dom/properties/scrollWidth|'''scrollWidth''']]
|Retrieves the scrolling width of the object.
|-
|[[dom/properties/sourceIndex|'''sourceIndex''']]
|Retrieves the ordinal position of the object, in source order, as the object appears in the document's [[dom/properties/all|'''all''']] collection.
|-
|[[dom/properties/tagName|'''tagName''']]
|Retrieves the tag name of the object.
|-
|[[dom/properties/tagUrn|'''tagUrn''']]
|Sets or gets the URN specified in the namespace declaration. 

This property is not supported for Metro style apps using JavaScript.
|-
|[[html/attributes/title|'''title''']]
|Sets or retrieves advisory information (a ToolTip) for the object.
|-
|[[dom/properties/uniqueID|'''uniqueID''']]
|Retrieves an autogenerated, unique identifier for the object.
|-
|[[dom/properties/uniqueNumber|'''uniqueNumber''']]
|Retrieves the element's unique number.
|}
 
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
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}