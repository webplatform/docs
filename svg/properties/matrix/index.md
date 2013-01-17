{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Topics|SVG}}
{{Notes_Section
|Notes=

===Remarks===

The matrix object is ''live''  (that is, any changes to the [[svg/objects/SVGTransform|'''SVGTransform''']] object are immediately reflected in the matrix object and vice versa). If you change  the matrix object directly (that is, without using the '''SVGTransform''' methods), the '''SVGTransform''' type  changes to SVG_TRANSFORM_MATRIX.

The values in the returned matrix changes based on the type of matrix:

*For a SVG_TRANSFORM_MATRIX matrix, the matrix contains the [[svg/properties/a|'''a''']], [[svg/properties/b|'''b''']], [[svg/properties/c|'''c''']], [[svg/properties/d|'''d''']], [[svg/properties/e|'''e''']], and [[svg/properties/f|'''f''']] values  that  the user supplies.

*For a SVG_TRANSFORM_TRANSLATE matrix, the [[svg/properties/e|'''e''']] and [[svg/properties/f|'''f''']] values represent the translation amounts ([[svg/properties/a|'''a''']]{{=}}1, [[svg/properties/b|'''b''']]{{=}}0, [[svg/properties/c|'''c''']]{{=}}0, and [[svg/properties/d|'''d''']]{{=}}1).

*For a SVG_TRANSFORM_SCALE matrix, the [[svg/properties/a|'''a''']] and [[svg/properties/d|'''d''']] values represent the translation amounts ([[svg/properties/b|'''b''']]{{=}}0, [[svg/properties/c|'''c''']]{{=}}0, [[svg/properties/e|'''e''']]{{=}}0, and [[svg/properties/f|'''f''']]{{=}}0).

*For a SVG_TRANSFORM_ROTATE, SVG_TRANSFORM_SKEWX,  or SVG_TRANSFORM_SKEWY matrix, the [[svg/properties/a|'''a''']], [[svg/properties/b|'''b''']], [[svg/properties/c|'''c''']], and [[svg/properties/d|'''d''']]  values represent the matrix  that causes  the given transformation ([[svg/properties/e|'''e''']]{{=}}0 and [[svg/properties/f|'''f''']]{{=}}0).

|Import_Notes=

===Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204735 Scalable Vector Graphics: Coordinate Systems, Transformations and Units], Section 7.14.4

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/objects/SVGTransform|'''SVGTransform''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]