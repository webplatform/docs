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
|Code=/* Correct use: a <number> (here an <integer>) followed by the unit. */
96dpi

/* Correct use in the context of a media query. */
@media print and (min-resolution: 300dpi) { ... }
}}{{Single Example
|Language=CSS
|Description=Here are some incorrect uses:
|Code=/* Incorrect: no spaces allowed between the <number> and the unit. */
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
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=29
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.5 (1.9.1)
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=dppx
|Chrome_supported=Yes
|Chrome_version=29
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=16.0 (16.0)
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.10
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=Yes
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=dppx
|Android_supported=No
|Android_version=
|Android_prefixed_supported=
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=16.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=12.10
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=WebKit
|Note=Webkit engine does not support CSS resolution query as in the specification, the use of the non-standard '''device-pixel-ratio''' query is needed for browsers Safari, see [https://bugs.webkit.org/show_bug.cgi?id=16832 bug 16832].
}}{{Compatibility Notes Row
|Browser=Firefox
|Version=< 8.0
|Note=Before Firefox 8 (Gecko 8.0), it erroneously accepted only CSS dimensions that were '''<integer>''' followed by the unit. From that version, it supports any valid CSS dimensions ('''<number>''' immediately followed by the unit).
}}
}}