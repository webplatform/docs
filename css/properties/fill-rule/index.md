{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
|Editorial notes=The SVG property pages will be linked to here.
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The ‘fill-rule’ property indicates the algorithm which is to be used to determine what parts of the canvas are included inside the shape. For a simple, non-intersecting path, it is intuitively clear what region lies "inside"; however, for a more complex path, such as a path that intersects itself or where one subpath encloses another, the interpretation of "inside" is not so obvious.

The ‘fill-rule’ property provides two options for how the inside of a shape is determined:
}}
{{CSS Property
|Initial value=nonzero
|Applies to=shapes and text content elements
|Inherited=Yes
|Media=visual
|Animatable=Yes
|CSS percentages=n/a
|Values={{CSS Property Value
|Data Type=evenodd
}}{{CSS Property Value
|Data Type=inherit
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=nonzero

This rule determines the "insideness" of a point on the canvas by drawing a ray from that point to infinity in any direction and then examining the places where a segment of the shape crosses the ray. Starting with a count of zero, add one each time a path segment crosses the ray from left to right and subtract one each time a path segment crosses the ray from right to left. After counting the crossings, if the result is zero then the point is outside the path. Otherwise, it is inside.
|Code=The following drawing illustrates the nonzero rule:
|LiveURL=http://www.w3.org/TR/SVG/images/painting/fillrule-nonzero.svg
}}{{Single Example
|Language=CSS
|Description=evenodd

This rule determines the "insideness" of a point on the canvas by drawing a ray from that point to infinity in any direction and counting the number of path segments from the given shape that the ray crosses. If this number is odd, the point is inside; if even, the point is outside.
|Code=The following drawing illustrates the evenodd rule:
|LiveURL=http://www.w3.org/TR/SVG/images/painting/fillrule-evenodd.svg
}}
}}
{{Notes_Section
|Usage=The ‘fill-rule’ property indicates the algorithm which is to be used to determine what parts of the canvas are included inside the shape. For a simple, non-intersecting path, it is intuitively clear what region lies "inside"; however, for a more complex path, such as a path that intersects itself or where one subpath encloses another, the interpretation of "inside" is not so obvious.
|Notes=(Note: the above explanations do not specify what to do if a path segment coincides with or is tangent to the ray. Since any ray will do, one may simply choose a different ray that does not have such problem intersections.)
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=SVG
|URL=http://www.w3.org/TR/SVG/painting.html#FillProperties
|Status=W3C Recommendation
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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}