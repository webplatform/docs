{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the style of an element's four borders. This property can have from one to four values. With only one value, the value will be applied to all four borders; otherwise, this works as a shorthand property for each of [[css/properties/border-top-style]], [[css/properties/border-right-style|border-right-style]], [[css/properties/border-bottom-style|border-bottom-style]], [[css/properties/border-left-style|border-left-style]], where each border style may be assigned a separate value. }}
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
|Description=Default. Border is not drawn, regardless of any [[css/properties/border-width|'''border-width''']].
}}{{CSS Property Value
|Data Type=hidden
|Description=Internet Explorer 8. Same as <code>none</code>, except in terms of conflict resolution of collapsed borders. Any element with a <code>hidden</code> border suppresses all shared borders at that location. Borders with a style of none have the lowest priority.
}}{{CSS Property Value
|Data Type=dotted
|Description=Border is a dotted line.
}}{{CSS Property Value
|Data Type=dashed
|Description=Border is a dashed line.
}}{{CSS Property Value
|Data Type=solid
|Description=Border is a solid line.
}}{{CSS Property Value
|Data Type=double
|Description=Border is a double line drawn on top of the background of the object. The sum of the two single lines and the space between equals the [[css/properties/border-width|'''border-width''']] value. The border width must be at least 3 pixels wide to draw a double border.
}}{{CSS Property Value
|Data Type=groove
|Description=3-D groove is drawn in colors based on the value.
}}{{CSS Property Value
|Data Type=ridge
|Description=3-D ridge is drawn in colors based on the value.
}}{{CSS Property Value
|Data Type=inset
|Description=3-D inset is drawn in colors based on the value.
}}{{CSS Property Value
|Data Type=outset
|Description=3-D outset is drawn in colors based on the value.
}}{{CSS Property Value
|Data Type=<border-style-top> <border-style-right> <border-style-bottom> <border-style-left>
|Description=Shorthand values syntax.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
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
|LiveURL=http://marcin-wosinek.github.com/border-style/
}}
}}
{{Notes_Section}}
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
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/border|border]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}