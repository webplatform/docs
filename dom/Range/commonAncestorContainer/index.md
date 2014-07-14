{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Returns the deepest node in which two boundary points exist.}}
{{API_Object_Property
|Property_applies_to=dom/Range
|Read_only=Yes
|Example_object_name=range
|Return_value_name=rangeAcestor
|Javascript_data_type=DOM Node
|Return_value_description=Node that contains both the Range.startContainer and Range.endContainer nodes.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var range {{=}} document.createRange();

range.setStart(startNode,startOffset);
range.setEnd(endNode,endOffset);
rangeAncestor {{=}} range.commonAncestorContainer;
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
rangeAncestor = range.commonAncestorContainer;
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-range-commonancestorcontainer
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Range.commonAncestorContainer Range.commonAncestorContainer]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974926(v=vs.85).aspx commonAncestorContainer Property]
|HTML5Rocks_link=
}}