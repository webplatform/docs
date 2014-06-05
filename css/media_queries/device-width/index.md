{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The media feature describes the actual width of the output device, such as the entire screen width or the page sheet width.}}
{{CSS_Media_Feature
|Content===Syntax==
* '''device-width: <length>'''
* '''min-device-width: <length>'''
* '''max-device-width: <length>'''

==Values==
'''<length>'''

''Value for the width of the device must be a [[css/data_types/length|length]] value and can not be negative.''
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The first media query describes a device, which has a screen width of exactly 320 pixels. 

The second example describes all screen devices with a screen width of 1024 pixels ans higher. Note: The width of the browser does not matter in this case. Therefore you would have to use [[css/media_queries/width|mediaqueries: width]].

The third media query describes all devices with a screen not wider than 1023 pixels.
|Code=@media screen and ( device-width: 320px ) { … }

@media screen and ( min-device-width: 1024px ) { … }

@media screen and ( max-device-width: 1023px ) { … }
}}
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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}