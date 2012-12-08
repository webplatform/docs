{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Creates a URL for the specified object.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=object
|Data type=function
|Description=The object that needs a URL. Usually a [[apis/file/File|File]].
|Optional=No
}}{{Method Parameter
|Name=options
|Data type=DOM Node
|Description=An dictionary object. See [[apis/file/ObjectURLOptions|ObjectURLOptions]] for more information. Used with [[apis/file/properties/oneTimeOnly|'''oneTimeOnly''']] attribute to create a single use URL that does not need to be revoked.
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
|Notes=The URL that is created can be used for resources for use with elements such as [[dom/images|'''Image''']], '''video''', and '''audio'''.
The object passed in through ''object'' is stored in an internal  hash table.
''oOptions'' is set when you want to only use the URL once. The [[apis/file/ObjectURLOptions|'''ObjectURLOptions''']] object has one property, [[apis/file/properties/oneTimeOnly|'''oneTimeOnly''']], that is set to '''false''' by default. To set the URL for the object (blob, stream, and so forth)  to single use, use the '''ObjectURLOptions''' object and set '''oneTimeOnly''' to '''true'''. For URLs created for [[apis/file/MSStream|'''MSStream''']] objects, '''oneTimeOnly''' is automatically set to '''true'''.
To revoke a URL created with  '''createObjectURL''', use [[apis/file/methods/revokeObjectURL|'''revokeObjectURL''']].
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
{{See_Also_Section
|Manual_sections=*<code>[[apis/file/methods/revokeObjectURL|revokeObjectURL]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}