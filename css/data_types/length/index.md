{{Page_Title|Length units}}
{{Flags
|Checked_Out=Yes
}}
{{API_Name}}
{{Summary_Section|Specify measurements using relative or absolute units}}
{{Concept_Page
|Content=Length units specify a distance on the display screen or
printed output. Pairs of length units are typically used to specify
''x''/''y'' screen coordinates or offsets.  Several different kinds of length
units are available:

* ''Absolute'' lengths:
** '''cm''' and '''mm''' specify centimeters and millimeters.
** '''in''' units specify inches.
** '''pc''' units specify picas, 6 per inch.
** '''pt''' units specify points, 72 per inch.
** '''px''' units specify pixels, 96 per inch. These are often referred to as ''CSS pixels'', and do not necessarily correspond to the device's resolution.
* ''Relative font'' lengths:
** '''em''' units equal the point size (nominal height) of the current font.  This is historically based on the mechanical typeset width of the (square) letter "M".
** '''rem''' units equal the ''em'' size for the document root (usually '''html''')
** '''ex''' units specify the height of the letter "x" in the current font, the general height of lowercase letters without ascenders.
** '''ch''' units specify the width of the numeral "0" in the current font, which is roughly the average for most text characters.
* ''Relative viewport' lengths:
** '''vw''' units specify a percentage of the width of the current viewport, e.g., the window.
** '''vh''' units specify a percentage of current viewport's height.
** '''vmax''' and '''vmin''' units specify the maximum or minimum of the viewport's width or height.

Note that [[css/units/numeric|percentages]] may refer to various length units, but for length specifies the height and width of an element, or the overall document window.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=.info {
    position: fixed;
    /* use various units to position element */
    top: 0.5in;
    right: 2em;
    /* provide fallback value for more recent viewport units */
    width: 25%;
    width: 25vw;
}
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
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}