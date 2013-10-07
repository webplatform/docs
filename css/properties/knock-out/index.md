{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Defines whether an element group is a knock-out group. When a group is set to ''knock-out'', the elements in the group only composite and blend with elements outside the group. When a group is set to ''preserve'' (the default), the elements composite normally and blend with other elements inside and outside the group.}}
{{CSS Property
|Initial value=preserve
|Applies to=All HTML elements. In SVG, it applies to all container elements except ''mask''.
|Inherited=Yes
|Media=visual
|Computed value=As specified.
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=preserve
|Description=Elements in the group composite normally and blend with other elements inside and outside the group.
}}{{CSS Property Value
|Data Type=knock-out
|Description=Elements in the group only composite and blend with elements outside the group.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* knock-out */
div.ko {
    knock-out: knock-out;
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Compositing and Blending Level 1
|URL=http://dev.w3.org/fxtf/compositing-1
|Status=W3C Editor's Draft
}}{{Related Specification
|Name=Compositing and Blending 1.0
|URL=http://www.w3.org/TR/2012/WD-compositing-20120816
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
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}