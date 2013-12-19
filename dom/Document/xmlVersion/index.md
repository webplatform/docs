{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets or sets the '''version''' attribute that is specified in the declaration of an XML document.}}
{{API_Object_Property
|Property_applies_to=dom/Document
|Read_only=No
|Example_object_name=document
|Return_value_name=version
|Javascript_data_type=String
|Return_value_description=The XML '''version''' of document.
|Example_value_name=newVersion
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=Other
|Description=The following code example shows an XML declaration that specifies a values for the '''version''' attribute.
|Code=&lt;?xml version{{=}}"1.0"?&gt;
}}
}}
{{Notes_Section
|Notes=Applications should use the [[dom/methods/normalize|'''normalize''']] method after  they change the '''xmlVersion''' property.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407
|Status=Recommendation
|Relevant_changes=Section 1.4
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
*<code>[[dom/document|document]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}