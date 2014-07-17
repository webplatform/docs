{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns the number of ranges in a selection}}
{{API_Object_Property
|Property_applies_to=dom/Selection
|Read_only=Yes
|Example_object_name=selObj
|Return_value_name=rangecount
|Javascript_data_type=Number
|Return_value_description=The number of ranges in a selection.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var selObj{{=}}window.selection();
var rangecount{{=}}selObj.rangeCount;
}}
}}
{{Notes_Section
|Notes====Remarks===
Windows Internet Explorer 9-11 does not currently support multiple or disjointed selections in standards mode. This property always returns a 1 with a valid selection. It returns a 0 if [[dom/Selection/removeRange|'''removeRange''']] or [[dom/Selection/removeAllRanges|'''removeAllRanges''']] have been applied, though calling [[dom/Selection/isCollapsed|'''isCollapsed''']] is recommended instead to detect an empty range.

Before the user has clicked a freshly loaded page, the rangeCount is 0. A user can normally only select one range at a time, so the rangeCount will usually be 1. Scripting can be used (currently) in Gecko to make the selection contain more than 1 range.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 7.6.1
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Selection.rangeCount Selection.rangeCount]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974693(v=vs.85).aspx rangeCount Property]
|HTML5Rocks_link=
}}