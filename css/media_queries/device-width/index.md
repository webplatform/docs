{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add description, specifications, compatibility.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The media feature describes the actual width of the output device, such as the entire screen width or the page sheet width.}}
{{CSS_Media_Feature
|Content=On all mobile browsers, the device-width media query uses the value of screen.width. Originally, that property held the width of the screen in device pixels, but on an increasing number of mobile browser it instead holds the width of the ideal viewport (the one that you get when you use the [[tutorials/mobile_viewport|meta viewport tag]]). Unfortunately it's impossible to tell which value is returned without resorting to a browser detect.

Since screen.width and the device-width media query are unreliable on mobile browsers they should not be used for responsive design purposes. Use [[css/media_queries/width|width]] instead.

==Syntax==
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
|Description=The first media query describes a device that has a screen width of exactly 320 pixels. 

The second example describes all screen devices with a screen width of 1024 pixels and higher. Note: The width of the browser does not matter in this case. Therefore you would have to use [[css/media_queries/width|mediaqueries: width]].

The third media query describes all devices with a screen width not wider than 1023 pixels.
|Code=@media screen and ( device-width: 320px ) { … }

@media screen and ( min-device-width: 1024px ) { … }

@media screen and ( max-device-width: 1023px ) { … }
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
|URL=http://www.w3.org/TR/mediaqueries-4/
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