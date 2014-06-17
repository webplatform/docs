{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add description, specifications, compatibility.
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The media feature describes the actual aspect ratio of the output device, such as the aspect ratio of an entire screen or the aspect ratio of a page sheet.}}
{{CSS_Media_Feature
|Content====Syntax===
'''device-aspect-ratio: <ratio>'''

===Values===
'''ratio'''

''Value for the aspect ratio of a device's rendering surface must be a [[css/data_types/ratio|ratio]] value.''
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The example describes all screen devices with a screen aspect ratio of 16:9 or smaller and therefore all widescreens that are 16:9 or wider. Note: The flexible aspect ratio of the browser or any other rendering surface does not matter in this case. Therefore you would have to use [[css/media_queries/width|mediaqueries: aspec-ratio]].
|Code=@media screen and ( max-device-aspect-ratio: 16/9 ) { … }
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