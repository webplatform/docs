{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=needs example
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies the number of bytes downloaded since the beginning of the operation.}}
{{API_Object_Property
|Property_applies_to=dom/ProgressEvent
|Read_only=Yes
|Javascript_data_type=unsigned long
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Used to calculate the percentage completed of an operation.
|Notes====Remarks===
This property refers to the content associated with the operation; it  does not account for headers or other overhead associated with the operation.
If the operation specifies content encoding or transfer encoding, the value of this property reflects the specified encoding.
|Import_Notes====Syntax===
value = ProgressEvent.loaded
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/ProgressEvent.loaded ProgressEvent.loaded]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh772355(v=vs.85).aspx loaded Property]
|HTML5Rocks_link=
}}