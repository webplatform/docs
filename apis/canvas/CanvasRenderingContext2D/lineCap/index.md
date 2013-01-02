{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Defines the type of endings the user agent will place on the end of lines.}}
{{API_Object_Property
|Property_applies_to=apis/canvas/CanvasRenderingContext2D
|Read_only=No
|Example_object_name=CanvasRenderingContext2D
|Javascript_data_type=String
|Return_value_description=Valid values are:
* "butt"
* "round"
* "square"
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=The ''round'' and ''square'' styles for the ''lineCap''  property make the lines slightly longer. For round ends, the cap diameter equals the  [[apis/canvas/CanvasRenderingContext2D/lineWidth|lineWidth]] value. The ''square'' style adds a rectangle with a width of 1/2 of ''lineWidth''. Both the ''round'' and ''square'' styles add approximately 1/2 of the current ''lineWidth''  value to the end of a line. You should consider this addition if your graphics accuracy is critical.
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