{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=imagedata|Data type=ICanvasImageData|Description=A [[canvas/objects/CanvasImageData|'''CanvasImageData''']] object with  an image's pixel data.|Optional=}}
{{Method Parameter|Name=dx|Data type=float|Description=The x-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.|Optional=}}
{{Method Parameter|Name=dy|Data type=float|Description=The y-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.|Optional=}}
{{Method Parameter|Name=dirtyX|Data type=VARIANT|Description=The horizontal (x) value, in CSS pixels, where to place  the image on  the canvas.|Optional=}}
{{Method Parameter|Name=dirtyY|Data type=VARIANT|Description=The vertical (y) value, in CSS pixels, where to place  the image on  the canvas.|Optional=}}
{{Method Parameter|Name=dirtyWidth|Data type=VARIANT|Description=The destination width value, in CSS pixels, to use  to  draw  the image to the canvas.|Optional=}}
{{Method Parameter|Name=dirtyHeight|Data type=VARIANT|Description=The destination height value, in CSS pixels to use  to  draw  the image to  the canvas.|Optional=}}
|Method_applies_to=canvas/objects/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code
!Description
|-
|S_OK
|The operation completed successfully.
|-
|NotSupportedError
|One of the parameters is infinite or not a number (NaN).
|-
|TypeMismatchError
|The first parameter is not an CanvasImageData object.
|-
|SecurityError
|The image is not of the same origin or domain as the destination.
|}
 

Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code
!Description
|-
|S_OK
|The operation completed successfully.
|-
|NotSupportedError
|One of the parameters is infinite or not a number (NaN).
|-
|TypeMismatchError
|The first parameter is not an CanvasImageData object.
|-
|SecurityError
|The image is not of the same origin or domain as the destination.
|}
 


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code example creates a graphic, gets the image, and then uses '''putImageData''' to create a copy.
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
function putImage()
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
&lt;body onload{{=}}"draw()" bgcolor{{=}}"lightgray" &gt;
      &lt;div&gt;
        &lt;button onclick{{=}}"putImage()"&gt;Copy graphic using putImage&lt;/button&gt;        
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
You can specify an optional rectangle  to show only those pixels. This  "dirty" rectangle refers to a section of pixels to paint.  You can use this option  to  specify areas on an image that might  change  without repainting the complete image.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 13


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