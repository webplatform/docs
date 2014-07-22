{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs a modern example (viz not JScript).

this should be with Selection object, not textRange.
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Retrieves the parent element for the given text range.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/TextRange
|Example_object_name=textRange
|Return_value_name=parentNode
|Javascript_data_type=DOM Node
|Return_value_description=Returns the parent element object if successful, or null otherwise.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536654(v=vs.85).aspx parentElement Method]
|HTML5Rocks_link=
}}