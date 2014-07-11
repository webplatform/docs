{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes={{Editorial/Deletion_Candidate
| This page is a candidate for deletion because the property was never implemented. To underline text, see http://docs.webplatform.org/wiki/css/properties/text-decoration.
}}
|Checked_Out=Yes
|High-level issues=Deletion Candidate, Needs Review
|Content=Compatibility Incomplete
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Unsupported.

The 'text-underline' property is the shorthand for 'text-underline-style', 'text-underline-width', 'text-underline-color', 'text-underline-mode' and 'text-underline-position'.
}}
{{CSS Property
|Initial value=not defined for shorthand properties
|Applies to=all elements with textual content, including generated content
|Inherited=No
|Media=visual
|Computed value=specified value (except for initial and inherit)
|Animatable=No
|CSS object model property=N/A
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=text-underline-style
|Description=This property specify the line style for underline.
Possible values: none/solid/double/dotted/dashed/dot-dash/dot-dot-dash/wave
}}{{CSS Property Value
|Data Type=text-underline-color
|Description=This property specifies the line color for the underline.
}}{{CSS Property Value
|Data Type=text-underline-mode
|Description=This property set the mode for the underline determining whether the text decoration affects the space characters or not. 'Space characters' are all characters classified by the Unicode Standard [UNICODE] as category 'Zs', in addition to the white space characters.
Possible values:  continuous/skip-white-space
}}{{CSS Property Value
|Data Type=text-underline-position
|Description=This property sets the position of the underline. It can appear either 'before' (above in an horizontal flow) or after (below in an horizontal flow) the run of text in relation to its baseline orientation. This property is typically used in vertical writing context where it may be desired to have the underline appear 'before' the run of text. This results in having the underline appearing on the right side of the vertical writing column.
Possible values: auto/before-edge/alphabetic/after-edge
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|LiveURL=http://code.webplatform.org/gist/5779274
}}
}}
{{Notes_Section
|Usage=The property text-underline is not supported by any of listed new browsers (Chrome/FF/Opera/IE10). 
Instead use '''text-decoration: underline'''.

The possible exception is '''text-underline-position''': http://docs.webplatform.org/wiki/css/properties/text-underline-position.
|Notes=The 'text-decoration' property has limitations stemming from its syntax, precluding fine control over each of those formatting effects. Specifically, it offers no way to control the color or line style of the underline, overline or line-through.
CSS3 extends the model by introducing new properties allowing additional controls over those formatting effects. CSS3 also makes turning these formatting effects on or off possible without affecting any other 'text-decoration' settings.
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
|Topic_clusters=CSS Font
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}