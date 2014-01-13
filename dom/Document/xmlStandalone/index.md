{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets or sets the value of the '''standalone''' attribute in the declaration of an XML document.}}
{{API_Object_Property
|Property_applies_to=dom/Document
|Read_only=No
|Example_object_name=document
|Return_value_name=isStandalone
|Javascript_data_type=Boolean
|Example_value_name=isStandalone
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=Other
|Description=The following example shows an XML declaration that specifies a value for the '''standalone''' attribute.
|Code=&lt;?xml standalone{{=}}"yes"?&gt;
}}
}}
{{Notes_Section
|Notes=Setting the value of the '''xmlStandalone''' property does not cause an XML document to validate.  Use the [[dom/methods/normalize|'''normalize''']] method instead.
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
*<code>[[dom/Document|Document]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}