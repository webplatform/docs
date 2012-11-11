{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Height (in pixels) of the browser window viewport including, if rendered, the horizontal scrollbar.}}
{{API_Object_Property
|Property_applies_to=dom/window
|Read_only=Yes
|Example_object_name=window
|Return_value_name=height
|Javascript_data_type=Number
|Return_value_description=Viewport height in CSS pixels
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Assumes a frameset
|Code=var intFrameHeight = window.innerHeight; // or
var intFrameHeight = self.innerHeight; /* will return the height of the 
frame viewport within the frameset */
var intFramesetHeight = parent.innerHeight; /* will return the height of 
the viewport of the closest frameset */
var intOuterFramesetHeight = top.innerHeight; /* will return the height 
of the viewport of the outermost frameset */
}}
}}
{{Notes_Section
|Notes='''Graphical example'''
The following figure shows the difference between outerHeight and innerHeight.

[[File:FirefoxInnerVsOuterHeight2.png|738px|||screenshot showing difference between innerHeight and outerHeight]]
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=4
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.10
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=4
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSSOM
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/DOM/window.innerHeight
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}