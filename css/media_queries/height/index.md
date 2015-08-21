{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add description, compatibility.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The media feature describes the height of the output device's rendering surface, such as the viewport height or the height of the page box.}}
{{CSS_Media_Feature
|Content=Just as the [[css/media_queries/width|width media query]] reports the layout viewport's width, the height media query reports its height. It tells you how many CSS pixels are available vertically for showing content, which is occasionally useful if you need to figure out if an item will be shown "above the fold."

Although the layout viewport width (and thus the media query) is equal to the width of the html element, this does *not* hold for height. Frequently, the html element's height is a lot larger than the layout viewport height. The height media query's value is usually the width media query value divided by the screen's aspect ratio.

The height media query is always equal to document.documentElement.clientHeight.

One serious problem on many mobile browsers is that the layout viewport height, and thus the height media query value, changes when the browser toolbar moves into or out of view. Thus, a height media query that works perfectly when the page is scrolled up and the toolbar is visible, may misfire when the user scrolls, the toolbar moves out of view, and the layout viewport height changes. 

For this reason it's best to use height media queries sparingly, and, if you need them, to give browsers ample leeway. In general you should expect a browser toolbar to be between 40 and 70 pixels high.

==Syntax==
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