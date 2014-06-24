{{Page_Title}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Returns the focus state of the current document, <code>true</code> if the document has focus, <code>false</code> if not.}}
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
|Description=The following example shows how to use the '''hasFocus''' method to determine if the document has focus. If you mouse over the text when the document has focus, "A message for you!" appears; if you mouse over the text when the document does not have focus, the message does not appear.
|Code=<!DOCTYPE HTML>
<html>
<head>
<script>
// Function displays the message DIV when the main document has focus
function fnOpenMessage()
{
	if (document.hasFocus())
	{
		oMessageDiv.style.display = "block";
	}
}
function fnCloseMessage()
{
	oMessageDiv.style.display = "none";
}
</script>
</head>
<body>
<nowiki>
<p>
<span style= "color:darkmagenta;font-size:large;" onmouseout="fnCloseMessage();" 
onmouseover="fnOpenMessage();">Mouse over this!</span>
</p>

<div id="oMessageDiv" style="display:none; font-family:arial; width:200px; font-size:large; color:steelblue; border:4px solid gold;">
A message for you!
</div>
</nowiki>
</body>
</html>
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