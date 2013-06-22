{{Page_Title}}
{{Flags
|Content=Examples Needed
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|This property adds a margin to a shape created using the [[css/properties/shape-outside|shape-outside]] property.}}
{{CSS Property
|Initial value=0
|Applies to=floats
|Inherited=No
|Media=visual
|Computed value=the absolute length
|Animatable=Yes
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<length>
|Description=Adds a margin to a shape-outside. This defines a new shape where every point is the specified length from the shape-outside.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following creates a shape that is offset 10 pixels from the fully-opaque pixels in an image.
|Code=shape-outside: url(path/to/image.png);
shape-image-threshold: 1.0;
shape-margin: 10px;
}}
}}
{{Notes_Section
|Notes=The specified <length> must be a positive value.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Shapes Module Level 1
|URL=http://dev.w3.org/csswg/css-shapes/
|Status=Editor's Draft
}}{{Related Specification
|Name=CSS Shapes Module Level 1
|URL=http://www.w3.org/TR/css-shapes/
|Status=First Public Working Draft
}}{{Related Specification
|Name=CSS Values and Units Module Level 3
|URL=http://www.w3.org/TR/css3-values/#lengths
|Status=Candidate Recommendation
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
|Manual_links=* [[css/properties/shape-outside|shape-outside]]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}