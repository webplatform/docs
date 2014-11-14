{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the style of an element's four borders. This property can have from one to four values. With only one value, the value will be applied to all four borders; otherwise, this works as a shorthand property for each of [[css/properties/border-top-style|border-top-style]], [[css/properties/border-right-style|border-right-style]], [[css/properties/border-bottom-style|border-bottom-style]], [[css/properties/border-left-style|border-left-style]], where each border style may be assigned a separate value.}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=borderStyle
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=Default. Border is not drawn, color and width are ignored. If the border is an image, the image layer counts but is not drawn. See [[css/properties/background-image|background-image]].
}}{{CSS Property Value
|Data Type=hidden
|Description=Same as <code>none</code>, except in terms of conflict resolution of collapsed borders. Any element with a <code>hidden</code> border suppresses all shared borders at that location. Borders with a style of none have the lowest priority.
}}{{CSS Property Value
|Data Type=dotted
|Description=A series of round dots.
}}{{CSS Property Value
|Data Type=dashed
|Description=A series of square-ended dashes.
}}{{CSS Property Value
|Data Type=solid
|Description=A single line segment.
}}{{CSS Property Value
|Data Type=double
|Description=Border is a double line drawn on top of the background of the object. The sum of the two single lines and the space between equals the [[css/properties/border-width|border-width]] value. The border width must be at least 3 pixels wide to draw a double border.
}}{{CSS Property Value
|Data Type=groove
|Description=Looks as if it were carved in the canvas. (This is typically achieved by creating a “shadow” from two colors that are slightly lighter and darker than the [[css/properties/border-color|border-color]].)
}}{{CSS Property Value
|Data Type=ridge
|Description=Looks as if it were coming out of the canvas.
}}{{CSS Property Value
|Data Type=inset
|Description=Looks as if the content on the inside of the border is sunken into the canvas.
}}{{CSS Property Value
|Data Type=outset
|Description=Looks as if the content on the inside of the border is coming out of the canvas.
}}{{CSS Property Value
|Data Type=<border-top-style> <border-right-style> <border-bottom-style> <border-left-style>
|Description=Shorthand values syntax.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Border styles in CSS.
|Code=.one {
  border-style: none;
}

.two {
  border-style: outset;
}

.three {
  border-style: hidden;
}

.four {
  border-style: dotted;
}

.five {
  border-style: dashed;
}

.six {
  border-style: solid;
}

.seven {
  border-style: double;
}

.eight {
  border-style: groove;
}

.nine {
  border-style: ridge;
}

.ten {
  border-style: inset;
}
|LiveURL=http://code.webplatform.org/gist/5544029
}}
}}
{{Notes_Section
|Usage=* Up to four different styles can be specified, in the following order: top, right, bottom, left. 
* If one style is specified, it is used for all four sides. If two styles are specified, the first is used for the top and bottom borders, and the second is used for left and right borders. If three styles are specified, they are used for top, right/left, and bottom borders, respectively. If left is missing, it is the same as right; if bottom is missing, it is the same as top; if right is missing, it is the same as top.
|Notes=* Borders are drawn in front of the element's background, but behind the element's content (in case it overlaps).
* There is no control over the spacing of the dots and dashes, nor over the length of the dashes.
* How borders of different styles are joined in the corner may vary.
* Rounded corners may cause the corners and the contents to overlap, if the padding is less than the radius of the corner.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Level 3 - Backgrounds and Borders Module
|URL=http://www.w3.org/TR/css3-background/#border-style
|Status=Candidate Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=Related CSS properties:
* [[css/properties/border-top-style|border-top-style]]
* [[css/properties/border-right-style|border-right-style]]
* [[css/properties/border-bottom-style|border-bottom-style]]
* [[css/properties/border-left-style|border-left-style]]

Related tutorials:
* [[tutorials/css_border_image|Decorating fancy borders with CSS border-image]]
|External_links=* [https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=4&cad=rja&ved=0CE4QFjAD&url=https%3A%2F%2Fdeveloper.mozilla.org%2Fen-US%2Fdocs%2FWeb%2FCSS%2Fborder-style&ei=um2mUb2QC6mliQKE-IHwDg&usg=AFQjCNHuEil-o7WWpH1wxOt_DzFDy_lm-A&sig2=Ifwz1_Fq4GzjkJct0EfFxw&bvm=bv.47244034,d.cGE CSS border-style property on MDN]
* [https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=8&cad=rja&ved=0CHIQFjAH&url=http%3A%2F%2Freference.sitepoint.com%2Fcss%2Fborder-style&ei=um2mUb2QC6mliQKE-IHwDg&usg=AFQjCNGjOxzgETcUxPFZD3txXZ3rgghK8Q&sig2=H8jwjVBXF55U1h_a6E3HsA&bvm=bv.47244034,d.cGE CSS border-style property on SitePoint]
|Manual_sections=
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}