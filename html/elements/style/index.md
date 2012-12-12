{{Page_Title}}
{{Flags
|High-level issues=Merge Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Defines style information for an HTML document.}}
{{Markup_Element
|DOM_interface=dom/HTMLStyleElement
|Content={{Editorial/Merge_Candidate
|Other=Meta:HTML/Elements/style
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example encloses style declarations in the '''STYLE''' element and changes one of those settings using the '''style''' object.
|Code=&lt;HEAD&gt;
&lt;STYLE&gt;
   BODY {  background-color: white; color: black;  }
   H1 {  font: 8pt Arial bold;  }
   P  {  font: 10pt Arial; text-indent: 0.5in;  }
   A  {  text-decoration: none; color: blue;  }
&lt;/STYLE&gt;
&lt;SCRIPT&gt;
    oParagraph.style.fontSize {{=}} 14;
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;P&gt;Sample Paragraph Text&lt;/P&gt;
&lt;/BODY&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''STYLE''' element should appear in the '''HEAD''' section of an HTML document. Microsoft Internet Explorer 4.0 and later permit multiple style blocks.

The '''STYLE''' element should appear in the '''HEAD''' section of an HTML document. Multiple style blocks are permitted.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 14.2.3


===Members===
The '''style''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''style''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[dom/events/abort|'''onabort''']]
|Fires when the user aborts the download.
|-
|[[dom/events/change|'''onchange''']]
|Fires when the contents of the object or selection have changed.
|-
|[[dom/events/error|'''onerror''']]
|Fires when an error occurs during object loading.
|-
|[[dom/events/input|'''oninput''']]
|Occurs when the text content of an element is changed through the user interface.
|-
|[[dom/events/load|'''onload''']]
|Fires immediately after the client loads the object.
|-
|[[dom/events/readystatechange|'''onreadystatechange''']]
|Fires when the state of the object has changed.
|-
|[[dom/events/reset|'''onreset''']]
|Fires when the user resets a form.
|-
|[[dom/events/selectstart|'''onselect''']]
|Fires when the current selection changes.
|}
 

====Methods====
The '''style''' object has these methods.
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
|[[dom/methods/dragDrop|'''dragDrop''']]
|Initiates a drag event.
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
|[[dom/methods/hasAttributeNS|'''hasAttributeNS''']]
|Determines whether an attribute that has the specified namespace and name exists.
|-
|[[dom/methods/matchesSelector|'''msMatchesSelector''']]
|Determines whether an object matches the specified selector.
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
The '''style''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/canHaveChildren|'''canHaveChildren''']]
|Gets a value indicating whether the object can contain child objects.
|-
|[[dom/properties/constructor|'''constructor''']]
|Returns a reference to the constructor of an object.
|-
|[[html/attributes/disabled|'''disabled''']]
|Sets or retrieves a value that indicates whether the user can interact with the object.
|-
|[[html/attributes/id|'''id''']]
|Sets or retrieves the string identifying the object.
|-
|[[css/cssom/properties/media|'''media''']]
|Sets or retrieves the media type.
|-
|'''scopeName'''
|Gets the namespace defined for the element. 

This property is not supported for Metro style apps using JavaScript.
|-
|[[css/cssom/properties/sheet|'''sheet''']]
|Gets the CSS style sheet that is associated with the object.
|-
|[[css/cssom/properties/styleSheet|'''styleSheet''']]
|Retrieves an interface pointer that provides access to the style sheet object's properties and methods.
|-
|[[dom/properties/tagUrn|'''tagUrn''']]
|Sets or gets the URN specified in the namespace declaration. 

This property is not supported for Metro style apps using JavaScript.
|-
|[[css/cssom/style/type|'''type''']]
|Retrieves the CSS language in which the style sheet is written.
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