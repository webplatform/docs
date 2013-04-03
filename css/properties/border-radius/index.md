{{Page_Title}}
{{Flags
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
|CSS object model property=element.style.borderRadius
|CSS percentages=Refer to the corresponding dimension (width or height) of the border box.
|Values={{CSS Property Value
|Data Type=length
|Description=Denotes the size of the circle radius or the horizontal and vertical radii, for elliptical curves. It can be expressed in any unit allowed in [[css/data_types/length|CSS <length> data types]]. em units are useful for controls that scale proportionally with the font-size. Viewport-relative units (vw, vh, vmin, vmax) can be useful for controls that scale with the viewport size. Negative values are invalid.
}}{{CSS Property Value
|Data Type=percentage
|Description=Denotes the size of the corner radius, in percentages of the box’s dimensions. Specifically, percentages for the horizontal axis refer to the width of the box, percentages for the vertical axis refer to the height of the box. Negative values are invalid.
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
}}{{Single Example
|Language=CSS
|Description=Multi value example
|Code=border-radius: 20px 1em 1vw / 0.5em 3em;

/*is equivalent to:*/

border-top-left-radius: 20px 0.5em;
border-top-right-radius: 1em 3em;
border-bottom-right-radius: 1vw 0.5em;
border-bottom-left-radius: 1em 3em;
}}{{Single Example
|Language=CSS
|Description=Create an ellipse, regardless of the element’s dimensions
|Code=border-radius: 50%;

/* Will be a circle if the element’s width is equal to its height */
}}{{Single Example
|Language=CSS
|Description=Shrinking curves to avoid overlapping
|Code=border-radius: 100% 150%;

/* equivalent to: */

border-radius: 40% 60%;

/* The values shrink proportionally, all multiplied by the same factor, until there is no overlap */
}}
}}
{{Notes_Section
|Usage=As with any shorthand property, individual inherited values are not possible, that is <code>border-radius:0 0 inherit inherit</code>, which would override existing definitions partially. In that case, the individual longhand properties have to be used.

===Syntax===

The syntax of the first radius allows one to four values, to specify different radius per corner:<br/>
<code class="language-css block">border-radius: [radius for all corners];<br/>           
border-radius: [radius for top left & bottom right corners] [radius for top right & bottom left corners];<br/>
border-radius: [top left radius] [top right & bottom left radius] [bottom right radius];<br/>
border-radius: [top left radius] [top right radius] [bottom right radius] [bottom left radius];</code>

The syntax of the vertical radius also allows one to four values<br/>
<code class="language-css block">border-radius: (horizontal radius values) / [radius for all corners];<br/>   
border-radius: (horizontal radius values) / [top left & bottom radius] [top right & bottom left radius];<br/>
border-radius: (horizontal radius values) / [top left radius] [top right & bottom left radius] [bottom right radius];<br/>
border-radius: (horizontal radius values) / [top left] [top right] [bottom right] [bottom left];</code>
|Notes====Remarks===

* The '''border-radius''' property is a composite property that specifies up to four '''border-*-radius''' properties. If values are given before and after the slash, the values before the slash set the horizontal radius and the values after the slash set the vertical radius. If there is no slash, the values set both radii equally. The four values for each radii are given in clockwise order, starting from the top left corner. If less than four values are provided, they are repeated until we get four values, similarly to other CSS properties, such as border-width.
* It’s possible to end up with elliptical corners, even by specifying one radius. This occurs when you are using percentages, since they resolve to a different number for each axis (horizontally they are percentages of the border box width, vertically of the height). For a demonstration, refer to the ellipse example above (example #3)
* Since border-radius rounds the border box of the element, the inner (padding box) corners will have smaller radii (specifically border-radius - border-width), or even no rounding, if the border is thicker than the border-radius value. Another consequence of this is that when there are different border widths on adjacent sides, the curves of the padding box will be elliptical.
* Note that although in the border-radius shorthand, there is a slash (/) to separate horizontal from vertical radii, they are space separated in the longhands.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3: Rounded Corners:
|URL=http://www.w3.org/TR/css3-background/#the-border-radius
|Status=Candidate Recommendation
}}{{Related Specification
|Name=CSS Backgrounds and Borders Module Level 4: Rounded Corners:
|URL=http://dev.w3.org/csswg/css4-background/#corners
|Status=Editor’s Draft
|Relevant_changes=Added border-corner-shape to let border-radius specify the size of a number of different corner shapes besides rounded corners.
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=4.0
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=0.2
|Firefox_supported=Yes
|Firefox_version=4.0 (2.0)
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=1.0 (1.7 or earlier)
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.0
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=3.0
}}{{Compatibility Table Desktop Row
|Feature=Percentages
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=Elliptical borders
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.5 (1.9.1)
|Firefox_prefixed_supported=Yes
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=4 values for 4 corners
|Chrome_supported=Yes
|Chrome_version=4.0
|Chrome_prefixed_supported=Yes
|Firefox_supported=Yes
|Firefox_prefixed_supported=Yes
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.2
|Android_prefixed_supported=Yes
|Android_prefixed_version=2.1
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=11.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=4.0
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=3.2
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Firefox
|Version=< 3.6
|Note=Used to treat percentage values as percentages of the width, for both axes
}}{{Compatibility Notes Row
|Browser=Firefox
|Version=< 3.6
|Note=Non-standard longhand names (-moz-border-radius-topleft etc)
}}{{Compatibility Notes Row
|Browser=WebKit
|Version=< 532.5
|Note=Supports only one value in border-radius. For different radii, the longhands need to be used. don't support the slash / notation. If two values are specified, they are interpreted as horizontal and vertical radii for all four corners.
}}{{Compatibility Notes Row
|Browser=WebKit
|Version=< 532.5
|Note=When the sum of two adjacent radii exceeds the length of the side they’re on, they are reduced to 0 instead of shrinking proportionally.
}}{{Compatibility Notes Row
|Browser=Opera
|Version=< 11.6
|Note=border-radius has no effect in replaced elements (like images)
}}{{Compatibility Notes Row
|Browser=Opera
|Version=< 11.6
|Note=Percentages are accepted in border-radius, but are treated incorrectly.
}}
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
<compatability topic="css" type="property" feature="border-radius" format="list"></compatability>






==Can I Use==
<compatability topic="css" type="property" feature="border-radius"></compatability>