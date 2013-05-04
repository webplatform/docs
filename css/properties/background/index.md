{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The ‘background’ property is a shorthand property for setting most background properties at the same place in the style sheet.}}
{{CSS Property
|Initial value=see individual properties
|Applies to=all elements
|Inherited=No
|Media=visual
|Computed value=see individual properties
|Animatable=No
|CSS percentages=see individual properties
|Values={{CSS Property Value
|Data Type=<background-color> <background-position> <background-size> <background-repeat> <background-clip> <background-origin> <background-attachment> <background-image>
|Description=The background property is a shorthand property for setting the color, position, size, repeat, clip, origin, attachment, and/or image of the element.

* color - Any of the values available to [[css/properties/background-color|'''background-color''']] property. The default value is <tt>transparent</tt>.
* position - Any of the values available to [[css/properties/background-position|'''background-position''']] property. The default value is <tt>0% 0%</tt>.
* size - Any of the values available to [[css/properties/background-size|'''background-size''']] property. The default value is <tt>auto</tt>.
* repeat - Any of the values available to [[css/properties/background-repeat|'''background-repeat''']] property. The default value is <tt>repeat</tt>.
* clip - Any of the values available to [[css/properties/background-clip|'''background-clip''']] property. The default value is <tt>border-box</tt>.
* origin - Any of the values available to [[css/properties/background-origin|'''background-origin''']] property. The default value is <tt>padding-box</tt>.
* attachment - Any of the values available to [[css/properties/background-attachment|'''background-attachment''']] property. The default value is <tt>scroll</tt>.
* image - Any of the values available to [[css/properties/background-image|'''background-image''']] property. The default value is <tt>none</tt>.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=In the first rule of the following example, only a value for ‘background-color’ has been given and the other individual properties are set to their initial values. In the second rule, many individual properties have been specified.
|Code=body { background: red }
p { background: url("chess.png") 40% / 10em gray
       round fixed border-box; }
}}{{Single Example
|Language=CSS
|Description=The first rule is equivalent to
|Code=body {
    background-color: red;
    background-position: 0% 0%;
    background-size: auto auto;
    background-repeat: repeat repeat;
    background-clip: border-box;
    background-origin: padding-box;
    background-attachment: scroll;
    background-image: none }
}}{{Single Example
|Language=CSS
|Description=The second is equivalent to
|Code=p {
    background-color: gray;
    background-position: 40% 50%;
    background-size: 10em 10em;
    background-repeat: round round;
    background-clip: border-box;
    background-origin: border-box;
    background-attachment: fixed;
    background-image: url(chess.png) }
}}{{Single Example
|Language=CSS
|Description=The following example shows how both a background color (#CCC) and a background image (url(metal.jpg)) are set. The image is rescaled to the full width of the element:
|Code=E { background: #CCC url("metal.jpg") top left / 100% auto no-repeat}
}}{{Single Example
|Language=CSS
|Description=The following
|Code=div { background: padding-box url(paper.jpg) white center }
}}{{Single Example
|Language=CSS
|Description=becomes
|Code=div {
    background-color: white;
    background-image: url(paper.jpg);
    background-repeat: repeat;
    background-attachment: scroll;
    background-position: center;
    background-clip: padding-box;
    background-origin: padding-box;
    background-size: auto auto }
}}{{Single Example
|Language=CSS
|Description=The following declaration with multiple, comma-separated values
|Code=background: url(a.png) top left no-repeat,
            url(b.png) center / 100% 100% no-repeat,
            url(c.png) white;
}}{{Single Example
|Language=CSS
|Description=is equivalent to
|Code=background-image:      url(a.png),  url(b.png),          url(c.png);
background-position:   top left,    center,              top left;
background-repeat:     no-repeat,   no-repeat no-repeat, repeat;
background-clip:       border-box,  border-box,          border-box;
background-origin:     padding-box, padding-box,         padding-box;
background-size:       auto auto,   100% 100%,           auto auto;
background-attachment: scroll,      scroll,              scroll;
background-color:      white;
}}
}}
{{Notes_Section
|Notes=Background of Special Elements

The background of the root element becomes the background of the canvas and its background painting area extends to cover the entire canvas, although any images are sized and positioned relative to the root element as if they were painted for that element alone. (In other words, the background positioning area is determined as for the root element.) If the root's ‘background-color’ value is ‘transparent’, the canvas's background color is UA dependent. The root element does not paint this background again, i.e., the used value of its background is transparent.

For documents whose root element is an HTML HTML element [HTML401] or an XHTML html element [XHTML11]: if the computed value of ‘background-image’ on the root element is ‘none’ and its ‘background-color’ is ‘transparent’, user agents must instead propagate the computed values of the background properties from that element's first HTML BODY or XHTML body child element. The used values of that BODY element's background properties are their initial values, and the propagated values are treated as if they were specified on the root element. It is recommended that authors of HTML documents specify the canvas background for the BODY element rather than the HTML element.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3
|URL=http://www.w3.org/TR/css3-background/
|Status=Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=HTML
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}