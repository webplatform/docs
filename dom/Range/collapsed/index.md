{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The Range.collapsed read-only property returns a Boolean flag indicating whether the start and end points of the Range are at the same position. It returns true if the start and end boundary points of the Range are the same point in the DOM, false if not.}}
{{API_Object_Property
|Property_applies_to=dom/Range
|Read_only=Yes
|Example_object_name=range
|Javascript_data_type=Boolean
|Return_value_description=true - start and end boundary points of the Range are the same point in the DOM

false - start and end boundary points of the Range are NOT the same point in the DOM
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var range {{=}} document.createRange(); 

range.setStart(startNode,startOffset); 
range.setEnd(endNode,endOffset);
var isCollapsed {{=}} range.collapsed;
}}
}}
{{Notes_Section
|Notes====Remarks===
A collapsed range has its start and end boundary points set to the same value, rendering it empty.
|Import_Notes====Syntax===
isCollapsed = range.collapsed;
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-range-collapsed
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Range.collapsed Range.collapsed]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974925(v=vs.85).aspx collapsed Property]
|HTML5Rocks_link=
}}