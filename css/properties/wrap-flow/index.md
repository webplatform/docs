{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Specifies how exclusions impact inline content within block-level elements}}
{{CSS Property
|Initial value=auto
|Applies to=block-level elements
|Inherited=No
|Media=visual
|Computed value=as specified except for element's whose ‘float’ computed value is not none, in which case the computed value is ‘auto’.
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=auto
|Description=No exclusion is created. Inline flow content interacts with the element as usual.

[[Image:exclusion_wrap_side_auto.png|alt=wrap-flow:auto applied to grid positioned elements;]]
}}{{CSS Property Value
|Data Type=both
|Description=Inline flow content can flow on all sides of the exclusion.

[[Image:exclusion_wrap_side_both.png|alt=wrap-flow:both applied to grid positioned elements;]]
}}{{CSS Property Value
|Data Type=start
|Description=Inline flow content can flow around the start edge of the exclusion area but must leave the area next to the end edge of the exclusion empty.

[[Image:exclusion_wrap_side_left.png|alt=wrap-flow:start applied to grid positioned elements;]]
}}{{CSS Property Value
|Data Type=end
|Description=Inline flow content can flow around the end edge of the exclusion area but must leave the area next to the start edge of the exclusion empty.

[[Image:exclusion_wrap_side_right.png|alt=wrap-flow:end applied to grid positioned elements;]]
}}{{CSS Property Value
|Data Type=minimum
|Description=Inline flow content can flow around the edge of the exclusion with the smallest available space within the flow content's containing block, and must leave the other edge of the exclusion empty.

[[Image:exclusion_wrap_side_minimum.png|alt=wrap-flow:minimum applied to grid positioned elements;]]
}}{{CSS Property Value
|Data Type=maximum
|Description=Inline flow content can flow around the edge of the exclusion with the largest available space within the flow content's containing block, and must leave the other edge of the exclusion empty.

[[Image:exclusion_wrap_side_maximum.png|alt=wrap-flow:maximum applied to grid positioned elements;]]
}}{{CSS Property Value
|Data Type=clear
|Description=Inline flow content can only flow before and after the exclusion in the flow content's block direction and must leave the areas next to the start and end edges of the exclusion empty.

[[Image:exclusion_wrap_side_clear.png|alt=wrap-flow:clear applied to grid positioned elements;]]
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=If the property's computed value is ‘auto’, the element does not become an exclusion.

An exclusion affects the inline flow content descended from the exclusion's containing block and that of all descendant elements of the same containing block. All inline flow content inside the containing block of the exclusions is affected. To stop the effect of exclusions defined outside an element, the  [[css/properties/wrap-through|wrap-through]] property can be used.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Exclusions Module Level 1
|URL=http://dev.w3.org/csswg/css-exclusions/
|Status=Editor's Draft
}}{{Related Specification
|Name=CSS Exclusions Module Level 1
|URL=http://www.w3.org/TR/css3-exclusions/
|Status=Working Draft
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
|Manual_links=See also: [[css/properties/wrap-through|wrap-through]] property
}}
{{Topics|CSS, CSS-Regions}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh772045(v=vs.85).aspx
|HTML5Rocks_link=
}}