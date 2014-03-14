{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets or sets the caption element of a table.}}
{{API_Object_Property
|Property_applies_to=dom/HTMLTableElement
|Read_only=No
|Example_object_name=table
|Return_value_name=captionElement
|Javascript_data_type=DOM Node
|Return_value_description=The caption element, or null.
|Example_value_name=newCaption
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example sets the inline style for the '''caption''' property.
|Code=document.getElementById("mytable").caption.style.color = "blue";
}}
}}
{{Notes_Section
|Notes=If a table contains multiple captions, this property returns the first one.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 1
|URL=http://www.w3.org/TR/REC-DOM-Level-1/
|Status=Recommendation
|Relevant_changes=Section 2.5.5
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