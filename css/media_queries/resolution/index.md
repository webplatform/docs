{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The media feature describes the resolution (pixel-density) of the output device. The resolution can be specified in dpi (dots per inch), dppx (dots per pixel) or dpcm (dots per centimeter).}}
{{CSS_Media_Feature
|Content===Syntax==
# '''resolution: <resolution>'''
# '''min-resolution: <resolution>'''
# '''max-resolution: <resolution>'''

==Values==
'''resolution'''

Value for the resolution of a device must be a [[css/data_types/resolution|resolution]] value.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The first media query describes a non-screen devices with a minimum resolution of 300 dots per inch.

The second example describes a device with a screen that has a pixel-density of 2 or higher.
|Code=@media print and (min-resolution: 300dpi) { ... }

@media screen and (min-resolution: 2dppx) { ... }
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