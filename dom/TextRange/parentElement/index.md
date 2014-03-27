{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/TextRange
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLElement'''

null
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''parentElement''' method to retrieve the parent element for the text range created from the current selection, and display the tag name of the element.
|Code=&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
var sel {{=}} document.selection;
var rng {{=}} sel.createRange();
var el {{=}} rng.parentElement();
alert(el.tagName);
&lt;/SCRIPT&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The parent element is the element that completely encloses the text in the range.
If the text range spans text in more than one element, this method returns the smallest element that encloses all the elements. When you insert text into a range that spans multiple elements, the text is placed in the parent element rather than in any of the contained elements.
This feature might not be available on non-Microsoft Win32 platforms.
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