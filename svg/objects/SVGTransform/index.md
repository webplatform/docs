{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
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

|Import_Notes=

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204735 Scalable Vector Graphics: Coordinate Systems, Transformations and Units], Section 7.14.4

===Members===

The '''SVGTransform''' object has these methods:

*[[svg/methods/setMatrix|'''setMatrix''']]: Sets the transform type to SVG_TRANSFORM_MATRIX  by using  the specified  new transformation.
*[[svg/methods/setRotate|'''setRotate''']]: Sets the transform type to SVG_TRANSFORM_ROTATE by using  the  specified  rotation angle and   center of rotation.
*[[svg/methods/setScale|'''setScale''']]: Sets the transform type to SVG_TRANSFORM_SCALE by using the  specified scale amounts.
*[[svg/methods/setSkewX|'''setSkewX''']]: Sets the transform type to SVG_TRANSFORM_SKEWX, with the given angle defining the amount of skew.
*[[svg/methods/setSkewY|'''setSkewY''']]: Sets the transform type to SVG_TRANSFORM_SKEWY, with the given angle defining the amount of skew.
*[[svg/methods/setTranslate|'''setTranslate''']]: Sets the transform type  to SVG_TRANSFORM_TRANSLATE  by using the specified components.

The '''SVGTransform''' object has these properties:

*[[svg/properties/angle|'''angle''']]: Gets or sets  a value that indicates an angle unit.
*[[svg/properties/matrix|'''matrix''']]: Gets  the matrix that represents this transformation.
*[[svg/properties/type (SVGTransform)|'''type''']]: Gets or sets the '''transform''' attribute type.

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}