{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=No
|Editorial notes='''As of time of writing, this property is not yet implemented in most browsers.'''
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|This property sets the mask image or the mask source of an element.}}
{{CSS Property
|Initial value=none
|Applies to=All elements. In SVG, it applies to container elements without the <defs> element and all graphics elements.
|Inherited=No
|Media=visual
|Computed value=As specified, but with URIs made absolute.
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<mask-reference>
|Description=May have the following values:
* none: Counts as an image layer but does not mask the element.
* <image>: A CSS image.
* <mask-source>:
** <url>: A URL reference to a <mask> element, e.g., <code>url(commonmasks.svg#mask)</code>, or to a CSS image.
** child: A keyword indicating that the last direct child <mask> element of the element the mask-image property is applied to should be used as the mask source. It is equivalent to <code>select(mask:last-of-type)</code>.
** <child-selector>: A functional notation accepting a comma-separated list of compound selectors that represents the first matching child <mask> element in DOM tree order.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* CSS gradient */
body { mask-image: linear-gradient(black 0%, transparent 100%) }

/* none */
p { mask-image: none }

/* URL */
div { mask-image: url(dot-mask.png) }
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Masking Level 1
|URL=https://dvcs.w3.org/hg/FXTF/raw-file/default/masking/index.html
|Status=W3C Editor's Draft
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