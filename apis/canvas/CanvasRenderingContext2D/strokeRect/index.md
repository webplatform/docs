{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=x|Data type=float|Description=The x-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.|Optional=}}
{{Method Parameter|Name=y|Data type=float|Description=The y-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.|Optional=}}
{{Method Parameter|Name=w|Data type=float|Description=The width, in pixels, of  the rectangle in relation to the coordinates of the canvas.|Optional=}}
{{Method Parameter|Name=h|Data type=float|Description=The height, in pixels, of the rectangle in relation to the coordinates of the canvas.|Optional=}}
|Method_applies_to=canvas/objects/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code example draws rectangles by using [[canvas/properties/strokeStyle|'''strokeStyle''']], [[canvas/properties/lineJoin|'''lineJoin''']], and [[canvas/properties/lineWidth|'''lineWidth''']] for different effects.
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
      ctx.lineWidth {{=}} "3";
      ctx.strokeStyle {{=}} "blue";
      ctx.strokeRect (5,5,300,250);  
      ctx.stroke();
      ctx.lineWidth {{=}} "5";
      ctx.strokeStyle {{=}} "red";
      ctx.strokeRect (150,200,300,150);
      ctx.stroke();
      ctx.lineJoin {{=}} "round";
      ctx.lineWidth {{=}} "10";
      ctx.lineWidth {{=}} "7";
      ctx.strokeStyle {{=}} "green";
      ctx.strokeRect (250,50,150,250);
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
The '''strokeRect'''  method creates a path  that  requires the use of  the [[canvas/methods/stroke|'''stroke''']]  method to render the rectangle. The outline uses the current [[canvas/properties/strokeStyle|'''strokeStyle''']], [[canvas/properties/lineWidth|'''lineWidth''']], [[canvas/properties/lineJoin|'''lineJoin''']], and, when appropriate, [[canvas/properties/miterLimit|'''miterLimit''']]  properties. If  the  ''w'' or ''h''  parameter  is zero, a line is drawn. If  the  ''w''  and ''h''  parameters are zero, the rectangle is not drawn.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 8


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