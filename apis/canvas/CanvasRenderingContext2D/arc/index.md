{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Adds the specified arc to the current subpath.}}
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
|Name=radius
|Data type=Number
|Description=The radius or distance from the point (x,y) that the arc's path  follows.
|Optional=No
}}{{Method Parameter
|Name=startAngle
|Data type=Number
|Description=The starting angle, in radians, where 0 is at the 3 o'clock position of the arc's circle.
|Optional=No
}}{{Method Parameter
|Name=endAngle
|Data type=Number
|Description=The ending angle, in radians.
|Optional=No
}}{{Method Parameter
|Name=anticlockwise
|Data type=Number
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
{{Notes_Section
|Notes=If the ''startAngle'' and ''endAngle''  angles are equal,  the '''arc'''  method  creates a circle. To convert degrees to radians use:
 <code>var radians {{=}} degrees * Math.PI/180</code>
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