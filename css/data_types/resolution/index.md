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
|Code=96dpi                                              Correct use: a <number> (here an <integer>) followed by the unit.
@media print and (min-resolution: 300dpi) { ... }  Correct use in the context of a media query.
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Values and Units Module Level 3
|URL=http://www.w3.org/TR/css3-values/
|Status=Candidate Recommendation
}}
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/Web/CSS/resolution
|MSDN_link=
|HTML5Rocks_link=
}}