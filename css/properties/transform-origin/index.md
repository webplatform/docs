{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|This property defines the origin of the transformation axes relative to the element to which the transformation is applied.}}
{{CSS Property
|Initial value=50% 50%
|Applies to=Transformable elements.
|Inherited=No
|Media=visual
|Computed value=For <length>, the absolute value; otherwise a percentage.
|Animatable=Yes
|CSS percentages=Refer to the size of the element's bounding box.
|Values={{CSS Property Value
|Data Type=percentage
|Description=A number, followed by a %.
The value is a percentage of the bounding box width (for the X axis) or the bounding box height (for the Y axis, if specified). A percentage cannot be applied to the Z axis.
}}{{CSS Property Value
|Data Type=length
|Description=A floating-point number, followed by a unit of measurement.
Units of measurement may be absolute (<code>cm</code>,
<code>mm</code>,
<code>in</code>,
<code>pt</code>,
or <code>pc</code>)
or relative
(<code>em</code>,
<code>ex</code>,
or <code>px</code>).
}}{{CSS Property Value
|Data Type=<named-position>
|Description=A named position along the specified axis, each of which has a percentage equivalent.
The values <code>left</code>, <code>center</code>, and <code>right</code> are valid for the X axis and are equivalent to 0%, 50%, and 100% respectively. The values <code>top</code>, <code>center</code>, and <code>bottom</code> are valid for the Y axis and are equivalent to 0%, 50%, and 100% respectively. There are no named positions along the Z axis.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=The origin may be moved along all three axes with this single property by specifying the relative position of each axis in X, Y, Z order. The grid complies with the right-hand rule for Cartesian coordinate systems. The x-axis increases from left to right; the y-axis increases from top to bottom; and the z-axis increases away from the user (higher z-values are more distant).

Microsoft deprecated <code>-ms-transform-origin</code>, the vendor-prefixed version of this property, with the release of Internet Explorer 10. It should only be included for compatibility with earlier versions.

If the <code>transform-origin</code> property is not set, the transform begins in the center at screen level (equal to a <code>transform-origin</code> value of <code>50% 50% 0</code>).
* If fewer than three values are provided, the third value (z-axis) is assumed to be <code>0</code> (screen level).
* If only one value is specified, the second value (y-axis) is assumed to be <code>50%</code>.

}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Transforms Module Level 3
|URL=http://www.w3.org/TR/css3-transforms
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/transforms/transform|transform]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}