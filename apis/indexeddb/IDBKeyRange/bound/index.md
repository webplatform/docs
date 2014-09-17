{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Creates and returns a new key range with lower set to lower, lowerOpen set to lowerOpen, upper set to upper and upperOpen set to upperOpen.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=lower
|Data type=String
|Description=The lower value of the key range.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=upper
|Data type=String
|Description=The upper value of the key range.
|Optional=No
}}{{Method Parameter
|Index=2
|Name=lowerOpen
|Data type=Boolean
|Description=Indicates whether the key range includes the lower value.
|Optional=No
}}{{Method Parameter
|Index=3
|Name=upperOpen
|Data type=Boolean
|Description=Indicates whether the key range includes the upper value.
|Optional=No
}}
|Method_applies_to=apis/indexeddb/IDBKeyRange
|Example_object_name=IDBKeyRange
|Return_value_name=range
|Javascript_data_type=DOM Node
|Return_value_description=A range that can be used for specifying the range of cursors.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var range = new IDBKeyRange.bound(2, 4);
var cursor = store.openCursor(range);
// each value is a contact and each key is the id for that  
// contact whose id is between 2 and 4, both inclusive
|LiveURL=
}}
}}
{{Notes_Section
|Usage=Raises a DOMException when either the lower or upper parameters were not passed a valid key or the lower key is greater than the upper key or the lower key and upper key match and either of the bounds are open.
|Notes=
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkId{{=}}224519 Indexed Database API]
}}
{{Related_Specifications_Section
|Specifications=
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