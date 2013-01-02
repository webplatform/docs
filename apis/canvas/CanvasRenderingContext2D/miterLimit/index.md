{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The current miter limit ratio.}}
{{API_Object_Property
|Property_applies_to=apis/canvas/CanvasRenderingContext2D
|Read_only=No
|Example_object_name=CanvasRenderingContext2D
|Javascript_data_type=Number
|Return_value_description=When setting, values that are not finite values greater than zero are ignored.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=The miter length is the distance from the point where two lines meet to the point where two lines that are drawn along the outer edges of the two lines would intersect. If the ratio of these values exceeds the ''miterLimit'' value,  a [[apis/canvas/CanvasRenderingContext2D/lineJoin|lineJoin]] miter style is not drawn.
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