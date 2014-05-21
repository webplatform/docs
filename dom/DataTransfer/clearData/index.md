{{Page_Title}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Removes one or more data formats (or all data) from the clipboard through the '''DataTransfer''' object or the [[dom/ClipboardData|ClipboardData]] object.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=format
|Data type=String
|Description=The format of the data to be cleared, using one of the following values (case insensitve):
*URL
*Text
If ''format'' is omitted, all data is removed.
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
|Description=This example uses the '''clearData''' method, the [[dom/DataTransfer/setData|setData]] method and the [[dom/DataTransfer/getData|getData]] method with the [[dom/DataTransfer|DataTransfer]] object.
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
*For drag-and-drop operations, the '''clearData''' method of the [[dom/DataTransfer|DataTransfer]] object is used generally in source events, such as [[dom/DragEvent/dragstart|dragstart]]. When you override the default behavior of the target, use '''clearData''' in the [[dom/DragEvent/drop|drop]] event. It is particularly useful for selectively removing data formats when multiple formats are specified.
*The clearData() method does not affect whether any files were included in the drag, so the types attribute's list might still not be empty after calling clearData() (it would still contain the "Files" string if any files were included in the drag).
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}