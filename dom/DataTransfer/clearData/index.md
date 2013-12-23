{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Removes one or more data formats from the clipboard through the '''dataTransfer''' object or the [[dom/clipboardData|'''clipboardData''']] object.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=format
|Data type=String
|Description=The format of the data to be cleared, using one of the following values (case insensitve) -
*'''URL'''
*'''Text'''
|Optional=Yes
}}
|Method_applies_to=dom/DataTransfer
|Example_object_name=event.dataTransfer
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''clearData''' method, the [[dom/methods/setData|'''setData''']] method and the [[dom/methods/getData|'''getData''']] method with the [[dom/objects/dataTransfer|'''dataTransfer''']] object.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;script&gt;
var sImageURL, oTarget, oImage;
function initiateDrag(e) {
/*  The setData parameters tell the source object
   to transfer data as a URL and provide the path.  */
  e.dataTransfer.setData("URL", oImage.src);
}
function finishDrag(e) {
  e.dataTransfer.clearData("URL");
  oTarget.textContent = e.dataTransfer.getData("URL");
}
function initialize() {
 oImage = document.getElementById("oImage");
 oTarget = document.getElementbyId("oTarget");
 oImage.addEventListener("dragstart", initiateDrag, false);
 oTarget.addEventListener("dragenter", finishDrag, false);
}
window.addEventListener("load", initialize, false);
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
  &lt;p&gt;This example demonstrates how to use the setData and getData methods of the dataTransfer object to enable the source path of the image to be dragged. Since we are clearing the data, dragging over the target will show "null" instead.&lt;/p&gt;
  &lt;img id{{=}}"oImage" src{{=}}"/workshop/graphics/black.png" width="20" height="20" alt="Black"&gt;
  &lt;span id{{=}}"oTarget"&gt;
    Drop the image here
  &lt;/span&gt;
 &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clearDataEX.htm
}}
}}
{{Notes_Section
|Notes=*If no ''format'' parameter is passed, all of the data formats are cleared.
*For drag-and-drop operations, the '''clearData''' method of the [[dom/objects/dataTransfer|'''dataTransfer''']] object is used generally in source events, such as [[dom/events/dragstart|'''ondragstart''']]. When you override the default behavior of the target, use '''clearData''' in the [[dom/events/drop|'''ondrop''']] event. It is particularly useful for selectively removing data formats when multiple formats are specified.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html5/
|Status=Working Draft
|Relevant_changes=Section 7.7
}}{{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage
|Status=Living Standard
|Relevant_changes=Section 7.7
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
*<code>[[dom/clipboardData|clipboardData]]</code>
*<code>[[dom/methods/getData|getData]]</code>
*<code>[[dom/methods/setData|setData]]</code>
}}
{{Topics|DOM, DOMEvents}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}