{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the value of a content attribute.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=name
|Data type=String
|Description=The name of the attribute.
|Optional=No
}}{{Method Parameter
|Name=value
|Data type=String
|Description=The value of the attribute.
|Optional=No
}}
|Method_applies_to=dom/Element
|Example_object_name=element
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=*The attribute will be created, if it is not already present.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Document Object Model (DOM) Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.4
}}{{Related Specification
|Name=Document Object Model (DOM) Level 2 Core
|URL=http://www.w3.org/TR/DOM-Level-2-Core/
|Status=Recommendation
|Relevant_changes=Section 1.2
}}{{Related Specification
|Name=Document Object Model (DOM) Level 1
|URL=http://www.w3.org/TR/REC-DOM-Level-1
|Status=Recommendation
|Relevant_changes=Section 1.2
}}{{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/
|Status=Living Standard
|Relevant_changes=Section 6.8
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=7 and earlier
|Note=The '''name''' parameter requires the name of the desired DOM attribute ("className", for example) and not the content attribute ("class").
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=7 and earlier
|Note=There is an optional '''flag''' parameter that accepts one of the following values - <code>0</code> (default) - case insensitive attribute name. <code>1</code> - case sensitive attribute name.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=7 and earlier
|Note=The '''name''' parameter value is case sensitive by default.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=7 and earlier
|Note=The '''value''' parameter should be converted to string beforehand, or else using [[dom/Element/getAttribute|getAttribute]] might result in a number or a boolean value.
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/Element/removeAttribute|removeAttribute]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}