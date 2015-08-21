{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add description, specifications, compatibility.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
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
|Specifications={{Related Specification
|Name=Media Queries Level 4
|URL=http://www.w3.org/TR/mediaqueries-4/
|Status=Working Draft
}}{{Related Specification
|Name=Media Queries
|URL=http://www.w3.org/TR/css3-mediaqueries/
|Status=Recommendation
}}
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}