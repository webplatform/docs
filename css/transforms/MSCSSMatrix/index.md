{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Needs title, spec reference, standardization status, fix table coding in Notes
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223140 CSS Transitions Module Level 3], Section 10.1


===Members===
The '''MSCSSMatrix''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''MSCSSMatrix''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[css/cssom/MSCSSMatrix/methods/inverse|'''inverse''']]
|Returns a new matrix that is the inverse of the current matrix.
|-
|[[css/cssom/MSCSSMatrix/methods/multiply|'''multiply''']]
|Returns a new matrix that is the result of current matrix multiplied by the input matrix.
|-
|[[css/properties/-ms-repeating-radial-gradient|'''multiplyLeft''']]
|Returns a new matrix that is the result of input matrix multiplied by the current matrix.
|-
|[[css/cssom/MSCSSMatrix/methods/rotate|'''rotate''']]
|Returns a new matrix that is the result of the current matrix multiplied by the rotation matrix corresponding to the input parameters.
|-
|[[css/cssom/MSCSSMatrix/methods/rotateAxisAngle|'''rotateAxisAngle''']]
|Returns a new matrix that is the result of the current matrix multiplied by the rotation matrix with the given axis and angle.
|-
|[[css/cssom/MSCSSMatrix/methods/scale|'''scale''']]
|Returns a new matrix that is the result of the current matrix multiplied by the scale matrix that corresponds to the input parameters.
|-
|[[css/cssom/MSCSSMatrix/methods/setMatrixValue|'''setMatrixValue''']]
|Replaces an existing matrix with the computed matrix that corresponds to the input.
|-
|[[css/cssom/MSCSSMatrix/methods/skew|'''skew''']]
|Returns a new matrix that is the result of the current matrix multiplied by the skew matrix that corresponds to the input parameters.
|-
|[[css/cssom/MSCSSMatrix/methods/skewX|'''skewX''']]
|Specifies a 2-D skew transformation along the ''x''-axis by the given angle.
|-
|[[css/cssom/MSCSSMatrix/methods/skewY|'''skewY''']]
|Specifies a 2-D skew transformation along the ''y''-axis by the given angle.
|-
|[[css/cssom/MSCSSMatrix/methods/toString|'''toString''']]
|Returns a string that corresponds to the matrix.
|-
|[[css/transforms/MSCSSMatrix/translate|'''translate''']]
|Returns a new matrix that is the result of the current matrix multiplied by a translation matrix that contains the input parameters.
|}
 

====Properties====
The '''MSCSSMatrix''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[css/MSCSSMatrix/apis/properties/a|'''a''']]
|Gets or sets the same value as the [[css/cssom/MSCSSMatrix/properties/m11|'''m11''']] property.
|-
|[[css/cssom/MSCSSMatrix/properties/b|'''b''']]
|Gets or sets the same value as the [[css/cssom/MSCSSMatrix/properties/m21|'''m21''']] property.
|-
|[[css/cssom/MSCSSMatrix/properties/c|'''c''']]
|Gets or sets the same value as the [[css/cssom/MSCSSMatrix/properties/m12|'''m12''']] property.
|-
|[[css/cssom/MSCSSMatrix/properties/d|'''d''']]
|Gets or sets the same value as the [[css/cssom/MSCSSMatrix/properties/m22|'''m22''']] property.
|-
|[[css/cssom/MSCSSMatrix/properties/e|'''e''']]
|Gets or sets the same value as the [[css/cssom/MSCSSMatrix/properties/m13|'''m13''']] property.
|-
|[[css/cssom/MSCSSMatrix/properties/f|'''f''']]
|Gets or sets the same value as the [[css/cssom/MSCSSMatrix/properties/m23|'''m23''']] property.
|-
|[[css/cssom/MSCSSMatrix/properties/m11|'''m11''']]
|Gets or sets the value in the first column of the first row of the 4×4 matrix.
|-
|[[css/cssom/MSCSSMatrix/properties/m12|'''m12''']]
|Gets or sets the value in the second column of the first row of the 4×4 matrix.
|-
|[[css/cssom/MSCSSMatrix/properties/m13|'''m13''']]
|Gets or sets the value in the third column of the first row of the 4×4 matrix.
|-
|[[css/cssom/MSCSSMatrix/properties/m14|'''m14''']]
|Gets or sets the value in the fourth column of the first row of the 4×4 matrix.
|-
|[[css/cssom/MSCSSMatrix/properties/m21|'''m21''']]
|Gets or sets the value in the first column of the second row of the 4×4 matrix.
|-
|[[css/cssom/MSCSSMatrix/properties/m22|'''m22''']]
|Gets or sets the value in the second column of the second row of the 4×4 matrix.
|-
|[[css/cssom/MSCSSMatrix/properties/m23|'''m23''']]
|Gets or sets the value in the third column of the second row of the 4×4 matrix.
|-
|[[css/cssom/MSCSSMatrix/properties/m24|'''m24''']]
|Gets or sets the value in the fourth column of the second row of the 4×4 matrix.
|-
|[[css/cssom/MSCSSMatrix/properties/m31|'''m31''']]
|Gets or sets the value in the first column of the third row of the 4×4 matrix.
|-
|[[css/cssom/MSCSSMatrix/properties/m32|'''m32''']]
|Gets or sets the value in the second column of the third row of the 4×4 matrix.
|-
|[[css/cssom/MSCSSMatrix/properties/m33|'''m33''']]
|Gets or sets the value in the third column of the third row of the 4×4 matrix.
|-
|[[css/cssom/MSCSSMatrix/properties/m34|'''m34''']]
|Gets or sets the value in the fourth column of the third row of the 4×4 matrix.
|-
|[[css/cssom/MSCSSMatrix/properties/m41|'''m41''']]
|Gets or sets the value in the first column of the fourth row of the 4×4 matrix.
|-
|[[css/cssom/MSCSSMatrix/properties/m42|'''m42''']]
|Gets or sets the value in the second column of the fourth row of the 4×4 matrix.
|-
|[[css/cssom/MSCSSMatrix/properties/m43|'''m43''']]
|Gets or sets the value in the third column of the fourth row of the 4×4 matrix.
|-
|[[css/cssom/MSCSSMatrix/properties/m44|'''m44''']]
|Gets or sets the value in the fourth column of the fourth row of the 4×4 matrix.
|}
 
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_css\ie]:%20MSCSSMatrix object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Transforms
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}