{{Page_Title|createObjectURL}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs example
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Creates a URL for the specified object.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=object
|Data type=function
|Description=The object that needs a URL. Usually a [[apis/file/File|File]].
|Optional=No
}}{{Method Parameter
|Index=1
|Name=options
|Data type=DOM Node
|Description=A dictionary object. See [[apis/file/ObjectURLOptions|ObjectURLOptions]] for more information. Used with ''oneTimeOnly'' attribute to create a single use URL that does not need to be revoked.
|Optional=Yes
}}
|Method_applies_to=apis/file/URL
|Example_object_name=URL
|Return_value_name=objectURL
|Javascript_data_type=String
|Return_value_description=A URL for the specified object.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=The URL that is created can be used for resources for use with elements such as '''Image''', '''video''', and '''audio'''.
The object passed in through ''object'' is stored in an internal  hash table.
''oOptions'' is set when you want to only use the URL once. The [[apis/file/ObjectURLOptions|ObjectURLOptions]] object has one property, ''oneTimeOnly'', that is set to ''false'' by default. To set the URL for the object (blob, stream, and so forth) to single use, use the ObjectURLOptions object and set ''oneTimeOnly'' to ''true''. 
To revoke a URL created with  createObjectURL, use [[apis/file/URL/revokeObjectURL|revokeObjectURL]].
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C File API Specification
|URL=http://www.w3.org/TR/FileAPI
|Status=W3C Working Draft
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
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
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