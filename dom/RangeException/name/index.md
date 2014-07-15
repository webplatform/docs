{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Deprecated}}
{{API_Name}}
{{Summary_Section|Returns a DOMString value that is the name of the error that occurred during a Range operation.}}
{{API_Object_Property
|Property_applies_to=dom/RangeException
|Read_only=Yes
|Example_object_name=rangeException
|Return_value_name=sErrName
|Javascript_data_type=String
|Return_value_description=The name of the specific RangeException that occured. 
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Range exception also supports a code value. The following table shows the code associated with the specific RangeException:
{{{!}} class="wikitable"
{{!}}-
!Code value
!Name value
{{!}}-
{{!}}1
{{!}}BadBoundarypointsError
{{!}}-
{{!}}2
{{!}}InvalidNodeTypeError
{{!}}}
 
|Import_Notes====Syntax===
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#interface-range
|Status=Living Standard
|Relevant_changes=Do not use RangeException anymore, use DOMException instead.
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}