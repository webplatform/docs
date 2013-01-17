{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following code example creates a 200 &times; 200 pixel viewport and draws a red, 50 px-radius circle that has a black border. If you move the mouse pointer over the rendered circle, the circle doubles its radius; if you move the mouse pointer off the rendered circle, the circle's current radius reduces by half. The rectangle element is used to outline the boundaries of the viewport.
|LiveURL=To make this example work across browsers, save this code example with a .xhtml extension.
|Code=
<syntaxhighlight lang="xml">
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
  <title>Manipulating the Radius of an SVG Circle</title>
  <script language="javascript" type="text/javascript">
    var red_circle;  // An object that represents the circle.
    var r;           // A variable that represents the circle's radius.

    window.onload = function() {
      red_circle = document.getElementById('redCircle');
      r = parseInt(red_circle.getAttribute("r"));
    }

    function grow() {
      r = 2*r;
      red_circle.setAttribute("r",r);
    }

    function shrink() {
      r = r/2;
      red_circle.setAttribute("r",r);
    }
  </script>
</head>
<body>
  <svg xmlns="http://www.w3.org/2000/svg" version="1.1" width="200px" height="200px">
    <circle id="redCircle" cx="100" cy="100" r="50" style="stroke: black; fill: red;" onmouseover="grow()" onmouseout="shrink()"/>
    <rect x="0" y="0" width="100%" height="100%" style="fill: none; stroke: black;"/>
  </svg>
</body>
</html>
</syntaxhighlight>
}}}}
{{Topics|SVG}}
{{Notes_Section
|Import_Notes=

===Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204737 Scalable Vector Graphics: Basic Shapes], Section 9.8.2

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/elements/circle|'''SVGCircleElement''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]