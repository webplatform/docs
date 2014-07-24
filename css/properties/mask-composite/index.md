{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Add description and compatibility.
'''As of time of writing, this property is not yet implemented in most browsers.'''
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Last Call Working Draft}}
{{API_Name}}
{{Summary_Section|This property allows to composite multiple mask layers define by [[css/properties/mask-image|mask-image]] with different Poter-Duff compositing modes.}}
{{CSS Property
|Initial value=add
|Applies to=All elements. In SVG, it applies to container elements without the <defs> element and all graphics elements.
|Inherited=No
|Media=visual
|Computed value=As specified
|Animatable=no
|Values={{CSS Property Value
|Data Type=add
|Description=The mask image layer closer to the user is placed above the next mask image layer.
}}{{CSS Property Value
|Data Type=subtract
|Description=The mask image layer closer to the user is placed where it falls outside of the next mask image layer.
}}{{CSS Property Value
|Data Type=intersect
|Description=The parts of the mask image layer closer to the user that overlap the next mask image layer replace the parts of the next mask image layer.
}}{{CSS Property Value
|Data Type=exclude
|Description=The non-overlaping parts of the mask image layer closer to the user and the next mask image layer are combined.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* The two mask layers are composited with the operation 'exclude' */
mask-image: url(source.png), url(destination.png);
mask-composite: exclude;
}}{{Single Example
|Language=CSS
|Code=/* destination.png and background.png are combined
with the compositing operator subtract.
The result of this operation and source.png are combined
with the compositing operator exclude. */
mask-image: url(source.png), url(destination.png), url(background.png);
mask-composite: exclude, subtract;
}}{{Single Example
|Language=CSS
|Code=/* Just one mask layer is specified. No compositing operation will happen. */
mask-image: url(source.png);
mask-composite: exclude;
}}
}}
{{Notes_Section
|Usage=Safari, Chrome and Opera implement this property '-webkit-' prefixed with different keywords. The keywords can be mapped as follows:

add &#8594; source-over,
subtract &#8594; source-out,
intersect &#8594; source-in,
exclude &#8594; xor
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Masking Level 1
|URL=http://www.w3.org/TR/css-masking-1/
|Status=W3C Last Call Working Draft
}}{{Related Specification
|Name=CSS Masking Level 1
|URL=http://dev.w3.org/fxtf/css-masking-1/
|Status=W3C Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=Yes
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