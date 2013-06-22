{{Page_Title}}
{{Flags
|Content=Examples Needed
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|This method retrieves a '''Node''' using a name. With HTML 4.01 documents, it first searches for a '''Node''' with a matching '''id''' attribute. If it doesn't find one, it then searches for a '''Node''' with a matching '''name''' attribute, but only on those elements that are allowed a '''name''' attribute. With XHTML 1.0 documents, this method only searches for '''Nodes''' with a matching '''id''' attribute. This method is case insensitive in HTML documents and case sensitive in XHTML documents.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=name
|Data type=String
|Description=The name of the Node to be fetched.
|Optional=No
}}
|Method_applies_to=dom/HTMLCollection
|Example_object_name=collection
|Return_value_name=item
|Javascript_data_type=DOM Node
|Return_value_description=The '''Node''' with a '''name''' or '''id''' attribute whose value corresponds to the specified string. Upon failure (e.g., no node with this name exists), returns '''null'''.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
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
{{See_Also_Section}}
{{Topics|DOM, HTML, JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}