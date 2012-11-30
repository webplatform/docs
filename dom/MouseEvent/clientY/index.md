{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Gets the y-coordinate of the mouse pointer, relative to the upper-left corner of the viewport (that is, the user agent's client area).}}
{{API_Object_Property
|Property_applies_to=dom/objects/MouseEvent
|Read_only=Yes
|Example_object_name=event
|Return_value_name=yCoordinate
|Javascript_data_type=Number
|Return_value_description=The Y coordinate of the mouse cursor.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''clientY''' property to determine the mouse position relative to the window. The console shows the mouse position at all times.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;script&gt;
function logClientCoords() {
  console.log("The x coordinate is: " + e.clientX + "The y coordinate is: " + e.clientY);
}
function logCursorPosition(e) {
  console.log("X = " + e.clientX + " Y = ' + e.clientY);
}
window.addEventListener("move", logCursorPosition, false);
window.addEventListener("click", logClientCoords, false)
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
 &lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes=Client coordinates do not reflect the scroll offset of the page. To get the mouse pointer's coordinates  relative to the upper-left corner of the document, use the  [[css/cssom/properties/pageX|'''pageX''']] and [[css/cssom/properties/pageY|'''pageY''']] properties.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Events
|URL=http://www.w3.org/TR/DOM-Level-3-Events/
|Status=Working Draft
|Relevant_changes=Section 5.2.3
}}
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
*<code>[[dom/objects/DragEvent|DragEvent]]</code>
*<code>[[dom/objects/MouseEvent|MouseEvent]]</code>
*<code>[[dom/objects/MouseWheelEvent|MouseWheelEvent]]</code>
*<code>[[dom/objects/WheelEvent|WheelEvent]]</code>
*<code>Reference</code>
*<code>[[css/cssom/properties/offsetY|offsetY]]</code>
*<code>[[css/cssom/properties/pageY|pageY]]</code>
*<code>[[dom/properties/screenY|screenY]]</code>
*<code>[[css/cssom/properties/y|y]]</code>
}}
{{Topics|DOM, DOMEvents}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}