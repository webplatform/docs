{{Page Title}}
{{Flags
|State=Not Ready
|Editorial notes=Unreviewed MSDN import
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=svg/objects/SVGElement
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=

===Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

Many SVG graphics operations use '''2&times;3''' matrices.  When you need  a matrix for matrix arithmetic, you can expand a '''2&times;3''' matrix into a '''3&times;3''' matrix equivalent by adding a third row of '''[0 0 1]'''.

|Import_Notes=

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204735 Scalable Vector Graphics: Coordinate Systems, Transformations and Units], Section 7.14.3

===Members===

The '''SVGMatrix''' object has these methods:

*[[svg/methods/flipX|'''flipX''']]: Returns a matrix equivalent to a flip about the x-axis.
*[[svg/methods/flipY|'''flipY''']]: Returns a matrix equivalent to a flip about the y-axis.
*[[svg/methods/inverse|'''inverse''']]: Returns the inverse of this matrix.
*[[svg/methods/multiply|'''multiply''']]: Post-multiplies the matrix by the specified second matrix and returns the resulting matrix.
*[[svg/methods/rotate|'''rotate''']]: Post-multiplies a rotation transformation on the current matrix and returns the resulting matrix.
*[[svg/methods/rotateFromVector|'''rotateFromVector''']]: Post-multiplies the matrix by a specified rotation transformation and returns the resulting matrix.
*[[svg/methods/scale|'''scale''']]: Post-multiplies the matrix by a uniform scale transformation and returns the resulting matrix.
*[[svg/methods/scaleNonUniform|'''scaleNonUniform''']]: Post-multiplies the matrix by a non-uniform scale transformation  and returns the resulting matrix.
*[[svg/methods/skewX|'''skewX''']]: Post-multiplies the matrix by a skew transformation along the x-axis and returns the resulting matrix.
*[[svg/methods/skewY|'''skewY''']]: Post-multiplies the matrix by a skew transformation along the y-axis  and returns the resulting matrix.
*[[svg/methods/translate|'''translate''']]: Post-multiplies the matrix by a translation transformation  and returns the resulting matrix.

The '''SVGMatrix''' object has these properties:

*[[svg/properties/a|'''a''']]: Gets or sets the '''a'''  entry of the '''SVGMatrix'''.
*[[svg/properties/b|'''b''']]: Gets or sets  the '''b'''  entry of the '''SVGMatrix'''.
*[[svg/properties/c|'''c''']]: Gets or sets  the '''c'''  entry of the '''SVGMatrix'''.
*[[svg/properties/d|'''d''']]: Gets or sets  the '''d'''  entry of the '''SVGMatrix'''.
*[[svg/properties/e|'''e''']]: Gets or sets  the '''e'''  entry of the '''SVGMatrix'''.
*[[svg/properties/f|'''f''']]: Gets or sets  the [[svg/properties/f|'''f''']]  entry of the '''SVGMatrix'''.

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}