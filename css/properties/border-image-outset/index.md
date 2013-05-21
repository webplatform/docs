{{Page_Title|border-image-outset}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>border-image-outset</code> property describes, by which amount the border image area extends beyond the border box.

[[File:bi-outset.png|border-outset visualized]]
}}
{{CSS Property
|Initial value=0
|Applies to=all elements, except internal table elements when <code>border-collapse</code> is set to <code>collapse</code>.
|Inherited=No
|Media=visual
|Computed value=all length made absolute, otherwise as specified
|Animatable=No
|CSS object model property=borderImageOutset
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<length>
|Description=Floating-point number, followed by an absolute units designator (cm, mm, in, pt, or pc) or a relative units designator (em, ex, or px). For more information about the supported length units, see CSS Values and Units Reference (Length). This length must not be negative.
}}{{CSS Property Value
|Data Type=inherit
|Description=Is a keyword indicating that all four values are inherited from their parent's element calculated value.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A simple example showing multiple &lt;div&gt;s, identical in style except that they have different border-image-outset properties applied to them.
|Code=&lt;div class="pattern one"&gt;one&lt;/div&gt;
&lt;div class="pattern two"&gt;two&lt;/div&gt;
&lt;div class="pattern three"&gt;three&lt;/div&gt;
&lt;div class="pattern four"&gt;four&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5622268
}}{{Single Example
|Language=CSS
|Code=/* This general class will apply the pattern to the containers */
.pattern {
	border-image-source: url(http://docs.webplatform.org/w/images/d/d8/border-image.png);
	border-image-slice: 30;
	border-image-width: 6;
	border-image-repeat: repeat;

}

/* One-value syntax */
.pattern.one{
	border-image-outset: 3;
}

/* Two-value syntax */
.pattern.two{
	border-image-outset: 1.2em 1.8em;
}

/* Three-value syntax */
.pattern.three{
	border-image-outset: 5px 3px 10px;
}

/* Four-value syntax */
.pattern.four{
	border-image-outset: 5 2em 10 3px; 
}
|LiveURL=http://code.webplatform.org/gist/5622268
}}
}}
{{Notes_Section
|Usage=* Up to four different values can be specified, in the following order: top, right, bottom, left.
* If one value is specified, it is used for all four sides. If two values are specified, the first is used for the top and bottom borders, and the second is used for left and right borders. If three values are specified, they are used for top, right/left, and bottom borders, respectively. If left is missing, it is the same as right; if bottom is missing, it is the same as top; if right is missing, it is the same as top.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3
|URL=http://www.w3.org/TR/css3-background/#the-border-image-outset
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
|Manual_links=* [[tutorials/css_border_image|Decorating fancy borders with CSS border-image]]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/border-image-outset
|MSDN_link=
|HTML5Rocks_link=
}}