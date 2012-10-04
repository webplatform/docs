{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=type|Data type=BSTR|Description=The standard MIME type for  the image format to return. If  you do not specify this parameter, the default  value is a PNG format image.|Optional=}}
{{Method Parameter|Name=jpegquality|Data type=VARIANT|Description=The quality level of a JPEG image in the range of 0.0 to 1.0.|Optional=}}
|Method_applies_to=dom/HTMLCanvasElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=String

The image data.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following code  example draws some graphics on a canvas and then uses '''toDataURL''' to make an image  that  is assigned to an '''img''' object.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt;&lt;html&gt;
&lt;head&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function draw()
{
// Create some graphics.    
  var canvas {{=}} document.getElementById("MyCanvas");
  if (canvas.getContext) 
    {
 	var ctx {{=}} canvas.getContext("2d");
    ctx.fillStyle{{=}}"white";
    ctx.beginPath();
    ctx.rect (5,5,300,250);
    ctx.fill(); 
    ctx.stroke();
    ctx.arc(150,150,100,0,Math.PI, false); 
    ctx.stroke();
    }  
}
function putImage()
{
  var canvas1 {{=}} document.getElementById("MyCanvas");        
  if (canvas1.getContext) {
 	 var ctx {{=}} canvas1.getContext("2d");                // Get the context for the canvas.
     var myImage {{=}} canvas1.toDataURL("image/png");      // Get the data as an image.
  }
  var imageElement {{=}} document.getElementById("MyPix");  // Get the img object.
  imageElement.src {{=}} myImage;                           // Set the src to data from the canvas.
  
}
  &lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"draw()" bgcolor{{=}}"lightgray" &gt;
      &lt;div&gt;
        &lt;button onclick{{=}}"putImage()"&gt;Copy graphic using toDataURL&lt;/button&gt;        
      &lt;/div&gt;
      &lt;div&gt;
        &lt;canvas id{{=}}"MyCanvas" width{{=}}"400" height{{=}}"400" &gt; &lt;/canvas&gt;
      &lt;img id{{=}}"MyPix"&gt;
      &lt;/div&gt;
  &lt;/body&gt;
&lt;/html&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
Typical values for  the ''type''  parameter are <code>image/png</code> or <code>image/jpg</code>.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.10


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[canvas/objects/canvas|canvas]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}