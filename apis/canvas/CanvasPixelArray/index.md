{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Allows access to each pixel within a canvas's rectangular selection, accessed via the [[canvas/objects/CanvasImageData|'''CanvasImageData''']] object's [[canvas/properties/data|'''data''']] property. The array uses four elements to represent each pixel's red, green, blue, and alpha channels.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Access or edit each pixel within a canvas:
|Code=var cx = document.querySelector('canvas').getContext('2d');
var imgData = cx.getImageData(0, 0, cx.canvas.width, cx.canvas.height);
var data = imgData.data; // data is CanvasPixelArray
var r,g,b,a;
for (var i = 0; l = data.length; i += 4) {
   // editable data is available as an integer less than 256.
   r = data[i];
   g = data[i+1];
   b = data[i+2];
   a = data[i+3];
}
}}
}}
{{Notes_Section
|Notes====Remarks===
A common task is to use values returned from a mouse or pointer event to calculate a pixel value of an canvas image that the user clicked or touched. Mouse or pointer events in Internet Explorer 10 on Windows 8return sub-pixel values that return incorrect data when used in pixel lookup calculations in a '''CanvasPixelArray'''.
For example, to calculate the colors of a pixel clicked on an image, use the formula <code>var ix {{=}} ((mouse.offsetY * canvas.width)+ mouse.offsetX)*4;</code>. The ix value is used as an index into the [[canvas/objects/CanvasImageData|'''CanvasImageData''']] array. The first index value   is the red value, followed by  green (ix+1), blue (ix + 2), and alpha (ix+3).
Windows 7  returns  mouse coordinates as  integers, such as "offsetY {{=}} 220", and "offsetX {{=}} 135", so the calculation works correctly with an index of 352540. However, in Windows 8, a mouse click event  returns "offsetY {{=}} 220.3441", and "offsetX {{=}} 135.4432", on a canvas that's 400 pixels wide, the index is  index of 353092.3328. If this index is used to look up a pixel value, it returns an undefined value.
Even when the calculated number is rounded to an integer value (353092), it returns the incorrect pixel.  By rounding individual mouse offset values to 220 and 135, the result is an index value of 352540, the correct pixel is returned. The following example shows a way to avoid rounding errors:
 <code>
 canvas.onclick {{=}} function(mouse){
 var mouseX {{=}} parseInt(mouse.offsetX); // round each value to an int
 var mouseY {{=}} parseInt(mouse.offsetY);
 var ix {{=}} ((mouseY * canvas.width)+mouseX)*4;  // calculate index 
 // use ix to lookup pixel value in imageData array
 }</code>
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 1


===Members===
The '''CanvasPixelArray''' object has these types of members:
*[#properties Properties]


====Properties====
The '''CanvasPixelArray''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[canvas/properties/length|'''length''']]
|Gets or sets the number of pixel entries in a '''CanvasPixelArray''' object.
|}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[canvas/properties/data|data]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}