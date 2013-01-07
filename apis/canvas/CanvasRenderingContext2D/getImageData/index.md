{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Returns an ImageData object representing the underlying pixel data for the area of the canvas denoted by the rectangle whose corners are the four points (sx, sy), (sx+sw, sy), (sx+sw, sy+sh), (sx, sy+sh), in canvas coordinate space units.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=sx
|Data type=Number
|Description=The x-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.
|Optional=No
}}{{Method Parameter
|Name=sy
|Data type=Number
|Description=The y-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.
|Optional=No
}}{{Method Parameter
|Name=sw
|Data type=Number
|Description=The width, in pixels, of the rectangle in relation to the coordinates of the canvas.
|Optional=No
}}{{Method Parameter
|Name=sh
|Data type=Number
|Description=The height, in pixels, of the rectangle in relation to the coordinates of the canvas.
|Optional=No
}}
|Method_applies_to=apis/canvas/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''ICanvasImageData'''

A ''CanvasImageData'' object with pixel information from the canvas within the specified coordinates.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=If the rectangle contains pixels outside the canvas, they are returned as transparent black. Pixels are returned as non-premultiplied alpha values.
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