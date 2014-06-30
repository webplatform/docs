{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add description and compatibility.
'''As of time of writing, this property is not yet implemented in most browsers.'''
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Determines the mask painting area, which defines the area that is affected by the mask. The painted content of an element may be restricted to this area.}}
{{CSS Property
|Initial value=border-box
|Applies to=All elements. In SVG, it applies to container elements without the <defs> element and all graphics elements.
|Inherited=No
|Media=visual
|Computed value=As specified.
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=no-clip
|Description=The painted content is not restricted (not clipped). The mask painting area is set to the bounding client rect.
}}{{CSS Property Value
|Data Type=border-box
|Description=The painted content is restricted (clipped) to the border box (painting box for objects without associated layout box).
}}{{CSS Property Value
|Data Type=padding-box
|Description=The painted content is restricted (clipped) to the padding box.
}}{{CSS Property Value
|Data Type=content-box
|Description=The painted content is restricted (clipped) to the content box (object bounding box for objects without associated layout box).
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* border-box */
body {
	background-color: white;
	mask-image: url(big-black-dot.jpg);
        mask-position: bottom right;
	mask-repeat: no-repeat;
        mask-clip: border-box;
	}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Masking Level 1
|URL=http://www.w3.org/TR/css-masking/
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