{{Page_Title|box-decoration-break}}
{{Flags
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Breaks a box into fragments creating new borders, padding and repeating backgrounds or lets it stay as a continuous box on a page break, column break, or, for inline elements, at a line break.}}
{{CSS Property
|Initial value=slice
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=clone
|Description=Each box fragment is independently wrapped with the border and padding. The <code>border-radius</code> and <code>border-image</code> and <code>box-shadow</code>, if any, are applied to each fragment independently. The background is drawn independently in each fragment of the element. A no-repeat background image will thus be rendered once in each fragment of the element.
}}{{CSS Property Value
|Data Type=slice
|Description=
No border and no padding are inserted at a break. No box-shadow is drawn at a broken edge; <code>border-radius</code> does not apply to its corners; and the <code>border-image</code> is rendered for the whole box as if it were unbroken. The effect is as though the element were rendered with no breaks present, and then sliced by the breaks afterward.

Backgrounds are drawn as if, after the element has been laid out (including any justification, reordering, page breaks, etc.), all the element's box fragments were taken and put one after the other in visual order. The background is applied to the bounding box of this composite box and then the fragments are put back, with each with its share of the background.

}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=This is an example of CSS how you can use box-decoration-break for a given element <code>.clone</code> which is part of the element element with column breaks.
|Code=/**
 * box-decoration-break
 *
 * Please be aware that this demo uses prefix-free.js to
 * remove the hassle of adding vendor prefixes.
 * This is currently not working in any browser.
 */
.clone {
	/* Set some values to be cloned */
	background: #eee;
	border: 1px solid #aaa;
	padding: 5px;

	/* Clone the box */
	box-decoration-break: clone;
}

/* Creating a bunch of columns */
.box {
	column-count: 4;
	column-gap: 1em;
}
|LiveURL=http://code.webplatform.org/gist/6363867
}}
}}
{{Notes_Section
|Usage=This property comes in handy if you want to indicate how a box splits when, for example a user prints a page.
When using CSS columns, grids or regions it is useful to decide how a box looks when it breaks.
|Notes=In Firefox there is <code>-moz-background-inline-policy</code> which enables you to treat background images how you want to. This is only a partial implementation of <code>box-decoration-break</code>.

}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3
|URL=http://www.w3.org/TR/css3-background/#box-decoration-break
|Status=Candidate Recommendation
}}{{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3
|URL=http://dev.w3.org/csswg/css-backgrounds/#box-decoration-break
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
|Topic_clusters=CSS Layout
|External_links=[[https://developer.mozilla.org/en-US/docs/Web/CSS/-moz-background-inline-policy|Documentation on -moz-background-inline-policy]]
[[http://bricss.net/post/24672339016/box-decoration-break-finally-coming-to-more-browsers|The state of box-decoration-break by Lennart Schoors]]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}