{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=pfFocus|Data type=VARIANT_TRUE|Description=|Optional=}}
|Method_applies_to=dom/Document
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Boolean

Boolean

Boolean

Document has focus.

Document does not have focus.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to use the '''hasFocus''' method to determine if the [[dom/document|'''document''']] has focus.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/callerWithHasFocusEX1.html
|Code=
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;SCRIPT&gt;
function fnCallDialog()                                             
{
 showModelessDialog("myDialogHasFocus.htm",window,"status:false;dialogWidth:300px;dialogHeight:300px");
}
// Function displays the message DIV when the main document has focus
function fnOpenMessage()
{
	if (document.hasFocus())
	{
		oMessageDiv.style.display {{=}} "block";
	}
}
function fnCloseMessage()
{
	oMessageDiv.style.display {{=}} "none";
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;INPUT TYPE{{=}}"button" 
VALUE{{=}}"Display Modeless Dialog" onclick{{=}}"fnCallDialog()"&gt;
&lt;P&gt;
&lt;SPAN STYLE{{=}} "color:darkmagenta;font-size:large;" onmouseout{{=}}"fnCloseMessage();" 
onmouseover{{=}}"fnOpenMessage();"&gt;Mouse over this!&lt;/SPAN&gt;
&lt;div id{{=}}"oMessageDiv" style{{=}}"display:none;width:200;font-family: 
arial;font-size:large; color: steelblue; border: 4 solid gold;"&gt;
A message for you!
&lt;/div&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;	

}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}