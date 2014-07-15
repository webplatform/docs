{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Missing code and message properties
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Deprecated}}
{{API_Name}}
{{Summary_Section|Describes errors thrown by selection and range operations.}}
{{API_Object}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Usage=Use [http://docs.webplatform.org/wiki/dom/DOMException DOMException] instead.
|Notes=Starting with Gecko 13.0 (Firefox 13.0 / Thunderbird 13.0 / SeaMonkey 2.10) the Range object throws a DOMException as defined in DOM 4, instead of a RangeException defined in prior specifications.

Gecko supported it up to Gecko 1.9, then removed it until Gecko 17 where it was reimplemented, matching the spec
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13
 
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#interface-range
|Status=Living Standard
|Relevant_changes=Do not use RangeException any more, use DOMExectption instead
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974358(v=vs.85).aspx RangeException Object]
|HTML5Rocks_link=
}}