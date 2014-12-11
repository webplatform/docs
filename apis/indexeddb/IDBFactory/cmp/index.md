{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Proposed Recommendation}}
{{API_Name}}
{{Summary_Section|This method compares two specified keys. Returns 1 if the first key is greater than the second, -1 if the first is less than the second, and 0 if the first is equal to the second.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=first
|Data type=DOM Node
|Description=The first key to compare
|Optional=No
}}{{Method Parameter
|Index=1
|Name=second
|Data type=String
|Description=The second key to compare
|Optional=No
}}
|Method_applies_to=apis/indexeddb/IDBFactory
|Example_object_name=window.indexeddb
|Return_value_name=result
|Javascript_data_type=Number
|Return_value_description=The method returns 1 if the first key is greater than the second, -1 if the first is less than the second, and 0 if the first is equal to the second.
Throws a DOMException (Data Error) is one of the supplied keys was not a valid key.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var value1 {{=}} "Alpha";
var value2 {{=}} "Beta";
var result {{=}} window.indexedDB.cmp( value1, value2 );
console.log( "Comparison results: " + result );
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C IndexedDB Specification
|URL=http://www.w3.org/TR/IndexedDB/
|Status=W3C Proposed Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}