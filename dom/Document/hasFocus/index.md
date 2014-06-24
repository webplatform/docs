{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs compat tables
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Document
|Example_object_name=document
|Return_value_name=boolean
|Javascript_data_type=Boolean
|Return_value_description=Returns true if the document has focus, otherwise returns false
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to use the '''hasFocus''' method to determine if the [[dom/Document|Document]] has focus.
|Code=&lt;HTML&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/callerWithHasFocusEX1.html
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html5/editing.html#dom-document-hasfocus
|Status=Candidate Recommendation
|Relevant_changes=Defined here
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