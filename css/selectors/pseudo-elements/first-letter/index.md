{{Page_Title|::first-letter}}
{{Flags
|State=Almost Ready
|Editorial notes=Remove topic cluster flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Represents the first letter of an element, if it is not preceded by any other content (such as images or inline tables) on its line. The ::first-letter pseudo-element may be used for "initial caps" and "drop caps", which are common typographical effects.}}
{{CSS_Selector
|Content====Syntax===
{{Single Example
|Language=CSS
|Code=::first-letter {}
}}
===Usage===
The ::first-letter pseudo-element selects the first letter or digit of the first line of a block. Some languages require two letters to be capitalised (digraphs) which are currently very poorly supported by browsers.

The ::first-letter pseudo-element can be attached to block-level elements. It can be attached to inline elements if you set the corresponding display property to block.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following CSS will create "initial caps" by doubling the size of the first letter of any paragraph.
|Code=p::first-letter {
   font-size: 200%;
}
|LiveURL=https://code.webplatform.org/gist/6cbbb246cdbcf6c2bfaf
}}{{Single Example
|Language=CSS
|Description=The following CSS will create a drop capital spanning about two lines.
|Code=p::first-letter {
    float: left;
    font-size: 300%;
}
|LiveURL=https://code.webplatform.org/gist/5257e9b2d1e11631d608
}}
}}
{{Notes_Section
|Notes=Only the following properties apply to the ::first-letter pseudo-element:
[[css/properties/background|'''background''']], [[css/properties/border|'''border''']], [[css/properties/color|'''color''']], [[css/properties/font|'''font''']], [[css/properties/font-family|'''font-family''']], [[css/properties/font-size|'''font-size''']], [[css/properties/font-style|'''font-style''']], [[css/fonts/font-variant|'''font-variant''']], [[css/properties/font-weight|'''font-weight''']], [[css/properties/float|'''float''']], [[css/properties/line-height|'''line-height''']], [[css/properties/margin|'''margin''']], [[css/properties/padding|'''padding''']], [[css/properties/text-decoration|'''text-decoration''']], [[css/properties/text-shadow|'''text-shadow''']], [[css/properties/text-transform|'''text-transform''']], [[css/properties/vertical-align|'''vertical-align''']] (if 'float' is set to 'none'), and [[css/text/word-spacing/word-spacing|'''word-spacing''']]
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1 Selectors
|URL=http://www.w3.org/TR/CSS2/selector.html#first-letter
|Status=W3C Recommendation
}}{{Related Specification
|Name=CSS 3 Selectors
|URL=http://www.w3.org/TR/css3-selectors/#first-letter
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=> 9
|Note=Only the one-colon form of this pseudo-element is recognized (:first-letter). Beginning with Internet Explorer 9, the first-letter pseudo-element requires two colons, though the one-colon form is still recognized and behaves identically to the two-colon form.
}}
}}
{{See_Also_Section
|Topic_clusters=Fonts, Pseudo-Elements, Selectors, Text
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}