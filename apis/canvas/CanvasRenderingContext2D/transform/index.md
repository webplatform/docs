{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Replaces the current transformation matrix with the result of multiplying the current transformation matrix with the matrix described by:

<code>a c e<br/>
b d f<br/>
0 0 1<br/>
-----</code>
}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=a
|Data type=any
|Description=The  m1,1  value in the matrix.
|Optional=No
}}{{Method Parameter
|Name=b
|Data type=any
|Description=The  m1,2 value  in the matrix.
|Optional=No
}}{{Method Parameter
|Name=c
|Data type=any
|Description=The  m2,1  value in the matrix.
|Optional=No
}}{{Method Parameter
|Name=d
|Data type=any
|Description=The  m2,2  value in the matrix.
|Optional=No
}}{{Method Parameter
|Name=e
|Data type=any
|Description=The delta x (dx)  value in the matrix.
|Optional=No
}}{{Method Parameter
|Name=f
|Data type=any
|Description=The  delta y (dy)  value in the matrix.
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
|Notes=The parameters of ''transform'' represent a matrix. This matrix is multiplied with the transformation matrix of the current context.

The arguments ''a, b, c, d, e, f'' are sometimes called ''m11, m12, m21, m22, dx, dy'' or ''m11, m21, m12, m22, dx, dy''. Care should be taken in particular with the order of the second and third arguments (''b'' and ''c'') as their order varies from API to API; APIs sometimes use the notation ''m12/m21'' and sometimes ''m21/m12'' for those positions.
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}