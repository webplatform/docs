{{Page_Title|border-image-source}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The property <code>border-image-source</code> is used to set the image to be used instead of the border style. If this is set to <code>none</code> the <code>border-style</code> is used instead.}}
{{CSS Property
|Initial value=none
|Applies to=all elements, except table elements where <code>border-collapse: collapse</code> is applied
|Inherited=No
|Media=visual
|Computed value=‘none’ or the image with its URI made absolute
|Animatable=No
|CSS object model property=borderImageSource
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=Default. <code>border-style</code> is used instead.
}}{{CSS Property Value
|Data Type=url(path/to/image.png)
|Description=This value contains a path to an image that you want to apply to the element in question as a background image, using the CSS images syntax, as described at [[css/functions/url()|"CSS images: url()"]].
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=border-image-source: url(path/to/image.png);
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3
|URL=http://www.w3.org/TR/css3-background/#the-border-image-source
|Status=W3C Candidate Recommendation
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
|Topic_clusters=Border
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}