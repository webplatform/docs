{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns whether a specific DOM standard is implemented.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=feature
|Data type=String
|Description=The name of the standard. Case insensitive.
|Optional=No
}}{{Method Parameter
|Name=version
|Data type=String
|Description=The version number of the standard.
|Optional=No
}}
|Method_applies_to=dom/implementation
|Example_object_name=implementation
|Return_value_name=featureImplemented
|Javascript_data_type=Boolean
|Return_value_description=Whether the feature is implemented.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example uses the '''hasFeature''' method to test whether the object implements the DOM HTML standard.
|Code=var featureImplemented = document.implementation.hasFeature("HTML", "1.0");
}}
}}
{{Notes_Section
|Notes====Remarks===
The ''bstrfeature'' parameter is case-insensitive.
'''hasFeature''' was introduced in Microsoft Internet Explorer 6.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Cor
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/implementation|implementation]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}