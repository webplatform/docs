{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=object|Data type=object|Description=The object that needs a URL. This object may be one of the following types:|Optional=}}
{{Method Parameter|Name=oOptions|Data type=ObjectURLOptions|Description=Used with [[apis/file/properties/oneTimeOnly|'''oneTimeOnly''']] attribute to create a single use URL that does not need to be   revoked.|Optional=}}
|Method_applies_to=dom/Element
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=String

A URL for the specified object.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The URL that is created can be used for resources for use with elements such as [[dom/images|'''Image''']], '''video''', and '''audio'''.
The object passed in through ''object'' is stored in an internal  hash table.
''oOptions'' is set when you want to only use the URL once. The [[apis/file/ObjectURLOptions|'''ObjectURLOptions''']] object has one property, [[apis/file/properties/oneTimeOnly|'''oneTimeOnly''']], that is set to '''false''' by default. To set the URL for the object (blob, stream, and so forth)  to single use, use the '''ObjectURLOptions''' object and set '''oneTimeOnly''' to '''true'''. For URLs created for [[apis/file/MSStream|'''MSStream''']] objects, '''oneTimeOnly''' is automatically set to '''true'''.
To revoke a URL created with  '''createObjectURL''', use [[apis/file/methods/revokeObjectURL|'''revokeObjectURL''']].
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/file/URL|URL]]</code>
*<code>[[apis/file/ObjectURLOptions|ObjectURLOptions]]</code>
*<code>[[apis/file/methods/revokeObjectURL|revokeObjectURL]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}