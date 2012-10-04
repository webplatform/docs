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
|Description=The following  code example uses '''strokeStyle''' to change the colors of three subpaths.
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
      ctx.beginPath();
      ctx.strokeStyle{{=}}"green";  // Use strokeStyle to set the color.
      ctx.rect (5,5,300,250); 
      ctx.stroke();
      ctx.beginPath();
      ctx.strokeStyle{{=}}"blue";  // Use strokeStyle to change the color.
      ctx.lineWidth {{=}} "5";
      ctx.moveTo(100,100);
      ctx.lineTo(130,100);
      ctx.moveTo(170,100);
      ctx.lineTo(200,100);
      ctx.stroke();
      ctx.beginPath();
      ctx.strokeStyle{{=}}"red";  // Use strokeStyle to change the color.
      ctx.arc(150,125,100,0,Math.PI, false);
      ctx.stroke();
    }  
}
  &lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"draw();"&gt;
  &lt;canvas id{{=}}"MyCanvas" width{{=}}"600" height{{=}}"600"&gt; &lt;/canvas&gt; 
&lt;/body&gt;
&lt;/html&gt;

}}}}
{{Notes_Section
|Notes=
===Remarks===
The style can consist of a string  that contains  a CSS color, [[canvas/objects/CanvasGradient|'''CanvasGradient''']] object, or [[canvas/objects/CanvasPattern|'''CanvasPattern''']] object.
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