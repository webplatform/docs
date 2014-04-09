{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Removes mouse capture from the object in the current document.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Document
|Example_object_name=document
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example invokes the '''releaseCapture''' method on the document object.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;title&gt;&lt;/title&gt;
 &lt;/head&gt;
 &lt;body onload{{=}}"oOwnCapture.setCapture();" 
    onclick{{=}}"document.releaseCapture();"&gt;
  &lt;div id{{=}}"oOwnCapture"
    onmousemove{{=}}"oWriteLocation.value {{=}} 
        event.clientX + event.clientY";
    onlosecapture{{=}}"alert(event.srcElement.id + 
        ' has lost mouse capture.')"&gt;
  &lt;textarea id{{=}}"oWriteLocation" cols{{=}}"2"&gt;&lt;/textarea&gt;
  &lt;/div&gt;
  &lt;hr/&gt;
  &lt;div id{{=}}oNoCapture&gt;
   &lt;p&gt;Click the document to invoke the releaseCapture method.&lt;/p&gt;
  &lt;/div&gt;
 &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/releaseCaptureEX.htm
}}
}}
{{Notes_Section
|Notes=*For '''releaseCapture''' to have an effect, you must set mouse capture through the '''setCapture''' method.
*You can invoke the '''releaseCapture''' method on the [[dom/Document|'''Document''']] object.
*The '''releaseCapture''' method makes it unnecessary to determine which element has capture to programmatically release it.
*Other actions that release document capture include displaying a modal dialog box and switching focus to another application or browser window.
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}