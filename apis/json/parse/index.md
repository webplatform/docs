{{Page_Title|JSON.parse}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Parse a JSON string to a JavaScript object.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=json string
|Data type=String
|Description=A JSON string.
|Optional=No
}}
|Method_applies_to=apis/json
|Example_object_name=JSON
|Return_value_name=
|Javascript_data_type=
|Return_value_description=A JavaScript object representing the JSON string.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=
|Code=var json = '{"result":true,"count":1}',
    obj = JSON && JSON.parse(json)
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=This method will throw an error if the argument is not a valid JSON string. You should wrap the parse call in a try/catch block.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}