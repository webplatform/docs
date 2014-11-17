{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|Content=Examples Needed
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The '''text-overline''' property is the shorthand for the [[css/properties/text-overline-style|text-overline-style]], [[css/properties/text-overline-width|text-overline-width]], [[css/properties/text-overline-color|text-overline-color]], and [[css/properties/text-overline-mode|text-overline-mode]] properties.}}
{{CSS Property
|Initial value=not defined for shorthand properties
|Applies to=all elements with and generated content with textual content
|Inherited=No
|Media=visual
|Computed value=
|Animatable=No
|CSS object model property=
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<'text-overline-style'>
|Description=Possible values:

None- Produces no line.
solid - Produces a solid line.
double - Produces a double line.
dotted - Produces a dotted line.
dashed - Produces a dashed line style.
dot-dash - Produces a line whose repeating pattern is a dot followed by a dash.
dot-dot-dash - Produces a line whose repeating pattern is two dots followed by a dash.
wave - Produces a wavy line.
}}{{CSS Property Value
|Data Type=<'text-overline-color'>
|Description=Possible values:
<color> - Specifies a color value.
}}{{CSS Property Value
|Data Type=<'text-overline-mode'>
|Description=This property determines whether only words meant to be overlined or if the whitespace between words and words meant to be overlined.  There are two unique values: continuous or words. 
Continuous is the default value and shows overline for both words and whitespaces. 
Words only shows onverline for words and not whitespaces.
It can also have the values of initial or inherit.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Produces a single, solid, blue overline.
|Code=p {
   text-overline: solid blue;
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS3 Text Module
|URL=http://www.w3.org/TR/2003/CR-css3-text-20030514/
|Status=Candidate Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}