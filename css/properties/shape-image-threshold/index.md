{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Defines the alpha channel threshold used to extract a shape from an image. Can be thought of as a "minimum opacity" threshold; that is, a value of 0.5 means that the shape will enclose all the pixels that are more than 50% opaque.}}
{{CSS Property
|Initial value=0.0
|Applies to=Floats
|Inherited=No
|Media=visual
|Computed value=As specified, clamped to a 0.0-1.0 range
|Animatable=Yes
|CSS percentages=Alpha channel of the image specified by [[css/properties/shape-outside|shape-outside]].
|Values={{CSS Property Value
|Data Type=<threshold>
|Description=A numeric value used to set the opacity threshold used for extracting a shape from an image. Any values outside the range 0.0 (fully transparent) to 1.0 (fully opaque) will be clamped to this range.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Note: Depends upon an image previously specified by [[css/properties/shape-outside|shape-outside]].
|Code=/*
Extract a shape from an image by enclosing all pixels greater than 25% opacity
*/
#myimg {
  shape-image-threshold: 0.25;
}
|LiveURL=http://code.webplatform.org/gist/5833790
}}
}}
{{Notes_Section
|Usage=Currently implemented as an experimental feature in WebKit and Blink. This can be used with a -webkit- prefix in WebKit nightly builds and with a -webkit- prefix in Chrome Canary builds with experimental-webkit-features enabled: chrome://flags/#enable-experimental-webkit-features
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Shapes Module Level 1
|URL=http://dev.w3.org/csswg/css-shapes
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
|Manual_links=[[css/properties/shape-outside|shape-outside]]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}