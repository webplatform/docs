{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=nilladic function.... no return value...
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Collapses (or removes) a range by moving the insertion point to the beginning or end of the current range.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=toStart
|Data type=Boolean
|Description=Specifies one of the following values: 

true (Default). Moves the insertion point to the beginning of the range.

false Moves the insertion point to the end of the range.
|Optional=Yes
}}
|Method_applies_to=dom/Range
|Example_object_name=range
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var range {{=}} document.createRange();

var referenceNode {{=}} document.getElementsByTagName("div").item(0);
range.selectNode(referenceNode);
range.collapse(true);
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
range.collapse(toStart);
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-range-collapse
|Status=Living Standard
|Relevant_changes=The parameter is now optional and default to false
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Range.collapse Range.collapse]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975439(v=vs.85).aspx collapse Method]
|HTML5Rocks_link=
}}