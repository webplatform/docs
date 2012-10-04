{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=image|Data type=IDispatch|Description=An image, canvas, or video element of the pattern to  use.|Optional=}}
{{Method Parameter|Name=repetition|Data type=VARIANT|Description=The direction of repetition. This parameter  specifies one of the following values:|Optional=}}
|Method_applies_to=canvas/objects/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=[[canvas/objects/CanvasPattern|'''CanvasPattern''']]

The pattern object to use as a [[canvas/properties/fillStyle|'''fill style''']]  together with a [[canvas/objects/CanvasRenderingContext2D|'''CanvasRenderingContext2D''']] object.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following code example demonstrates each type of direction that you can repeat an image in a canvas.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function draw(direction)
{
  var canvas {{=}} document.getElementById("MyCanvas");
  if (canvas.getContext) 
     {
      var ctx {{=}} canvas.getContext("2d");                // Get the context.
      ctx.clearRect(0,0,canvas.width,canvas.height);    // Clear the last image if it exists.
      var image {{=}} document.getElementById("pix");       // Get the address of the picture.
      var pattern {{=}} ctx.createPattern(image, direction);// Get the direction from the button.    
      ctx.fillStyle {{=}} pattern;                          // Assign pattern as a fill style.
      ctx.fillRect(0,0,canvas.width,canvas.height);     // Fill the canvas.   
    }  
}
  &lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;p&gt;This picture will appear below.&lt;/p&gt;
    &lt;div&gt;
    &lt;img id{{=}}"pix" src{{=}}"http://go.microsoft.com/fwlink/?LinkID{{=}}199028" /&gt;   
    &lt;/div&gt;
    &lt;button onclick{{=}}"draw('repeat')"&gt;Repeat all&lt;/button&gt; 
    &lt;button onclick{{=}}"draw('repeat-x')"&gt;Repeat across&lt;/button&gt; 
    &lt;button onclick{{=}}"draw('repeat-y')"&gt;Repeat down&lt;/button&gt; 
    &lt;button onclick{{=}}"draw('no-repeat')"&gt;No Repeat&lt;/button&gt;     
  &lt;canvas id{{=}}"MyCanvas" width{{=}}"600" height{{=}}"500"&gt; &lt;/canvas&gt;
&lt;/body&gt;
&lt;/html&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
If  the ''repetition''  parameter equals null or an empty string,   the '''createPattern''' method assumes that the ''repetition'' parameter is '''repeat'''.
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