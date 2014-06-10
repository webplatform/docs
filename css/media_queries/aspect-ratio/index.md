{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The media feature describes the aspect ratio of the output device's rendering surface, such as the viewport aspect ratio or the aspect ratio of the page box.}}
{{CSS_Media_Feature
|Content===Syntax==

# '''aspect-ratio: <ratio>'''
# '''min-aspect-ratio: <ratio>'''
# '''max-aspect-ratio: <ratio>'''

==Values==

'''ratio'''

''Value for the aspect ratio of a device's rendering surface must be a [[css/data_types/ratio|ratio]] value.''
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example describes a viewport with a minimum aspect ratio of 1. This describes all viewports, which are quadratic or have a landscape ratio. Note: The aspect ratio of the viewport must not be the same as the aspect ratio of the screen. If you want to describe the aspect ratio of the screen, you have to use [[css/media_queries/device-aspect-ratio|device-aspect-ratio]].
|Code=@media screen and (min-aspect-ratio: 1/1) { ... }
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