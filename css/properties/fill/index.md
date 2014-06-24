{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add example and compatibility.
The SVG property pages will be linked to here. Needs good examples.
|Checked_Out=No
|High-level issues=Needs Review
|Content=Examples Needed
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The ‘fill’ property paints the interior of the given graphical element. The area to be painted consists of any areas inside the outline of the shape. To determine the inside of the shape, all subpaths are considered, and the interior is determined according to the rules associated with the current value of the ‘fill-rule’ property. The zero-width geometric outline of a shape is included in the area to be painted.}}
{{CSS Property
|Initial value=black
|Applies to=shapes and text content elements
|Inherited=Yes
|Media=visual
|Animatable=Yes
|CSS percentages=n/a
|Values={{CSS Property Value
|Data Type=<paint>
|Description=Properties ‘fill’ and ‘stroke’ take on a value of type <paint>
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=The fill operation fills open subpaths by performing the fill operation as if an additional "closepath" command were added to the path to connect the last point of the subpath with the first point of the subpath. Thus, fill operations apply to both open subpaths within ‘path’ elements (i.e., subpaths without a closepath command) and ‘polyline’ elements.
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