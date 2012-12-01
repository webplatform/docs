{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Gets the x-coordinate of the mouse cursor, relative to the target node.}}
{{API_Object_Property
|Property_applies_to=dom/objects/MouseEvent
|Read_only=Yes
|Example_object_name=event
|Return_value_name=xCoordinate
|Javascript_data_type=Number
|Return_value_description=The X coordinate of the mouse cursor.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''offsetX''' property to determine the mouse position relative to the container that fired the event, and also displays the mouse coordinates in the console.
|Code=&lt;!doctype htmk&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;style&gt;
#div {
  position:absolute;
  top:200px;
  left:300px;
}
  &lt;/style&gt;
  &lt;script&gt;
function offsetCoords(e) {
  var offsetInfo = ""
  offsetInfo = "The x coordinate is: " + e.offsetX + "\n"
  offsetInfo += "The y coordinate is: " + e.offsetY + "\r"
  console.log(offsetInfo);
}
function logCoords(e) {
  console.log("X = " + e.offsetX + " Y = " + e.offsetY);
}
function initialize() {
  document.body.addEventListener("mousemove", logCoords, false);
  document.body.addEventListener("click", offsetCoords, false);
  document.getElementById("div").addEventListener("click", offsetCoords, false);
}
window.addEventListener("load", initialize, false);
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
  &lt;div id="div"&gt;
  &lt;/div&gt;
 &lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes=Offset coordinates include the padding of an element, but not its margin or border.
|Import_Notes={{TODO|Check that this is correct.}}
The coordinates match the [[dom/properties/offsetLeft|'''offsetLeft''']] and [[dom/properties/offsetTop|'''offsetTop''']] properties of the object. Use [[dom/properties/offsetParent|'''offsetParent''']] to find the container object that defines this coordinate system.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSSOM View
|URL=http://www.w3.org/TR/cssom-view/
|Status=Working Draft
|Relevant_changes=Section 9
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
|Topic_clusters=CSSOM
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/objects/DragEvent|DragEvent]]</code>
*<code>[[dom/objects/MouseWheelEvent|MouseWheelEvent]]</code>
*<code>[[dom/objects/WheelEvent|WheelEvent]]</code>
*<code>Reference</code>
*<code>[[dom/properties/clientX|clientX]]</code>
*<code>[[css/cssom/properties/pageX|pageX]]</code>
*<code>[[dom/properties/screenX|screenX]]</code>
*<code>x</code>
}}
{{Topics|DOM, DOMEvents}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}