{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Gets the arguments that are specified when [[dom/HTMLElement/showModalDialog|showModalDialog]] or [[dom/HTMLElement/showModelessDialog|showModelessDialog]] are called.}}
{{API_Object_Property
|Property_applies_to=dom/WindowModal
|Read_only=No
|Example_object_name=window
|Return_value_name=arguments
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example shows how to get information passed into a modal dialog window by using the '''dialogArguments''' property. The code corresponds to two different files. One file launches the modal window and the other file stores the code for the modal window.

This file launches the modal window and then sends an object to that modal window.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;script&gt;
function fnLaunch() {
    var aForm;
    aForm {{=}} document.getElementById("oForm").elements;
    var myObject {{=}} {};
    myObject.firstName {{=}} aForm.oFirstName.value;
    myObject.lastName {{=}} aForm.oLastName.value;
	// The object "myObject" is sent to the modal window.
    window.showModalDialog("modalDialogSource.htm", myObject, "dialogHeight:300px; dialogLeft:200px;"); 
}
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
  &lt;button onclick{{=}}"fnLaunch();"&gt;Launch The Dialog&lt;/button&gt;
  &lt;form id{{=}} "oForm"&gt;
   First Name:
   &lt;input type{{=}}"text" name{{=}}"oFirstName" value{{=}}"Jane"&gt;
   &lt;br/&gt;
   Last Name:
   &lt;input type{{=}}"text" name{{=}}"oLastName" value{{=}}"Smith"&gt;
  &lt;/form&gt;
 &lt;/body&gt;
&lt;/html&gt;
}}{{Single Example
|Language=HTML
|Description=This file (modalDialogSource.htm), stores the code for the modal window. Get the object sent to this modal window by using the '''dialogArguments''' property.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;script&gt;
var oMyObject {{=}} window.dialogArguments;
var sFirstName {{=}} oMyObject.firstName;
var sLastName {{=}} oMyObject.lastName;
  &lt;/script&gt;
  &lt;title&gt;Untitled&lt;/title&gt;
 &lt;/head&gt;
 &lt;body style{{=}}"font-family: arial; font-size: 14pt; color: Snow; 
background-color: RosyBrown;"&gt;
  First Name:
  &lt;span style{{=}}"color:#00ff7f"&gt;
   &lt;script&gt;
document.write(sFirstName);
   &lt;/script&gt;
  &lt;/span&gt;
  &lt;br/&gt;
  Last Name:
  &lt;span style{{=}}"color:#00ff7f"&gt;
   &lt;script&gt;
document.write(sLastName);
   &lt;/script&gt;
  &lt;/span&gt;
 &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/dialogArgumentsCallerEX1.htm
}}
}}
{{Notes_Section
|Notes=This property applies only to windows that are created with the [[dom/HTMLElement/showModalDialog|'''showModalDialog''']] method and the [[dom/HTMLElement/showModelessDialog|'''showModelessDialog''']] method.
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