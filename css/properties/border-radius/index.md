{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The border-radius CSS property allows authors to round the corners of an element. The rounding can be different per-corner, and it could have different horizontal and vertical radii, to produce elliptical curves.}}
{{CSS Property
|Initial value=0
|Applies to=All elements, except the table element when border-collapse is collapse
|Inherited=No
|Media=visual
|Computed value=As specified by individual properties
|Animatable=Yes
|CSS object model property=borderRadius
|CSS percentages=Refer to the corresponding dimension (width or height) of the border box.
|Values={{CSS Property Value
|Data Type=length
|Description=Denotes the size of the circle radius or the horizontal and vertical radii, for elliptical curves. It can be expressed in any unit allowed in [[css/data_types/length|CSS <length> data types]]. em units are useful for controls that scale proportionally with the font-size. Viewport-relative units (vw, vh, vmin, vmax) can be useful for controls that scale with the viewport size. Negative values are invalid. You can specify a single length for all four corners, or two, three or four lengths to specify different lengths for different corners: see the syntax section for more details.
}}{{CSS Property Value
|Data Type=percentage
|Description=Denotes the size of the corner radius, in percentages of the box’s border-box dimensions. Specifically, percentages for the horizontal axis refer to the width of the border-box, percentages for the vertical axis refer to the height of the border-box. Negative values are invalid. You can specify a single percentage for all four corners, or two, three or four percentages to specify different percentages for different corners: see the syntax section for more details.
}}{{CSS Property Value
|Data Type=length / length
|Description=Specifying two sets of length values separated by a forward slash equates to specifying separate lengths for the X and Y radii of the corners, resulting in elliptical corners if the X and Y radii have different lengths. Each set can consist of one, two, three or four values.
}}{{CSS Property Value
|Data Type=percentage / percentage
|Description=Specifying two sets of percentage values separated by a forward slash equates to specifying separate percentages for the X and Y radii of the corners, resulting in elliptical corners if the X and Y radii have percentages resulting in different computed values (depending on the width and height of the element, different percentages might result in the same computed values; see the remarks section for more). Each set can consist of one, two, three or four values.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=One value example
|Code=border-radius: 1em;

/* is equivalent to: */

border-top-left-radius: 1em;
border-top-right-radius: 1em;
border-bottom-right-radius: 1em;
border-bottom-left-radius: 1em;
|LiveURL=http://code.webplatform.org/gist/5495188
}}{{Single Example
|Language=CSS
|Description=Multi value example
|Code=border-radius: 20px 1em 1vw / 0.5em 3em;

/* is equivalent to: */

border-top-left-radius: 20px 0.5em;
border-top-right-radius: 1em 3em;
border-bottom-right-radius: 1vw 0.5em;
border-bottom-left-radius: 1em 3em;
|LiveURL=http://code.webplatform.org/gist/5495188
}}{{Single Example
|Language=CSS
|Description=Create an ellipse, unless the
|Code=border-radius: 50%;

/* Will be a circle if the element’s width is equal to its height */
|LiveURL=http://code.webplatform.org/gist/5495188
}}{{Single Example
|Language=CSS
|Description=Shrinking curves to avoid overlapping
|Code=border-radius: 100% 150%;

/* is equivalent to: */

border-radius: 40% 60%;

/* The values shrink proportionally, all multiplied by the same factor, until there is no overlap */
|LiveURL=http://code.webplatform.org/gist/5495188
}}
}}
{{Notes_Section
|Usage=As with any shorthand property, individual inherited values are not possible, that is <code>border-radius:0 0 inherit inherit</code>, which would override existing definitions partially. In that case, the individual longhand properties have to be used.

===Syntax===

<code>border-radius</code> can take between one and four values:

* one value will be applied to all four corners
* two values will be applied to top-left + bottom-right, and top-right + bottom-left, respectively
* three values will be applied to top-left, top-right + bottom-left, and bottom-right, respectively 
* four values will be applied to the four corners separately, in the order of top-left, top-right, bottom-right, bottom-left
|Notes====Remarks===

* The '''border-radius''' property is a composite property that specifies up to four '''border-*-radius''' properties. If values are given before and after the slash, the values before the slash set the horizontal radius and the values after the slash set the vertical radius. If there is no slash ("/"), the values set both radii equally. The four values for each radii are given in clockwise order, starting from the top left corner. If less than four values are provided, they are repeated until we get four values, similarly to other CSS properties, such as border-width.
* It’s possible to end up with elliptical corners, even by specifying one radius. This occurs when you are using percentages, since they resolve to a different number for each axis (horizontally they are percentages of the border box width, vertically of the height). For a demonstration, refer to the ellipse example above (example #3)
* Since border-radius rounds the border box of the element, the inner (padding box) corners will have smaller radii (specifically border-radius - border-width), or even no rounding, if the border is thicker than the border-radius value. Another consequence of this is that when there are different border widths on adjacent sides, the curves of the padding box will be elliptical.
* Note that although in the border-radius shorthand, there is a slash (/) to separate horizontal from vertical radii, they are space separated in the longhands.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3: Rounded Corners:
|URL=http://www.w3.org/TR/css3-background/#the-border-radius
|Status=Candidate Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=CSS Backgrounds and Borders Module Level 4: Rounded Corners:
|URL=http://dev.w3.org/csswg/css4-background/#corners
|Status=Editor’s Draft
|Relevant_changes=Added border-corner-shape to let border-radius specify the size of a number of different corner shapes besides rounded corners.
}}
}}
{{See_Also_Section
|Topic_clusters=Border
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>Reference</code>
*<code>[[css/properties/border-top-left-radius|border-top-left-radius]]</code>
*<code>[[css/properties/border-top-right-radius|border-top-right-radius]]</code>
*<code>[[css/properties/border-bottom-right-radius|border-bottom-right-radius]]</code>
*<code>[[css/properties/border-bottom-left-radius|border-bottom-left-radius]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/CSS/border-radius Border-radius]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}