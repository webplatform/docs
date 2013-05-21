{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The border-image-slice CSS property divides the image specified by border-image-source in nine regions: the four corners, the four edges and the middle. It does this by specifying 4 inwards offsets.

[[File:slice.png|slicing]]
}}
{{CSS Property
|Initial value=100%
|Applies to=all elements, except internal table elements when <code>border-collapse</code> is set to <code>collapse</code>.
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=borderImageSlice
|CSS percentages=refer to size of the border image
|Values={{CSS Property Value
|Data Type=<number>
|Description=Represents pixels for raster images and coordinates for vector images.
}}{{CSS Property Value
|Data Type=<percentage>
|Description=Percentages values are relative to the height or width of the image, whichever is adequate.
}}{{CSS Property Value
|Data Type=fill
|Description=Is a keyword whose presence forces the use of the middle image slice to be displayed over the background image, its size and height are resized like those of the top and left image slices, respectively.
}}{{CSS Property Value
|Data Type=inherit
|Description=Is a keyword indicating that all four values are inherited from their parent's element calculated value.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A simple example showing multiple &lt;div&gt;s, identical in style except that they have different border-image-slice properties applied to them.
|Code=&lt;div class="pattern one"&gt;one&lt;/div&gt;
&lt;div class="pattern two"&gt;two&lt;/div&gt;
&lt;div class="pattern three"&gt;three&lt;/div&gt;
&lt;div class="pattern four"&gt;four&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5622431
}}{{Single Example
|Language=CSS
|Code=/* This general class will apply the pattern to the containers */
.pattern {
	border-image-source: url(http://docs.webplatform.org/w/images/d/d8/border-image.png);
	border-image-width: 6;
	border-image-outset: 3;
	border-image-repeat: repeat;

}

/* One-value syntax */
.pattern.one{
	border-image-slice: 30;
}

/* Two-value syntax */
.pattern.two{
	border-image-slice: 30 20;
}

/* Three-value syntax */
.pattern.three{
	border-image-slice: 20 15 30;
}

/* Four-value syntax */
.pattern.four{
	border-image-slice: 25 20 30 15; 
}
|LiveURL=http://code.webplatform.org/gist/5622431
}}
}}
{{Notes_Section
|Usage=* Up to four different values can be specified, in the following order: top, right, bottom, left.
* If one value is specified, it is used for all four sides. If two values are specified, the first is used for the top and bottom slice-lines, and the second is used for left and right sides. If three values are specified, they are used for top, right/left, and bottom slice-lines, respectively. If left is missing, it is the same as right; if bottom is missing, it is the same as top; if right is missing, it is the same as top.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3
|URL=http://www.w3.org/TR/css3-background/#the-border-image-slice
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
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/border-image-slice
|MSDN_link=
|HTML5Rocks_link=
}}