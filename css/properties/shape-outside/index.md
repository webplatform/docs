{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Wrap text around a given shape using floats.}}
{{CSS Property
|Initial value=auto
|Applies to=floats
|Inherited=No
|Media=visual
|Computed value=computed lengths for <basic-shape>, the absolute URI for <uri>, otherwise as specified
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=auto
|Description=The float area uses the margin box as normal.
}}{{CSS Property Value
|Data Type=<basic-shape>
|Description=The shape is computed based on the values of one of ‘rectangle’, ‘inset-rectangle’, ‘circle’, ‘ellipse’ or ‘polygon’.
}}{{CSS Property Value
|Data Type=<uri>
|Description=If the <uri> references an image, which is CORS-same-origin, the shape is extracted and computed based on the alpha channel of the specified image. If the <uri> does not reference an image or if it references an image which is not CORS-same-origin, the effect is as if the value ‘auto’ had been specified.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This is a working example pulled from the Editor's Draft.
|LiveURL=http://code.webplatform.org/gist/5832982
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Shapes Module Level 1
|URL=http://dev.w3.org/csswg/css-shapes/
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
|External_links=See also: [[css/properties/shape-margin|shape-margin]] property
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}