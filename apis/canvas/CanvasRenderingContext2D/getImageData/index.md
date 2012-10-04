{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=sx|Data type=float|Description=The x-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.|Optional=}}
{{Method Parameter|Name=sy|Data type=float|Description=The y-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.|Optional=}}
{{Method Parameter|Name=sw|Data type=float|Description=The width, in pixels, of the rectangle in relation to the coordinates of the canvas.|Optional=}}
{{Method Parameter|Name=sh|Data type=float|Description=The height, in pixels, of the rectangle in relation to the coordinates of the canvas.|Optional=}}
|Method_applies_to=canvas/objects/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''ICanvasImageData'''

A [[canvas/objects/CanvasImageData|'''CanvasImageData''']] object with pixel information from the canvas within the specified coordinates.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code example draws some shapes on one canvas and copies the data to a second canvas.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function draw()
{
  var canvas {{=}} document.getElementById("MyCanvas");
  if (canvas.getContext) 
    {
 	var ctx {{=}} canvas.getContext("2d");
    ctx.beginPath();
    ctx.rect (5,5,300,250); 
    ctx.stroke();
    ctx.arc(150,150,100,0,Math.PI, false); 
    ctx.stroke();
    }  
}
function clone()
{
  var canvas1 {{=}} document.getElementById("MyCanvas");        
  var canvas2 {{=}} document.getElementById("YourCanvas");
  if (canvas1.getContext) {
      var ctx {{=}} canvas1.getContext("2d");                // Get the context on the first canvas.
      var imageStuff {{=}} ctx.getImageData(0,0,canvas1.width,canvas1.height);    // Get image data from the first canvas.
  }
  if (canvas2.getContext) {
      var ctx2 {{=}} canvas2.getContext("2d");                // Get the context on the second canvas.
      ctx2.putImageData(imageStuff,0,0);                  // Put image data on the second canvas.
  }   
}
  &lt;/script&gt;
&lt;/head&gt;
&lt;body bgcolor{{=}}"lightgray"&gt;
      &lt;div&gt;
        &lt;button onclick{{=}}"draw()"&gt;Draw Images on canvas&lt;/button&gt; 
        &lt;button onclick{{=}}"clone()"&gt;Copy canvas to canvas&lt;/button&gt;
      &lt;/div&gt;
      &lt;div&gt;
        &lt;canvas id{{=}}"MyCanvas" width{{=}}"400" height{{=}}"400" &gt; &lt;/canvas&gt;
        &lt;canvas id{{=}}"YourCanvas" width{{=}}"400" height{{=}}"400"&gt; &lt;/canvas&gt;
      &lt;/div&gt;
  &lt;/body&gt;
&lt;/html&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
If the rectangle contains pixels outside the canvas, they are returned as transparent black.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 13


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[canvas/objects/CanvasRenderingContext2D|CanvasRenderingContext2D]]</code>
*<code>[[canvas/objects/CanvasPixelArray|CanvasPixelArray]]</code>
*<code>[[canvas/methods/getImageData|getImageData]]</code>
*<code>[[canvas/properties/data|data]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}