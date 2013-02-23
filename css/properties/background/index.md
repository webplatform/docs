{{Page_Title}}
{{Flags}}
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
|Values=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=In the first rule of the following example, only a value for ‘background-color’ has been given and the other individual properties are set to their initial values. In the second rule, many individual properties have been specified.

|Code=body { background: red }
p { background: url("chess.png") 40% / 10em gray
       round fixed border-box; }
The first rule is equivalent to:

body {
    background-color: red;
    background-position: 0% 0%;
    background-size: auto auto;
    background-repeat: repeat repeat;
    background-clip: border-box;
    background-origin: padding-box;
    background-attachment: scroll;
    background-image: none }
The second is equivalent to:

p {
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
|Code=The following example shows how a both a background color (#CCC) and a background image (url(metal.jpg)) are set. The image is rescaled to the full width of the element:

E { background: #CCC url("metal.jpg") top left / 100% auto no-repeat}
}}{{Single Example
|Language=CSS
|Code=Another example shows equivalence:

div { background: padding-box url(paper.jpg) white center }
div {
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
|Code=The following declaration with multiple, comma-separated values

background: url(a.png) top left no-repeat,
            url(b.png) center / 100% 100% no-repeat,
            url(c.png) white;
is equivalent to

background-image:      url(a.png),  url(b.png),          url(c.png);
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

According to these rules, the canvas underlying the following HTML document will have a “marble” background:

<!DOCTYPE html PUBLIC '-//W3C//DTD HTML 4.0//EN'
  >
<html>
  <head>
    <title>Setting the canvas background</title>
    <style type="text/css">
       body { background: url("http://example.org/marble.png") }
    </style>
  </head>
  <body>
    <p>My background is marble.</p>
  </body>
</html>
The ‘::first-line’ pseudo-element is like an inline-level element for the purposes of the background (see section 5.12.1 of [CSS21]). That means, e.g., that in a left-justified first line, the background does not necessarily extend all the way to the right margin.
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
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}