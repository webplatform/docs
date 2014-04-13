{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{Summary_Section|The <code>&lt;image></code> CSS data type represents graphical content.  Images are usually specified with the <code>url()</code> function, but may also be created with a gradient function.  Other syntaxes are defined but not widely implemented.}}
{{Data_Type_Page
|Content=In CSS, images may be used as property values for backgrounds, borders, custom list bullets and for pseudo-element content.  The <code>&lt;image></code> data type is introduced in CSS3; in CSS 2.1 and earlier the only way to specify an image was with the [[css/functions/url()|<code>url()</code> function]] and so the <code>&lt;uri></code> data type was sufficient.

The [http://www.w3.org/TR/css3-images CSS Image Values and Replaced Content Module] defines four ways in which an image may be specified:

* as a reference to an image file (or SVG file fragment), specified using the same syntax as the [[css/data_types/url|<code>&lt;url></code>]] data type;

* as a gradient, using one of the four CSS gradient functions ([[css/functions/linear-gradient|<code>linear-gradient()</code>]], [[css/functions/radial-gradient|<code>radial-gradient()</code>]], [[css/functions/repeating-linear-gradient|<code>repeating-linear-gradient()</code>]], or [[css/functions/repeating-radial-gradient|<code>repeating-radial-gradient()</code>]]);

* as a reference to a mark-up element on the page, specified using the [[css/functions/element|<code>element(#id)</code> function]]; the "live" displayed state of that element would be copied into the property referencing this image.

* as a list of one or more image options, specified with the [[css/functions/image|<code>image()</code> function]].   The parameters to the function are a list of comma-separated values, starting with the value preferred image and (optionally) followed by various fallback alternatives.   Each image value could be given as absolute or relative file paths, possibly including [http://www.w3.org/TR/media-frags/#naming-space media fragment identifiers] to clip the image, or an element or gradient function.  As a final fallback, the last parameter to the <code>image()</code> function could be a solid [[css/data_types/color|<code>&lt;color></code>]] value.

Only the first two options are commonly implemented, and even browsers that support gradients as images may not support them for all image properties.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Values and Units Module Level 3
|URL=http://www.w3.org/TR/css3-values/#images
|Status=Candidate Recommendation
}}{{Related Specification
|Name=CSS Image Values and Replaced Content Module Level 3
|URL=http://www.w3.org/TR/css3-images/#image-values
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
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}