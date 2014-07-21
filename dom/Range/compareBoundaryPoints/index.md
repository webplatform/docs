{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The Range.compareBoundaryPoints() method compares the boundary points of the Range with another one.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=how
|Data type=unsigned short
|Description=Specifies how ''sourceRange'' is compared to the range of the object on which '''compareBoundaryPoints''' is invoked.

Must be one of -
Range.END_TO_END (2) compares the end boundary-point of sourceRange to the end boundary-point of Range.

Range.END_TO_START (3) compares the end boundary-point of sourceRange to the start boundary-point of Range.

Range.START_TO_END (1) compares the start boundary-point of sourceRange to the end boundary-point of Range.

Range.START_TO_START (0) compares the start boundary-point of sourceRange to the start boundary-point of Range.
|Optional=No
}}{{Method Parameter
|Name=sourceRange
|Data type=Range
|Description=[[dom/Range|'''Range''']] object that is compared to the range of the object on which '''compareBoundaryPoints''' is invoked.
|Optional=No
}}
|Method_applies_to=dom/Range
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''Integer'''

Returns a –1, 0, or 1 to indicate whether the ''sourceRange'' point is before, equal to, or after the boundary point of the [[dom/Range|'''Range''']] object on which '''compareBoundaryPoints''' is invoked.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var range, sourceRange, compare;
range {{=}} document.createRange();
range.selectNode(document.getElementsByTagName("div")[0]);
sourceRange {{=}} document.createRange();
sourceRange.selectNode(document.getElementsByTagName("div")[1]);
compare {{=}} range.compareBoundaryPoints(Range.START_TO_END, sourceRange);
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-range-compareboundarypoints
|Status=Living Standard
|Relevant_changes=Throws an exception for unexpected `how` value.
}}{{Related Specification
|Name=DOM Level 2 Traversal and Range
|URL=http://www.w3.org/TR/DOM-Level-2-Traversal-Range/ranges.html#Level-2-Range-Comparing
|Status=Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Chrome
|Version=37 and earlier
|Note=Does not throw a NotSupportedError exception when the `how` parameter does not have an expected value.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=any
|Note=Does not throw a NotSupportedError exception when the `how` parameter does not have an expected value.
}}
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Range.compareBoundaryPoints Range.compareBoundaryPoints]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975440(v=vs.85).aspx compareBoundaryPoints Method]
|HTML5Rocks_link=
}}