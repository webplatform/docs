{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Returns a number representing where in the Range.endContainer the Range ends.}}
{{API_Object_Property
|Property_applies_to=dom/Range
|Read_only=Yes
|Example_object_name=range
|Return_value_name=offset
|Javascript_data_type=Number
|Return_value_description=the end offset value. 
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var range {{=}} document.createRange();

range.setStart(startNode,startOffset);
range.setEnd(endNode,endOffset);
endRangeOffset {{=}} range.endOffset;
}}
}}
{{Notes_Section
|Notes====Remarks===
If the boundary point offset is within a container that is not a character data node, the offset is a count based on where it falls between child nodes. For example, the offset is 0 if it falls before the first child, and 1 if it is between the first and second child. If the offset is within a character data node container, the value represents 16-bit unit positions.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-range-endoffset
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Range.endOffset Range.endOffset]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974928(v=vs.85).aspx endOffset Property]
|HTML5Rocks_link=
}}