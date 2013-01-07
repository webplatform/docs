{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Returns a radial CanvasGradient initialized with the two specified circles. This effectively creates a cone, touched by the two circles defined in the creation of the gradient, with the part of the cone before the start circle (0.0) using the color of the first offset, the part of the cone after the end circle (1.0) using the color of the last offset, and areas outside the cone (untouched by the gradient) transparent black.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x0
|Data type=Number
|Description=The x-coordinate of the starting circle of the gradient.
|Optional=No
}}{{Method Parameter
|Name=y0
|Data type=Number
|Description=The y-coordinate of the starting circle of the gradient.
|Optional=No
}}{{Method Parameter
|Name=r0
|Data type=Number
|Description=The radius of the starting circle.
|Optional=No
}}{{Method Parameter
|Name=x1
|Data type=Number
|Description=The x-coordinate of the ending circle of the gradient.
|Optional=No
}}{{Method Parameter
|Name=y1
|Data type=Number
|Description=The y-coordinate of the ending circle of the gradient.
|Optional=No
}}{{Method Parameter
|Name=r1
|Data type=Number
|Description=The radius of the ending circle.
|Optional=No
}}
|Method_applies_to=apis/canvas/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=A CanvasGradient object that represents the radial gradient.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=You can use radial gradients  together  with the  ''fillText'' or ''fillRect'' method.
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