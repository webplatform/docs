{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/Element
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to get information passed into a modal dialog window by using the '''dialogArguments''' property. The code corresponds to two different files. One file launches the modal window and the other file stores the code for the modal window.


|LiveURL=This file launches the modal window and then sends an object to that modal window.
|Code=
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;SCRIPT&gt;
function fnLaunch()
{
    var aForm;
    aForm {{=}} oForm.elements;
    var myObject {{=}} new Object();
    myObject.firstName {{=}} aForm.oFirstName.value;
    myObject.lastName {{=}} aForm.oLastName.value;
	// The object "myObject" is sent to the modal window.
    window.showModalDialog("modalDialogSource.htm", myObject, "dialogHeight:300px; dialogLeft:200px;"); 
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;BUTTON onclick{{=}}"fnLaunch();" &gt;Launch The Dialog&lt;/BUTTON&gt;
&lt;FORM ID{{=}} "oForm"&gt;
First Name:
&lt;INPUT TYPE{{=}}"text" NAME{{=}}"oFirstName" VALUE{{=}}"Jane"&gt;
&lt;BR&gt;
Last Name:
&lt;INPUT TYPE{{=}}"text" NAME{{=}}"oLastName" VALUE{{=}}"Smith"&gt;
&lt;/FORM&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;

}}
{{Single_Example
|Description=This file (modalDialogSource.htm), stores the code for the modal window. Get the object sent to this modal window by using the '''dialogArguments''' property.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/dialogArgumentsCallerEX1.htm
|Code=
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;SCRIPT&gt;
var oMyObject {{=}} window.dialogArguments;
var sFirstName {{=}} oMyObject.firstName;
var sLastName {{=}} oMyObject.lastName;
&lt;/SCRIPT&gt;
	&lt;title&gt;Untitled&lt;/title&gt;
&lt;/head&gt;
&lt;BODY STYLE{{=}}"font-family: arial; font-size: 14pt; color: Snow; 
background-color: RosyBrown;"&gt;

First Name:
&lt;SPAN STYLE{{=}}"color:00ff7f"&gt;
&lt;SCRIPT&gt;
document.write(sFirstName);
&lt;/SCRIPT&gt;
&lt;/SPAN&gt;
&lt;BR&gt;
Last Name:
&lt;SPAN STYLE{{=}}"color:00ff7f"&gt;
&lt;SCRIPT&gt;
document.write(sLastName);
&lt;/SCRIPT&gt;
&lt;/SPAN&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;

}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''dialogArguments''' property applies only to windows that are created with the [[dom/methods/showModalDialog|'''showModalDialog''']] method and the [[dom/methods/showModelessDialog|'''showModelessDialog''']] method.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>window</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}