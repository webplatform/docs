{{Page_Title|Color units}}
{{Flags
|High-level issues=Stub
|Editorial notes=(Stub to populate css/units tree)
}}
{{API_Name}}
{{Summary_Section|Specify color and opacity}}
{{Concept_Page
|Content=Several different ways are available to specify simple color values:

* ''Keyword'' values specify common color names such as '''yellow''', '''black''', or '''transparent'''.

* Hexadecimal values specify opaque colors in the range of '''#000000''' ('''black''') to '''#ffffff''' ('''white'''), where  each pair of characters correspond to red, green, and blue.

* An '''rgb()''' function specifies red, green and blue values either as integers between 0 and 255 (corresponding to the hex values above), or as percentages. For example, '''rgb(256,0,0)''' and '''rgb(100%,0%,0%)''' both correspond to '''red'''.

* An '''hsl()''' function specifies hue, saturation, and luminance values. Hue values are specified as an [[css/units/angle|angle within the color wheel]] relative to '''red''', and numeric values default to degrees. Saturation specifies vividness as a percentage, with '''0%''' specifying various shades of gray. Luminence specifies brightness, with '''0%''' and '''100%'' corresponding to '''black''' and '''white''', and '''50%''' appearing as a more vivid hue. For example, '''hsl(0%,100%,50%)''' also corresponds to '''red'''.

The following variations on the above allow you to incorporate an
''alpha'' channel specifying transparencies:

* An '''rgba()''' function specifies red, green and blue values as described above, along with opacity expressed in decimal terms between 0 and 1. For example, '''rgba(100%,0%,0%,0.5)''' specifies a semi-transparent red, which appears as pink.

* An '''hsla()''' function specifies hue, saturation, and luminance as described above, but with an additional ''alpha'' channel. For example, '''hsla(0%,100%,50%,0.5)''' specifies the same semi-transparent red as the '''rgba()''' example above.

The recently introduced '''transparent''' color name specifies a full transparency.

[http://www.w3.org/TR/2011/REC-css3-color-20110607/ color]

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=aside {
    color: white;              /* white letterforms */
    text-shadow: 0 0 4px red;  /* red backlight effect */
    background-color: #777777; /* gray background */
}
.semitrans {
    /* elements behind this show through */
    background-color: rgba(50%, 50%, 50%, 0.5); 
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