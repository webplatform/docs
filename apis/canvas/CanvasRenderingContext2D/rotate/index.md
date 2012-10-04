{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=angle|Data type=float|Description=The  rotation angle, in radians.|Optional=}}
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
|Description=The following  code example rotates  a rectangle by 5-degree increments.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;title&gt;Rotate example&lt;/title&gt;
  &lt;script type{{=}}"text/javascript"&gt;    
function draw()
{
  var canvas {{=}} document.getElementById("MyCanvas");
 	if (canvas.getContext) 
    {
 	  var ctx {{=}} canvas.getContext("2d");   
      ctx.beginPath();
      ctx.lineWidth {{=}} "3";
      ctx.strokeStyle {{=}} "blue";
      ctx.moveTo(0,0);
      ctx.lineTo(200,50);
      ctx.moveTo(0,0);
      ctx.lineTo(250,50);
      ctx.moveTo(0,0);
      ctx.lineTo(200,125);
      ctx.rect (200,50,50,75);  
      ctx.stroke();
    }      
}
function rotateRect()
{
    var canvas {{=}} document.getElementById("MyCanvas");
 	if (canvas.getContext) 
    {
 	  var ctx {{=}} canvas.getContext("2d");
      ctx.clearRect(0,0,canvas.width,canvas.height);    // Clear the rectangle before scaling.
      ctx.rotate(5 * Math.PI/180); // Rotate 5 degrees.
      draw();
    }
}
function refresh()                 
   {
    window.location.reload( false );           // Reload the page.
   }
  &lt;/script&gt;
&lt;/head&gt;
&lt;body bgcolor{{=}}"lightgray" onload{{=}}"draw();"&gt;   
            &lt;button onclick{{=}}"rotateRect()"&gt;Rotate by 5 degrees&lt;/button&gt;            
    &lt;button onclick{{=}}"refresh()"&gt;refresh page&lt;/button&gt;
    &lt;/div&gt;        
    &lt;div&gt;
	    &lt;canvas id{{=}}"MyCanvas" width{{=}}"300" height{{=}}"300"&gt; &lt;/canvas&gt; 
    &lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Rotation is based on the current origin.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 3


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