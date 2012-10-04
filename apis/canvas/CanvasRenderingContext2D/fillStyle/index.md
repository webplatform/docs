{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=canvas/objects/CanvasRenderingContext2D
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code example shows filling rectangles with a linear gradient and a solid color.
|LiveURL=
|Code=

&lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function draw()
{
  var canvas {{=}} document.getElementById("MyCanvas");
 	if (canvas.getContext) {
 	  var ctx {{=}} canvas.getContext("2d");
      gradient {{=}} ctx.createLinearGradient(0, 0, canvas.width, 0);
  // Add the colors with fixed stops at 1/4 of the width.
      gradient.addColorStop("0","magenta");
      gradient.addColorStop(".25","blue");
      gradient.addColorStop(".50","green");
      gradient.addColorStop(".75","yellow");
      gradient.addColorStop("1.0","red");
      
      // Use the gradient.
      ctx.fillStyle {{=}} gradient;
      ctx.fillRect (0,0,300,250);  
      ctx.fillStyle {{=}} "blue";
      ctx.fillRect(250,300,600,500);
    }  
}
  &lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"draw();"&gt;
  &lt;canvas id{{=}}"MyCanvas" width{{=}}"600" height{{=}}"500" border{{=}}"1"&gt; &lt;/canvas&gt; 
&lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Invalid values are ignored.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[canvas/objects/CanvasRenderingContext2D|CanvasRenderingContext2D]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}