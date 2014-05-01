{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Gets the data in the specified format from the clipboard through the '''DataTransfer''' object or the [[dom/clipboardData|'''clipboardData''']] object.
If there is no data, returns an empty string.
}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=format
|Data type=String
|Description=The format of the data to be transferred, using one of the following values (case insensitve) -
*'''URL'''
*'''Text'''
|Optional=No
}}
|Method_applies_to=dom/DataTransfer
|Example_object_name=event.dataTransfer
|Return_value_name=eventData
|Javascript_data_type=String
|Return_value_description=Returns the data in the format retrieved from the clipboard/drag and drop operation through the [[dom/DataTransfer|'''DataTransfer''']] object or the [[dom/clipboardData|'''clipboardData''']] object. Depending on the information contained in [[dom/DataTransfer/setData|'''setData''']], this variable can get a path to an image, text, or an anchor URL.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''getData''' method and the [[dom/DataTransfer/setData|'''setData''']] method with the [[dom/DataTransfer|'''DataTransfer''']] object to create a shortcut to an image.
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
{{Notes_Section
|Notes=*The '''getData''' method enforces cross-frame security and allows data transfers only in the same domain. To the user, this means that a selection that is dragged between different security protocols, such as HTTP and HTTPS, fails. In addition, that a selection that is dragged between two instances of the application with different security levels, where the first instance is set to medium and the second is set to high, fails. Finally, that a selection that is dragged into the application from another drag-enabled application, such as Microsoft Word, also fails.
*To use the '''getData''' method to get data from the clipboard in the '''oncopy''' event or the '''oncut''' event, you must call [[dom/Event/preventDefault|event.preventDefault()]] in the event handler script.
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
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}