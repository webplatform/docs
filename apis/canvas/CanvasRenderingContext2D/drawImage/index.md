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
|Not_required=No
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
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=22.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=15.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=5.0-7.0 (partial)
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|API, Canvas}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}