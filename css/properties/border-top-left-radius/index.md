{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Defines the shape of the border of the top-left corner.}}
{{CSS Property
|Initial value=0
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=two absolute <length> or percentages
|Animatable=Yes
|CSS object model property=object.style.borderTopLeftRadius
|Values={{CSS Property Value
|Data Type=length
|Description=Denotes the size of the circle radius or the semi-major and semi-minor axes of the ellipsis. It can be expressed in any unit allowed by the [[css/data_types/length|CSS <length> data types]]. Negative values are invalid.
}}{{CSS Property Value
|Data Type=percentage
|Description=Denotes the size of the circle radius, or the semi-major and semi-minor axes of the ellipsis, using percentage values. Percentages for the horizontal axis refer to the width of the box, percentages for the vertical axis refer to the height of the box. Negative values are invalid.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=One value example to use an arc of circle as the border on the top left corner.
|Code=border-top-left-radius: 10px;

/* is equivalent to: */
border-top-left-radius: 10px 10px;
}}{{Single Example
|Language=CSS
|Description=Two value example to use an arc of ellipse as the border on the top left corner.
|Code=border-top-left-radius: 10px 5px;
}}{{Single Example
|Language=CSS
|Description=One value percentage example on the top left corner. If the box is a square an arc of circle is used as the border, if the box is not a square an arc of ellipse is used as the border.
|Code=border-top-left-radius: 30%;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''border-top-left-radius''' property specifies the horizontal and vertical radii of the ellipse that defines the rounded upper-left corner for a border box. If there is only one value given, that value specifies both horizontal and vertical radii of the ellipse. If there are two values given, the first value sets the horizontal radius and the second value sets the vertical radius.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3: Rounded Corners:
|URL=http://www.w3.org/TR/css3-background/#border-top-left-radius
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
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>Reference</code>
*<code>[[css/properties/border-radius|border-radius]]</code>
*<code>[[css/properties/border-top-right-radius|border-top-right-radius]]</code>
*<code>[[css/properties/border-bottom-right-radius|border-bottom-right-radius]]</code>
*<code>[[css/properties/border-bottom-left-radius|border-bottom-left-radius]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/es/docs/CSS/border-top-left-radius Border-top-left-radius]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}