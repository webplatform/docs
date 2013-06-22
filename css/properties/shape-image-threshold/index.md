{{Page_Title}}
{{Flags
|Content=Examples Needed
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Defines the alpha channel threshold used to extract a shape from an image.}}
{{CSS Property
|Initial value=0.5
|Applies to=floats
|Inherited=No
|Media=visual
|Animatable=Yes
|CSS percentages=alpha channel of the image specified by <uri>
|Values={{CSS Property Value
|Data Type=<alphavalue>
|Description=A <number> value used to set the threshold used for extracting a shape from an image. Any values outside the range 0.0 (fully transparent) to 1.0 (fully opaque) will be clamped to this range.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=Example from Editor's Draft
|LiveURL=http://code.webplatform.org/gist/5833790
}}{{Single Example
|Language=CSS
|Description=Extract a shape from an image by subtracting all pixels less than 25% opacity
|Code=shape-image-threshold: 0.25;
}}
}}
{{Notes_Section
|Usage=Currently implemented as an experimental feature in WebKit and Blink. This can be used with a -webkit- prefix in WebKit nightly builds and with a -webkit- prefix in Chrome Canary builds with experimental-webkit-features enabled: chrome://flags/#enable-experimental-webkit-features
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Shapes Module Level 1
|URL=http://dev.w3.org/csswg/css-shapes/#shape-image-threshold-property
|Status=Editor's Draft
}}{{Related Specification
|Name=CSS Shapes Module Level 1
|URL=http://www.w3.org/TR/css-shapes/
|Status=First Public Working Draft
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
|Manual_links=See also: [[css/properties/shape-outside|shape-outside]] property
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}