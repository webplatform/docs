{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=x|Data type=float|Description=The x-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.|Optional=}}
{{Method Parameter|Name=y|Data type=float|Description=The x-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.|Optional=}}
{{Method Parameter|Name=w|Data type=float|Description=The width, in pixels, of the rectangle in relation to the coordinates of the canvas.|Optional=}}
{{Method Parameter|Name=h|Data type=float|Description=The height, in pixels, of the rectangle in relation to the coordinates of the canvas.|Optional=}}
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
|Description=The following  code example draws a filled rectange  by using [[canvas/methods/fillRect|'''fillRect''']] and then clears the center portion  by using '''clearRect'''. '''fillRect''' uses the width and height of the canvas, and '''clearRect''' uses percentages of the canvas width and height to create a frame.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
&lt;script type{{=}}"text/javascript"&gt;
  function draw()
  {
   var canvas {{=}} document.getElementById("MyCanvas"); // Get the canvas element.
 	 if (canvas.getContext) // Test for support.
     {
 	   var ctx {{=}} canvas.getContext("2d"); // Get the context to draw on.
       ctx.fillStyle {{=}} "black";  // Specify black as the fill color.             
       ctx.fillRect (0,0,canvas.width,canvas.height);  // Create a filled rectangle.
     }  
  }
  function clearMe()
  {
   var canvas {{=}} document.getElementById("MyCanvas");
 	 if (canvas.getContext) 
     {
 	   var ctx {{=}} canvas.getContext("2d");
       // Clear the center 80% of the canvas.
       ctx.clearRect(canvas.width*.1,canvas.height*.1,canvas.width*.8,canvas.height * .8);
     }
  }
  &lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"draw();"&gt;
  &lt;canvas id{{=}}"MyCanvas" width{{=}}"600" height{{=}}"500"&gt; &lt;/canvas&gt;
&lt;p&gt;
    &lt;button onclick{{=}}"clearMe();"&gt;clear me&lt;/button&gt;   
    &lt;button onclick{{=}}"draw();"&gt;Reset&lt;/button&gt;   
&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''clearRect'''  method clears the canvas to transparent black  (that is, each pixel's RGBA value is equal to zero). To clear to a specific color, use the  [[canvas/methods/fillRect|'''fillRect''']] method.
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