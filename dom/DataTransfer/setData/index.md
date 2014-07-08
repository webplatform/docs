{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Adds data in a specified format to the '''DataTransfer''' object or the [[dom/ClipboardData|'''ClipboardData''']] object.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=format
|Data type=String
|Description=The format of the data to be transferred, using one of the following values (case insensitve):
*URL
*Text
|Optional=No
}}{{Method Parameter
|Index=1
|Name=data
|Data type=String
|Description=Specifies the data supplied by the source object. This information can be descriptive text, a source path to an image, or a URL for an anchor. When you pass "URL" as the ''format'' parameter, you must use the ''data'' parameter to provide the location of the object that is transferred.
|Optional=No
}}
|Method_applies_to=dom/DataTransfer
|Example_object_name=event.dataTransfer
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''setData''' method and the [[dom/DataTransfer/getData|'''getData''']] method with the [[dom/DataTransfer|'''DataTransfer''']] object to create a shortcut to an image.
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
/*  The parameter passed to getData tells the target
    object what data format to expect.  */
  sImageURL = e.dataTransfer.getData("URL");
  oTarget.textContent = sImageURL;
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
  &lt;p&gt;This example demonstrates how to use the setData and getData methods of the dataTransfer object to enable the source path of the image to be dragged.&lt;/p&gt;
  &lt;img id{{=}}"oImage" src{{=}}"/workshop/graphics/black.png" width="20" height="20" alt="Black"&gt;
  &lt;span id{{=}}"oTarget"&gt;
    Drop the image here
  &lt;/span&gt;
 &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setDataEX.htm
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/editing.html
|Status=Candidate Recommendation
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