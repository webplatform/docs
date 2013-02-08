{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The border-radius CSS property allows Web authors to define how rounded border corners are. The curve of each corner is defined using one or two radii, defining its shape: circle or ellipse.}}
{{CSS Property
|Initial value=0
|Applies to=all elements, except the table element when border-collapse is collapse
|Inherited=No
|Media=visual
|Computed value=as specified by individual properties
|Animatable=Yes
|CSS object model property=object.style.borderRadius
|CSS percentages=Refer to corresponding dimension of the border box.
|Values={{CSS Property Value
|Data Type=length
|Description=Denotes the size of the circle radius or the semi-major and semi-minor axes of the ellipsis. It can be expressed in any unit allowed by the CSS <length> data types. Negative values are invalid.
}}{{CSS Property Value
|Data Type=percentage
|Description=Denotes the size of the circle radius, or the semi-major and semi-minor axes of the ellipsis, using percentage values. Percentages for the horizontal axis refer to the width of the box, percentages for the vertical axis refer to the height of the box. Negative values are invalid.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=One value example
|Code=border-radius:2em;

/*is equivalent to:*/

border-top-left-radius:2em;
border-top-right-radius:2em;
border-bottom-right-radius:2em;
border-bottom-left-radius:2em;
}}{{Single Example
|Language=CSS
|Description=Multi value example
|Code=border-radius: 2em 1em 4em / 0.5em 3em;

/*is equivalent to:*/

border-top-left-radius: 2em 0.5em;
border-top-right-radius: 1em 3em;
border-bottom-right-radius: 4em 0.5em;
border-bottom-left-radius: 1em 3em;
}}{{Single Example
|Language=CSS
|Description=Valid max percentage value example
|Code=border-radius:50%;
/*0% - 50%*/
}}{{Single Example
|Language=CSS
|Description=Wrong max percentage value example
|Code=border-radius:100%;
/*larger then allowed*/
}}
}}
{{Notes_Section
|Usage=As with any shorthand property, individual inherited values are not possible, that is <code>border-radius:0 0 inherit inherit</code>, which would override existing definitions partially. In that case, the individual longhand properties have to be used.

===Syntax===
The syntax of the first radius allows one to four values:<br/>
<code>
border-radius: radius <br/>           
border-radius: top-left-and-bottom-right top-right-and-bottom-left <br/>
border-radius: top-left top-right-and-bottom-left bottom-right <br/>
border-radius: top-left top-right bottom-right bottom-left </code><br/>
<br/>
The syntax of the second radius also allows one to four values<br/>
<code>
border-radius: (first radius values) / radius <br/>   
border-radius: (first radius values) / top-left-and-bottom-right top-right-and-bottom-left <br/>
border-radius: (first radius values) / top-left top-right-and-bottom-left bottom-right <br/>
border-radius: (first radius values) / top-left top-right bottom-right bottom-left </code><br/>
|Notes====Remarks===
The '''border-radius''' property is a composite property that specifies up to four '''border-*-radius''' properties. If values are given before and after the slash, the values before the slash set the horizontal radius and the values after the slash set the vertical radius. If there is no slash, the values set both radii equally. The four values for each radii are given in the following order: top-left, top-right, bottom-right, bottom-left. If the bottom-left value is omitted, the value is the same as the top-right value. If the bottom-right value is omitted, the value is the same as the top-left value. If the top-right value is omitted, the value is the same as the top-left value.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3: Rounded Corners:
|URL=http://www.w3.org/TR/css3-background/#the-border-radius
|Status=Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=5.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
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
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.2
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Yes
|Blackberry_prefixed_version=7.0
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=9.0
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
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=9.0
|Note=The border-radius property can't be animated/transitioned in IE. See this demo for a keyframe animation and a transition: http://jsfiddle.net/FPnV6/1/
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
*<code>[[css/properties/border-top-right-radius|border-top-right-radius]]</code>
*<code>[[css/properties/border-bottom-left-radius|border-bottom-left-radius]]</code>
*<code>[[css/properties/border-bottom-right-radius|border-bottom-right-radius]]</code>
*<code>[[css/properties/border-top-left-radius|border-top-left-radius]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/CSS/border-radius Border-radius]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}