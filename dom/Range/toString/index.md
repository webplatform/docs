{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Returns the contents of a Range as a string. This string contains only the data characters, no markup.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Range
|Example_object_name=range
|Return_value_name=text
|Javascript_data_type=String
|Return_value_description=Contains only the data characters, no markup.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var range {{=}} document.createRange();

range.selectNode(document.getElementsByTagName("div").item(0));
text {{=}} range.toString();
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
text = range.toString();
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-range-stringifier
|Status=Living Standard
|Relevant_changes=No Change
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Range.toString Range.toString]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh869616(v=vs.85).aspx toString Method]
|HTML5Rocks_link=
}}