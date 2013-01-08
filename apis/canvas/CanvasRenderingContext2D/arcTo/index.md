{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Ensures there is a subpath for (x1, y1). Then, the behavior depends on the arguments and the last point in the subpath. See Notes.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x1
|Data type=Number
|Description=The x-coordinate for the first tangent that intersects with the current path point.
|Optional=No
}}{{Method Parameter
|Name=y1
|Data type=Number
|Description=The y-coordinate for the first tangent that intersects with the current point.
|Optional=No
}}{{Method Parameter
|Name=x2
|Data type=Number
|Description=The x-coordinate for the second tangent that intersects with  the ''x1'' and ''y1'' points.
|Optional=No
}}{{Method Parameter
|Name=y2
|Data type=Number
|Description=The y-coordinate for the second tangent that intersects with  the ''x1'' and ''y1'' points.
|Optional=No
}}{{Method Parameter
|Name=radius
|Data type=Number
|Description=The radius of the arc to create.
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
{{!}}IndexSizeError
{{!}}The radius given is negative.
{{!}}}

}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=The '''arcTo'''  method creates an arc of ''radius'' radius between two tangents. The first tangent is defined by an imaginary line that is drawn through the last point in a path and the point ''(x1, y1)''. The second tangent is defined by an imaginary line that is drawn through the point ''(x1, y1)'' and the point ''(x2, y2)''.

The arc is drawn between the two tangents using ''radius'' as the radius. '''arcTo''' will draw a straight line from the last point of the path to the start of the arc which lies on the tangent that contains the last point on the path and ''x1'' and ''y1''.

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