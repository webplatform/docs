{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The method compares two specified keys. 
The method returns 1 if the first key is greater than the second, -1 if the first is less than the second, and 0 if the first is equal to the second.
}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=first
|Data type=DOM Node
|Description=The first key to compare
|Optional=No
}}{{Method Parameter
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
|Code=var value1 {{=}} "Alpha";
var value2 {{=}} "Beta";
var result {{=}} window.indexedDB.cmp( value1, value2 );
console.log( "Comparison results: " + result );
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]
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
*<code>[[apis/indexedDB/properties/indexedDB|indexedDB]]</code>
*<code>[[apis/indexedDB/IDBFactory|IDBFactory]]</code>
}}
{{Topics|API, IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}