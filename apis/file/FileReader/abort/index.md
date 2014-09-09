{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=need examples
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Last Call Working Draft}}
{{API_Name}}
{{Summary_Section|The abort method is used to aborts the read operation. Upon return, the [[dom/Element/readyState]] will be ''DONE''.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/file/FileReader
|Example_object_name=FileReader
|Return_value_name=
|Javascript_data_type=void
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var instanceOfFileReader = new FileReader();

// ...read the file...
instanceOfFileReader.abort();
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=The '''abort''' method is used to interrupt an asynchronous  read operation that is in progress on an onloadend event, sets the state of the [[dom/Element/readyState]] property of the FileReader to <code>DONE</code>, and sets result property to <code>null</code>.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C File API Specification
|URL=http://www.w3.org/TR/FileAPI/
|Status=Last Call Working Draft 12 September 2013
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, FileAPI}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/FileReader.abort abort]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh772297(v=vs.85).aspx abort Method]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic Support
|Chrome_supported=Yes
|Chrome_version=22.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=15.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=6.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=Basic Support
|Android_supported=Yes
|Android_version=3.0
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=10.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=6.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}