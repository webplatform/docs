{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Connects the last point in the subpath to the given point (x, y) using a straight line, and then adds the point to the subpath.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=Number
|Description=The x-coordinate, in pixels.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=Number
|Description=The y-coordinate, in pixels.
|Optional=No
}}
|Method_applies_to=apis/canvas/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=If subpath is not allocated, the user agent will create it. If subpath has no any point (x, y), then point (x, y) will be created for subpath as its first (and only) point, as if the ''moveTo(x, y)'' method had been called.
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