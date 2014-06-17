{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add description, specifications, compatibility.
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The media feature describes the height of the output device's rendering surface, such as the viewport height or the height of the page box.}}
{{CSS_Media_Feature
|Content===Syntax==
* '''height: <length>'''
* '''min-height: <length>'''
* '''max-height: <length>'''

==Values==
'''<length>'''

''Value for the height of the device's viewport must be a [[css/data_types/length|length]] value and can not be negative.''
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The first media query describes a viewport with a height of exactly 480 pixels. Note: The height of the viewport, for example in a smartphone browser is not the same as the height of the screen, because of the browser bars. If you want to describe the screen height, you have to use [[css/media_queries/device-height|mediaqueries: device-height]].

The second example describes viewports with height of 700 pixels and higher. 

The third media query describes all viewports with a height not bigger than 699 pixels.
|Code=@media screen and ( height: 400px ) { … }

@media screen and ( min-height: 700px ) { … }

@media screen and ( max-height: 699px ) { … }
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