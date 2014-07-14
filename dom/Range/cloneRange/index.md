{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Returns a new range with boundary points that are equal to the original range.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Range
|Example_object_name=range
|Return_value_name=clone
|Javascript_data_type=Object
|Return_value_description=[object Range]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var range {{=}} document.createRange();
range.selectNode(document.getElementsByTagName("div").item(0));
var clone {{=}} range.cloneRange();
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
clone = range.cloneRange();
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Range.cloneRange Range.cloneRange]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975438(v=vs.85).aspx cloneRange Method]
|HTML5Rocks_link=
}}