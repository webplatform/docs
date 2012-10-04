{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Topics|HTML}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''WBR''' element to create line breaks. In contrast, the '''NOBR''' element does not break lines.
|LiveURL=
|Code=
&lt;NOBR&gt;This line of text will not break, no matter how narrow the window gets.&lt;/NOBR&gt;
&lt;NOBR&gt;This one, however,&lt;WBR&gt; will break after the word "however," 
if the window gets small enough.&lt;/NOBR&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
A soft line break is a point inside a '''NOBR''' section at which a line break is permitted but not required.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification] (Obsolete)


===HTML information===
{| class="wikitable"
|-
!Closing Tag
|forbidden
|-
!CSS Display
|
|}

===Members===
The '''wbr''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''wbr''' object has these events.
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
|[[dom/events/beforecopy|'''onbeforecopy''']]
|Fires on the source object before the selection is copied to the system clipboard.
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
|[[dom/events/dataavailable|'''ondataavailable''']]
|Fires periodically as data arrives from data source objects that asynchronously transmit their data.
|-
|[[dom/events/datasetchanged|'''ondatasetchanged''']]
|Fires when the data set exposed by a data source object changes.
|-
|[[dom/events/datasetcomplete|'''ondatasetcomplete''']]
|Fires to indicate that all data is available from the data source object.
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
|[[dom/events/input|'''oninput''']]
|Occurs when the text content of an element is changed through the user interface.
|-
|[[dom/events/layoutcomplete|'''onlayoutcomplete''']]
|Fires when the print or print preview layout process finishes filling the current LayoutRect object with content from the source document.
|-
|[[dom/events/load|'''onload''']]
|Fires immediately after the client loads the object.
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
|}
 

====Methods====
The '''wbr''' object has these methods.
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
|[[dom/methods/clearAttributes|'''clearAttributes''']]
|Removes all attributes and values from the object.
|-
|[[dom/methods/componentFromPoint|'''componentFromPoint''']]
|Returns the component located at the specified coordinates via certain events.
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
|[[dom/methods/matchesSelector|'''msMatchesSelector''']]
|Determines whether an object matches the specified selector.
|-
|[[dom/methods/normalize|'''normalize''']]
|Merges adjacent DOM objects to produce a normalized document object model.
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
The '''wbr''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
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
|[[html/attributes/id|'''id''']]
|Sets or retrieves the string identifying the object.
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
|[[html/attributes/role|'''role''']]
|Sets or retrieves the role for this element.
|-
|'''scopeName'''
|Gets the namespace defined for the element. 

This property is not supported for Metro style apps using JavaScript.
|-
|[[dom/properties/tagUrn|'''tagUrn''']]
|Sets or gets the URN specified in the namespace declaration. 

This property is not supported for Metro style apps using JavaScript.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>br</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}