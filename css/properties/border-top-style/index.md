{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the style of an element's top border. To set all four borders, use the shorthand property,  [[css/properties/border-style|border-style]]. Otherwise, you can set the borders individually with [[css/properties/border-top-style|border-top-style]], [[css/properties/border-right-style|border-right-style]], [[css/properties/border-bottom-style|border-bottom-style]], [[css/properties/border-left-style|border-left-style]].}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=borderStyleTop
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=Default. Border is not drawn, color and width are ignored. If the border is an image, the image layer counts but is not drawn. See [[css/properties/background-image|background-image]].
}}{{CSS Property Value
|Data Type=hidden
|Description=Same as <code>none</code>, except in terms of conflict resolution of collapsed borders. Any element with a <code>hidden</code> border suppresses all shared borders at that location. Borders with a style of none have the lowest priority.
}}{{CSS Property Value
|Data Type=dotted
|Description=A series of round or square dots.
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
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Border styles in CSS.
|Code=.one {
  border-top-style: none;
}

.two {
  border-top-style: outset;
}

.three {
  border-top-style: hidden;
}

.four {
  border-top-style: dotted;
}

.five {
  border-top-style: dashed;
}

.six {
  border-top-style: solid;
}

.seven {
  border-top-style: double;
}

.eight {
  border-top-style: groove;
}

.nine {
  border-top-style: ridge;
}

.ten {
  border-top-style: inset;
}
|LiveURL=http://code.webplatform.org/gist/5544029
}}
}}
{{Notes_Section
|Notes=* Borders are drawn in front of the element's background, but behind the element's content (in case it overlaps).
* There is no control over the spacing of the dots and dashes, nor over the length of the dashes.
* How borders of different styles are joined in the corner may vary.
* Rounded corners may cause the corners and the contents to overlap, if the padding is less than the radius of the corner.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3
|URL=http://www.w3.org/TR/css3-background/#border-style
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
{{See_Also_Section
|Topic_clusters=Border
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}