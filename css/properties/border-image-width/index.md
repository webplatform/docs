{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>border-image-width</code> CSS property defines the offset to use for dividing the border image in nine parts, the top-left corner, central top edge, top-right-corner, central right edge, bottom-right corner, central bottom edge, bottom-left corner, and central right edge. They represent inward distance from the top, right, bottom, and left edges.}}
{{CSS Property
|Initial value=none
|Applies to=all elements, except internal table elements when <code>border-collapse</code> is set to <code>collapse</code>.
|Inherited=No
|Media=visual
|Computed value=all length made absolute, or as specified
|Animatable=No
|CSS object model property=borderImageWidth
|CSS percentages=Relative to the width, for horizontal effects, or the height, for vertical effects, of the border image area.
|Values={{CSS Property Value
|Data Type=<length>
|Description=Represents the length of the image slice. It can be an absolute or relative length. This length must not be negative.
}}{{CSS Property Value
|Data Type=<percentage>
|Description=Represents the percentage of the image slice relative to the height, or width, of the border image area. The percentage must not be negative.
}}{{CSS Property Value
|Data Type=<number>
|Description=Represents a multiple of the computed value of the element's <code>border-width</code> property to be used as the image slice size. The number must not be negative.
}}{{CSS Property Value
|Data Type=auto
|Description=Indicates that the width, or height, of the image size must be the intrinsic size of that dimension.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A simple example showing multiple &lt;div&gt;s, identical in style except that they have different border-image-width properties applied to them.
|Code=&lt;div class="pattern one"&gt;one&lt;/div&gt;
&lt;div class="pattern two"&gt;two&lt;/div&gt;
&lt;div class="pattern three"&gt;three&lt;/div&gt;
&lt;div class="pattern four"&gt;four&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5621387
}}{{Single Example
|Language=CSS
|Code=/* This general class will apply the pattern to the containers */
.pattern {
	border-image-source: url(http://docs.webplatform.org/w/images/d/d8/border-image.png);
	border-image-slice: 30;
	border-image-repeat: repeat;
	border-image-outset: 3;	
}

/* One-value syntax */
.pattern.one{
	border-image-width: 3;
}

/* Two-value syntax */
.pattern.two{
	border-image-width: 1.2em 1.8em;
}

/* Three-value syntax */
.pattern.three{
	border-image-width: 5% 15% 10%;
}

/* Four-value syntax */
.pattern.four{
	border-image-width: 5% 2em 10% auto; 
}
|LiveURL=http://code.webplatform.org/gist/5621387
}}
}}
{{Notes_Section
|Usage=* Up to four different widths can be specified, in the following order: top, right, bottom, left.
* If one width is specified, it is used for all four sides. If two widths are specified, the first is used for the top and bottom borders, and the second is used for left and right borders. If three widths are specified, they are used for top, right/left, and bottom borders, respectively. If left is missing, it is the same as right; if bottom is missing, it is the same as top; if right is missing, it is the same as top.
}}
{{Related_Specifications_Section
|Specifications=
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
|Manual_links=* [[tutorials/css_border_image|Decorating fancy borders with CSS border-image]]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/border-image-width
|MSDN_link=
|HTML5Rocks_link=
}}