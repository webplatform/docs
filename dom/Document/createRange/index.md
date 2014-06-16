{{Page_Title}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Creates an empty [[dom/Range|'''Range''']] instance object that has both of its boundary points positioned at the beginning of the document. After a Range is created, you must set its starting and ending boundary points before you can make use of most of its methods.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Document
|Example_object_name=document
|Return_value_name=range
|Javascript_data_type=DOM Node
|Return_value_description=An empty [[dom/Range|'''Range''']] instance object.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//create a document range
var myRange = document.createRange();
//set starting and ending boundaries using predefined objects and variables
myRange.setStart(startNode, startOffset);
myRange.setEnd(endNode, endOffset);

}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 Traversal and Range
|URL=http://www.w3.org/TR/DOM-Level-2-Traversal-Range/
|Status=Recommendation
|Relevant_changes=Section 1.2
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
|MDN_link=https://developer.mozilla.org/en-US/docs/DOM/Document.createRange
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}