{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Specifies whether an element inherits its parent's wrapping context as defined by the [[css/properties/wrap-flow|wrap-flow]] property.}}
{{CSS Property
|Initial value=wrap
|Applies to=Block-level elements
|Inherited=No
|Media=visual
|Computed value=As specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=wrap
|Description=The element inherits its parent node's wrapping context. Its descendant inline content wraps around exclusions defined outside the element.
}}{{CSS Property Value
|Data Type=none
|Description=The element ignores its parent's wrapping context. Its descendent inline content only wraps around exclusions defined inside this element.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* wrap */
.exelem1 {
wrap-through: wrap;
}

/* none */
.exelem2 {
wrap-through: none;
}
}}
}}
{{Notes_Section
|Usage=Top half of image below illustrates "wrap-through:wrap"; bottom half illustrates "wrap-through:none".

[[Image:exclusion_wrap_through.png|alt=wrap-flow:start applied to grid positioned elements]]
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Exclusions Module Level 1
|URL=http://dev.w3.org/csswg/css-exclusions/
|Status=Editor's Draft
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
|Manual_links=[[css/properties/wrap-flow|wrap-flow]]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}