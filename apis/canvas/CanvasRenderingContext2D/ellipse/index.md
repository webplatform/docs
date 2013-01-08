{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Draws the specified ellipse. If the object's path has any subpaths, this method adds a straight line from the last point in the subpath to the start point of the arc. Then, it adds the start and end points of the arc to the subpath, and connects them with an arc.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=Number
|Description=The x-coordinate, in pixels, for the center point of the arc in relation to the upper-left corner of the canvas rectangle.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=Number
|Description=The y-coordinate, in pixels, for the center point of the arc in relation to the upper-left corner of the canvas rectangle.
|Optional=No
}}{{Method Parameter
|Name=radiusX
|Data type=Number
|Description=The x-coordinate, in pixels, from the point (x,y) that the arc's path  follows.
|Optional=No
}}{{Method Parameter
|Name=radiusY
|Data type=Number
|Description=The y-coordinate, in pixels, from the point (x,y) that the arc's path  follows.
|Optional=No
}}{{Method Parameter
|Name=rotation
|Data type=Number
|Description=The rotation, in radians, the semi-major axis is inclined clockwise from the x-axis.
|Optional=No
}}{{Method Parameter
|Name=startAngle
|Data type=Number
|Description=The starting angle, in radians, where 0 is at the 3 o'clock position of the arc's circle.
|Optional=No
}}{{Method Parameter
|Name=endAngle
|Data type=Number
|Description=The starting angle, in radians.
|Optional=No
}}{{Method Parameter
|Name=anticlockwise
|Data type=Boolean
|Description=''true'': The arc is drawn in a counterclockwise direction from start to end.

''false'': The arc  is drawn in a clockwise direction from start to end.
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
{{!}}The  specified radius value  is negative.
{{!}}}
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section}}
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
{{Topics|Canvas}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}