{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Initialized to a Uint8ClampedArray object. The Uint8ClampedArray object must use a Canvas Pixel ArrayBuffer for its storage, and must have a zero start offset and a length equal to the length of its storage, in bytes.}}
{{API_Object_Property
|Property_applies_to=apis/canvas/ImageData
|Read_only=Yes
|Example_object_name=ImageData
|Javascript_data_type=Object
|Return_value_description=Return type Uint8ClampedArray.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=An image is organized by pixels with four values per pixel: red, green, blue, and alpha. To access a specific pixel, use the formula  <code>((canvas.width * y)+ x) *4</code>, where ''x'' and ''y'' are the row and offset in the image.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML Canvas 2D Specification
|URL=http://www.w3.org/TR/2012/CR-2dcontext-20121217/
|Status=W3C Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=Yes
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