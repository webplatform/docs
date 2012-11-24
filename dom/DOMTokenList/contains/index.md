{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Gets whether a given class is included within the [[html/attributes/class|class]] of an element.}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=className|Data type=String|Description=The class name to look for.|Optional=}}
|Method_applies_to=dom/DOMTokenList
|Example_object_name=element.classList
|Return_value_name=classExists
|Javascript_data_type=Boolean
|Return_value_description=Whether the given value exists in the list.}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Throws a <code>SyntaxError</code> exception if ''token'' is empty.

Throws an <code>InvalidCharacterError</code> exception if ''token'' contains any spaces.
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
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/DOMTokenList|DOMTokenList]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}