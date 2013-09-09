{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Specifies the algorithm used to determine which parts of a graphics element are affected by a fill operation.}}
{{CSS Property
|Initial value=nonzero
|Applies to=Graphics elements that are contained within a <clipPath> element.
|Inherited=Yes
|Media=visual
|Computed value=As specified
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=nonzero
|Description=This value defines whether a point is inside or outside the path by drawing a ray from that point to infinity in any direction and counting the places where a shape segment crosses the ray in a specific direction. When a segment crosses the ray from left to right, the count is incremented; when a segment crosses the ray from right to left, the count is decremented. If the count is zero, the point is outside; if non-zero, it is inside.

See [http://www.w3.org/TR/2011/REC-SVG11-20110816/painting.html#FillRuleProperty SVG fill-rule property] for details.
}}{{CSS Property Value
|Data Type=evenodd
|Description=This value defines whether a point is inside or outside the path by drawing a ray from that point to infinity in any direction and counting the number of  shape segments that the ray crosses. If the count is odd, the point is inside; if even, the point is outside.

See [http://www.w3.org/TR/2011/REC-SVG11-20110816/painting.html#FillRuleProperty SVG fill-rule property] for details.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=In this code fragment, the ''evenodd'' clip-rule type will be applied to the rectangle, because the clip-rule type is specified on the <path> element that defines the clipping shape.
|Code=<clipPath id="MyClip">
  <path d="..." clip-rule="evenodd" />
</clipPath>
<rect clip-path="url(#MyClip)" ... />

}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Masking
|URL=http://dev.w3.org/fxtf/masking/
|Status=Editor's Draft
}}{{Related Specification
|Name=SVG 1.1
|URL=http://www.w3.org/TR/SVG/
|Status=Recommendation
}}
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}