{{Page_Title|&lt;length&gt;}}
{{Flags
|State=Almost Done
|Editorial notes=compatibility
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{Summary_Section|A <code>&lt;length></code> is a CSS data type that is used to specify distance measurements using relative or absolute units.  It consists of an integer or decimal number followed (without whitespace) by a unit abbreviation; the unit may be omitted if the number is zero (0).}}
{{Data_Type_Page
|Content=In CSS, there are many properties that can take a length as a value — such as [[css/properties/width|width]], [[css/properties/height|height]], [[css/properties/top|top]] and [[css/properties/bottom|bottom]] — or at least part of their value, for example [[css/properties/box-shadow|box-shadow]], [[css/properties/border|border]], [[css/properties/background-image|background-image]] and [[css/properties/flex|flex]].

Length units specify a distance on the display screen or printed output. Pairs of length units are typically used to specify <code>x</code>/<code>y</code> screen coordinates or offsets.  Several different kinds of length
units are available:
* ''Absolute'' lengths:
* ''Relative font'' lengths:
* ''Relative viewport'' lengths:

==''Absolute'' lengths==
* '''cm''' and '''mm''' specify centimeters and millimeters.
* '''in''' units specify inches.
* '''pc''' units specify picas, 6 per inch.
* '''pt''' units specify points, 72 per inch.
* '''px''' units specify pixels, 96 per inch. These are often referred to as ''CSS pixels'', and do not necessarily correspond to the device's resolution.

Absolute does not mean that these units will be treated the same on every device, only that they do not depend on other style properties and that they have fixed conversion factors between them.  In particular, the '''in''' and '''cm''' units will not always correspond to the "real-world" definitions of an inch or a centimeter.  For devices which are usually viewed at a distance (TVs and projectors), the specifications define a [http://www.w3.org/TR/css3-values/#reference-pixel reference pixel] based on the expected angle it would cover in the user's field of view; the other units should be mapped relative to this reference.  The reference pixel (and therefore other units) of a screen device may also be affected by user settings.   For print media, it is recommended (but not required) that normal physical inches or centimeters be used as the reference value.

==''Relative font'' lengths==
* '''em''' units equal the point size (nominal height) of the current font.  This is historically based on the mechanical typeset width of the (square) letter "M".
* '''rem''' units equal the ''em'' size for the document root (usually '''html''')
* '''ex''' units specify the height of the letter "x" in the current font, the general height of lowercase letters without ascenders.
* '''ch''' units specify the width of the numeral "0" in the current font, which is roughly the average for most text characters.

==''Relative viewport'' lengths==
* '''vw''' units specify a percentage of the width of the current viewport, e.g., the window.
* '''vh''' units specify a percentage of current viewport's height.
* '''vmax''' and '''vmin''' units specify the maximum or minimum of the viewport's width or height.

Note that [[css/data_types/numeric|percentages]] may refer to various length units, but for length specifies the height and width of an element, or the overall document window.

Also bear in mind that some properties accept negative values, while some don't. So for example, you can't specify negative [[css/properties/padding|padding]], but you could use a negative [[css/properties/margin|margin]] to move a block in the direction of the negative margin's side, and you can use negative units in [[css/properties/box-shadow|box-shadow]] to move the box left and up rather than right and down.
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
}}{{Related Specification
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS21/syndata.html#length-units
|Status=W3C Recommendation
|Relevant_changes=Defined the CSS pixel as 1/96th of an inch.
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{API_Name}}