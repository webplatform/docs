{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|This property allows you to define the origin of the transformation axes relative to the element on which the transformation is applied.}}
{{CSS Property
|Initial value=50% 50% 0
|Applies to=transformable elements
|Inherited=No
|Media=visual
|Computed value=The transformation origin is always calculated relative to the top-left corner of the transformed element. Named positions are converted to the equivalent percentage values. Percentage values are based on the relevant axis of the element's bounding box.
|Animatable=Yes
|Values={{CSS Property Value
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
For more information about the supported length units,
see CSS Values and Units.
}}{{CSS Property Value
|Data Type=percentage
|Description=A number, followed by a %.
The value is a percentage of the bounding box width (for the x-axis) or the bounding box height (for the y-axis, if specified). A percentage cannot be applied to the z-axis.
}}{{CSS Property Value
|Data Type=named-position
|Description=A named position along the specified axis, each of which has a percentage equivalent.
The values <code>left</code>, <code>center</code>, and <code>right</code> are valid for the x-axis and are equivalent to 0%, 50%, and 100% respectively. The values <code>top</code>, <code>center</code>, and <code>bottom</code> are valid for the y-axis and are equivalent to 0%, 50%, and 100% respectively. There are no named positions along the z-axis.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The origin may be moved along all three axes with this single property by specifying the relative position of each axis in the following order: <code>x-axis y-axis z-axis</code>. The grid complies with the right-hand rule for Cartesian coordinate systems. The x-axis increases from left to right; the y-axis increases from top to bottom; and the z-axis increases away from the user (higher z-values are more distant).

The version of this property using a vendor prefix, '''-ms-transform-origin''', has been deprecated in Internet Explorer 10 and later. To ensure compatibility in the future, applications using this property with a vendor prefix should be updated accordingly. However, be aware that '''-ms-transform-origin''' is the only form of this property that is recognized by Windows Internet Explorer 9, which supports 2-D Cascading Style Sheets (CSS) transforms.

If the '''transform-origin''' property is not set, the transform begins in the center (equal to a '''transform-origin''' value of <code>50% 50%</code>).
If only one value is specified, the second value is assumed to be <code>center</code>.

3-D transforms are only supported in Internet Explorer 10 and later.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223145 CSS Transforms Module, Level 3], Section 8
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Yes (-webkit)
|Chrome_prefixed_version=2.0 (17.0 for 3D)
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Yes (-moz)
|Firefox_prefixed_version=3.5 (10.0 for 3D)
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=Yes (-ms)
|Internet_explorer_prefixed_version=9.0 (10.0 for 3D)
|Opera_supported=Yes
|Opera_version=12.10
|Opera_prefixed_supported=Yes (-o)
|Opera_prefixed_version=10.5 (no support for 3D)
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Yes (-webkit)
|Safari_prefixed_version=3.1 (4.0 for 3D)
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Transforms
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}