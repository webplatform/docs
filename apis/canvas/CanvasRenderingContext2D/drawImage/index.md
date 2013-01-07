{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Draws the specified image onto the canvas. Can be called in three ways; see Notes.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=image
|Data type=DOM Node
|Description=An image, canvas, or video element of the pattern to  use.
|Optional=No
}}{{Method Parameter
|Name=sx
|Data type=Number
|Description=The horizontal starting value (x), in CSS pixels, relative to the source image.
|Optional=No
}}{{Method Parameter
|Name=sy
|Data type=Number
|Description=The vertical starting value (y), in CSS pixels, relative to the source image.
|Optional=No
}}{{Method Parameter
|Name=sw
|Data type=Number
|Description=The width of the source image, in CSS pixels, to draw onto the canvas.
|Optional=No
}}{{Method Parameter
|Name=sh
|Data type=Number
|Description=The height of the source image, in CSS pixels, to draw onto the canvas.
|Optional=No
}}{{Method Parameter
|Name=dx
|Data type=Number
|Description=The horizontal (x) value, in CSS pixels, where to place the image on the canvas.
|Optional=No
}}{{Method Parameter
|Name=dy
|Data type=Number
|Description=The vertical (y) value, in CSS pixels, where to place the image on the canvas.
|Optional=No
}}{{Method Parameter
|Name=dw
|Data type=Number
|Description=The destination width value, in CSS pixels, to use when drawing the image to the canvas.
|Optional=No
}}{{Method Parameter
|Name=dh
|Data type=Number
|Description=The destination height value, in CSS pixels, to use when drawing the image to the canvas.
|Optional=No
}}
|Method_applies_to=apis/canvas/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{{{!}} class="wikitable"
{{!}}-
!Return code
!Description
{{!}}-
{{!}}S_OK
{{!}}The operation completed successfully.
{{!}}-
{{!}}TypeMismatchError
{{!}}The ''image''  parameter is not an img object,  canvas element, or video element.
{{!}}-
{{!}}InvalidStateError _ERR
{{!}}The ''image''  parameter does not contain  image data.
{{!}}-
{{!}}IndexSizeError
{{!}}The numeric arguments are not valid  (for example, the destination is a 0x0 rectangle).
{{!}}-
{{!}}SecurityError
{{!}}The img or video element is not of the same origin or domain as the document that owns the canvas element.
{{!}}}
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=The '''drawImage'''  method provides three ways to draw an image onto a canvas, depending on how you use  the optional parameters:

*drawImage(''image'',''dx'',''dy'')  copies  an image exactly to the canvas at the location  that  the ''dx'' and ''dy'' parameters specify.
*drawImage(''image'',''dx'',''dy'',''dw'',''dh'')  copies  an image to the canvas by using  the ''dw'' and ''dh''  parameters to stretch or reduce the image. This option is similar to the size attributes on an '''img'''  tag.
*drawImage(''image'',''sx'',''sy'',''sw'',''sh'',''dx'',''dy'',''dw'',''dh'') copies  all or part of a source image to the canvas. You can place and size the destination image by  using the destination parameters.

If  you do not specify  the ''dw''  and ''dh''  parameters, they  equal the values of ''sw'' and ''sh''. One CSS pixel in the image is treated as one unit in the canvas coordinate space.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML Canvas 2D Specification
|URL=http://www.w3.org/TR/2012/CR-2dcontext-20121217/
|Status=W3C Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Canvas}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}