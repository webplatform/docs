{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes={{Editorial/Move_Candidate
| Probably should be under HTML5 canvas element. See [http://www.w3.org/html/wg/drafts/html/master/single-page.html#the-canvas-element HTML5 specification].
}}
|Checked_Out=No
|High-level issues=Move Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=
|Name=type
|Data type=any
|Description=The standard MIME type for  the image format to return. If  you do not specify this parameter, the default  value is a PNG format image.
|Optional=No
}}{{Method Parameter
|Index=
|Name=jpegquality
|Data type=any
|Description=The quality level of a JPEG image in the range of 0.0 to 1.0.
|Optional=No
}}
|Method_applies_to=dom/HTMLCanvasElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=String

The image data.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=The following code  example draws some graphics on a canvas and then uses '''toDataURL''' to make an image  that  is assigned to an '''img''' object.
|Code=&lt;!DOCTYPE html&gt;&lt;html&gt;
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
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
Typical values for  the ''type''  parameter are <code>image/png</code> or <code>image/jpg</code>.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.10
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[canvas/objects/canvas|canvas]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}