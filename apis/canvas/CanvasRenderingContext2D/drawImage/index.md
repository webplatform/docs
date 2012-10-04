{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=pSrc|Data type=IDispatch|Description=An image, canvas, or video element of the pattern to  use.|Optional=}}
{{Method Parameter|Name=sx|Data type=VARIANT|Description=The horizontal starting value (x), in CSS pixels, relative to the source image.|Optional=}}
{{Method Parameter|Name=sy|Data type=VARIANT|Description=The vertical starting value (y), in CSS pixels, relative to the source image.|Optional=}}
{{Method Parameter|Name=sw|Data type=VARIANT|Description=The width of the source image, in CSS pixels, to draw onto the canvas.|Optional=}}
{{Method Parameter|Name=sh|Data type=VARIANT|Description=The height of the source image, in CSS pixels, to draw onto the canvas.|Optional=}}
{{Method Parameter|Name=dx|Data type=VARIANT|Description=The horizontal (x) value, in CSS pixels, where to place the image on the canvas.|Optional=}}
{{Method Parameter|Name=dy|Data type=VARIANT|Description=The vertical (y) value, in CSS pixels, where to place the image on the canvas.|Optional=}}
{{Method Parameter|Name=dw|Data type=VARIANT|Description=The destination width value, in CSS pixels, to use when drawing the image to the canvas.|Optional=}}
{{Method Parameter|Name=dh|Data type=VARIANT|Description=The destination height value, in CSS pixels, to use when drawing the image to the canvas.|Optional=}}
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
|TypeMismatchError
|The pSrc  parameter is not an img object,  canvas element, or video element.
|-
|InvalidStateError _ERR
|The pSrc  parameter does not contain  image data.
|-
|IndexSizeError
|The numeric arguments are not valid  (for example, the destination is a 0x0 rectangle).
|-
|SecurityError
|The img or video element is not of the same origin or domain as the document that owns the canvas element.
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
|TypeMismatchError
|The pSrc  parameter is not an img object,  canvas element, or video element.
|-
|InvalidStateError _ERR
|The pSrc  parameter does not contain  image data.
|-
|IndexSizeError
|The numeric arguments are not valid  (for example, the destination is a 0x0 rectangle).
|-
|SecurityError
|The img or video element is not of the same origin or domain as the document that owns the canvas element.
|}
 


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following code  example draws an image on the canvas by using all three methods.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function draw()
{
  var canvas {{=}} document.getElementById("MyCanvas");
  if (canvas.getContext) {
 	  var ctx {{=}} canvas.getContext("2d");                // Get the context.
      ctx.clearRect(0,0,canvas.width,canvas.height);    // Clear the last image, if it exists.
      var image {{=}} document.getElementById("pix");       // Get the address of the picture.
// Straight draw. 
      ctx.drawImage(image,1,1);                         
// Stretch the image a bit.
      ctx.drawImage(image,125,125,200,200);              
// Draw it in pieces.
      ctx.drawImage(image,1,1, image.width/2, image.height/2 , 50,125,50,50);
      ctx.drawImage(image,1, image.height/2, image.width/2, image.height/2 , 50,275,50,50);
      ctx.drawImage(image,image.width/2, 1, image.width/2, image.height/2 , 350,125,50,50);      
      ctx.drawImage(image,image.width/2, image.height/2, image.width/2, image.height/2 , 350,275,50,50);
    }  
}
  &lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;p&gt;This picture will appear below.&lt;/p&gt;
    &lt;div&gt;
    &lt;img id{{=}}"pix" src{{=}}"http://go.microsoft.com/fwlink/?LinkID{{=}}199028" /&gt;   
    &lt;/div&gt;
    &lt;button onclick{{=}}"draw()"&gt;Draw Images on canvas&lt;/button&gt; 
  &lt;canvas id{{=}}"MyCanvas" width{{=}}"600" height{{=}}"500"&gt; &lt;/canvas&gt;
&lt;/body&gt;
&lt;/html&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''drawImage'''  method provides three ways to draw an image onto a canvas, depending on how you use  the optional parameters:

*drawImage(''pSrc'',''dx'',''dy'')  copies  an image exactly to the canvas at the location  that  the ''dx'' and ''dy'' parameters specify.
*drawImage(''pSrc'',''dx'',''dy'',''dw'',''dh'')  copies  an image to the canvas by using  the ''dw'' and ''dh''  parameters to stretch or reduce the image. This option is similar to the size attributes on an '''img'''  tag.
*drawImage(''pSrc'',''sx'',''sy'',''sw'',''sh''''dx'',''dy'',''dw'',''dh'')  copies  all or part of a source image to the canvas.  You can place and size the destination image  by  using the destination parameters.

If  you do not specify  the ''dw''  and ''dh''  parameters, they  equal the values of ''sw'' and ''sh''. One CSS pixel in the image is treated as one unit in the canvas coordinate space.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 12


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