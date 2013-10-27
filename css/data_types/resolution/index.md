{{Page_Title|Resolution units}}
{{Flags
|Content=Incomplete
|Checked_Out=No
}}
{{API_Name}}
{{Summary_Section|Specify the display or print dot density}}
{{Concept_Page
|Content=The '''<resolution>''' CSS data types, used in media queries, denotes the density of pixels of an output device, its resolution. It is a '''<number>''' immediately followed by a unit of resolution ('''dpi''', '''dpcm''', ...). Like for any CSS dimension, there is no space between the unit literal and the number.

On screens, the length related to CSS inches, centimeters or pixels, not on physical values.

Even if all units represent the same resolution for the value '''0''', the unit may not be omitted in that case as it isn't a '''<length>''': '''0''' is invalid and does not represent '''0dpi''', '''0dpcm''', nor '''0dppx'''.

==Units==

'''dpi'''
    This unit represents the number of dots per inch. A screen typically contains 72 or 96 dpi; a printed document usually reach much greater dpi. As 1 inch is 2.54 cm, '''1dpi ≈ 2.54dpcm'''.
'''dpcm'''
    This unit represents the number of dots per centimeter. As 1 inch is 2.54 cm, '''1dpcm ≈ 0.39dpi'''.
'''dppx'''
    This unit represents the number of dots per px unit. Due to the 1:96 fixed ratio of CSS '''in''' to CSS '''px''', '''1dppx''' is equivalent to '''96dpi''', that corresponds to the default resolution of images displayed in CSS as defined by {{cssxref("image-resolution")}}.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Here are some correct uses of <resolution> values:
|Code=
/* Correct use: a <number> (here an <integer>) followed by the unit. */
96dpi

/* Correct use in the context of a media query. */
@media print and (min-resolution: 300dpi) { ... }
}}{{Single Example
|Language=CSS
|Description=Here are some incorrect uses:
|Code=
/* Incorrect: no spaces allowed between the <number> and the unit. */
72 dpi

/* Incorrect: only digits must be used. */
ten dpi

/* Incorrect: the unit can be omitted for 0 values only for <length>. */
0
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Values and Units Module Level 3
|URL=http://www.w3.org/TR/css3-values/
|Status=Candidate Recommendation
}}{{Related Specification
|Name=CSS Image Values and Replaced Content Module Level 3
|URL=http://dev.w3.org/csswg/css3-images/#resolution-units
|Status=Candidate Recommendation
|Relevant_changes=Added the dppx unit
}}{{Related Specification
|Name=Media Queries
|URL=http://dev.w3.org/csswg/css3-mediaqueries/#resolution
|Status=Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=4.0
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=0.2
|Firefox_supported=Yes
|Firefox_version=4.0 (2.0)
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=1.0 (1.7 or earlier)
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.0
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=3.0
}}{{Compatibility Table Desktop Row
|Feature=Percentages
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=Elliptical borders
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.5 (1.9.1)
|Firefox_prefixed_supported=Yes
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=4 values for 4 corners
|Chrome_supported=Yes
|Chrome_version=4.0
|Chrome_prefixed_supported=Yes
|Firefox_supported=Yes
|Firefox_prefixed_supported=Yes
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.2
|Android_prefixed_supported=Yes
|Android_prefixed_version=2.1
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=11.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=4.0
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=3.2
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Firefox
|Version=< 3.6
|Note=Used to treat percentage values as percentages of the width, for both axes
}}{{Compatibility Notes Row
|Browser=Firefox
|Version=< 3.6
|Note=Non-standard longhand names (-moz-border-radius-topleft etc)
}}{{Compatibility Notes Row
|Browser=WebKit
|Version=< 532.5
|Note=Supports only one value in border-radius. For different radii, the longhands need to be used. don't support the slash / notation. If two values are specified, they are interpreted as horizontal and vertical radii for all four corners.
}}{{Compatibility Notes Row
|Browser=WebKit
|Version=< 532.5
|Note=When the sum of two adjacent radii exceeds the length of the side they’re on, they are reduced to 0 instead of shrinking proportionally.
}}{{Compatibility Notes Row
|Browser=Opera
|Version=< 11.6
|Note=border-radius has no effect in replaced elements (like images)
}}{{Compatibility Notes Row
|Browser=Opera
|Version=< 11.6
|Note=Percentages are accepted in border-radius, but are treated incorrectly.
}}
}}
{{See_Also_Section
|Topic_clusters=Media Queries
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/Web/CSS/resolution
|MSDN_link=
|HTML5Rocks_link=
}}