{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Ensures there is a subpath for ''(cp1x, cp1y)'', then connects the last point in the subpath to the given point ''(x, y)'' using a cubic Bézier curve with control points ''(cp1x, cp1y)'' and ''(cp2x, cp2y)'', then adds the point ''(x, y)'' to the subpath.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=cp1x
|Data type=Number
|Description=The x-coordinate of the first Bézier control point.
|Optional=No
}}{{Method Parameter
|Name=cp1y
|Data type=Number
|Description=The y-coordinate of the first Bézier control point.
|Optional=No
}}{{Method Parameter
|Name=cp2x
|Data type=Number
|Description=The x-coordinate of the second Bézier control point.
|Optional=No
}}{{Method Parameter
|Name=cp2y
|Data type=Number
|Description=The y-coordinate of the second Bézier control point.
|Optional=No
}}{{Method Parameter
|Name=x
|Data type=Number
|Description=The x-coordinate of the point to add to the current path.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=Number
|Description=The y-coordinate of the point to add to the current path.
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
|Notes=A cubic Bézier curve  must include  three points. The first two are control points and the third is the ending point for the curve. The first point on the curve is the last point in the existing current subpath. If a path does not exist, use the ''beginPath'' and ''moveTo'' methods to create a starting point.
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