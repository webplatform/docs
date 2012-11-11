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
|Notes=The following figure shows the difference between outerHeight and innerHeight.
}}
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