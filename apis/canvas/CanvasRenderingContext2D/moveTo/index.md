{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=x|Data type=float|Description=The x-coordinate, in pixels.|Optional=}}
{{Method Parameter|Name=y|Data type=float|Description=The y-coordinate, in pixels.|Optional=}}
|Method_applies_to=canvas/objects/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code example uses  the '''moveTo'''  and  [[canvas/methods/lineTo|'''lineTo''']] methods  to incrementally draw horizontal lines across the canvas.
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
      for(i{{=}}10;i&lt;500;i+{{=}}20)
      {
      ctx.moveTo(0,i);
      ctx.lineTo(canvas.width,i);
      ctx.stroke();
      }             
   }
}
  &lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"draw()"&gt;
  &lt;canvas id{{=}}"MyCanvas" width{{=}}"600" height{{=}}"600"&gt; &lt;/canvas&gt; 
&lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 9


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[canvas/objects/CanvasRenderingContext2D|CanvasRenderingContext2D]]</code>
*<code>[[canvas/methods/lineTo|lineTo]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}