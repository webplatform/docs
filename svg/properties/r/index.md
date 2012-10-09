{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following code example creates a 200 × 200 pixel viewport and draws a red, 50 px-radius circle that has a black border. If you move the mouse pointer over the rendered circle, the circle doubles its radius; if you move the mouse pointer off the rendered circle, the circle's current radius reduces by half. The rectangle element is used to outline the boundaries of the viewport.
|LiveURL=To make this example work across browsers, save this code example with a .xhtml extension.
|Code=
&lt;?xml version{{=}}"1.0" encoding{{=}}"UTF-8"?&gt;
&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;
&lt;html xmlns{{=}}"http://www.w3.org/1999/xhtml"&gt;
&lt;head&gt;
  &lt;title&gt;Manipulating the Radius of an SVG Circle&lt;/title&gt;
  &lt;script language{{=}}"javascript" type{{=}}"text/javascript"&gt;
    var red_circle;  // An object that represents the circle.
    var r;           // A variable that represents the circle's radius.
		
    window.onload {{=}} function() {
      red_circle {{=}} document.getElementById('redCircle');
      r {{=}} parseInt(red_circle.getAttribute("r"));
    }
		
    function grow() {
      r {{=}} 2*r;
      red_circle.setAttribute("r",r);
    }
		
    function shrink() {
      r {{=}} r/2;
      red_circle.setAttribute("r",r);
    }
  &lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;svg xmlns{{=}}"http://www.w3.org/2000/svg" version{{=}}"1.1" width{{=}}"200px" height{{=}}"200px"&gt;
    &lt;circle id{{=}}"redCircle" cx{{=}}"100" cy{{=}}"100" r{{=}}"50" 
                style{{=}}"stroke: black; fill: red;" 
                onmouseover{{=}}"grow()" onmouseout{{=}}"shrink()"/&gt;
    &lt;rect x{{=}}"0" y{{=}}"0" width{{=}}"100%" height{{=}}"100%" style{{=}}"fill: none; stroke: black;"/&gt;
  &lt;/svg&gt;
&lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204737 Scalable Vector Graphics: Basic Shapes], Section 9.8.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/circle|SVGCircleElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]