{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The CSS border-color property sets the color of an element's four borders. This property can have from one to four values, made up of the elementary properties: 

* [[css/properties/border-top-color|border-top-color]]
* [[css/properties/border-right-color|border-right-color]]
* [[css/properties/border-bottom-color|border-bottom-color]]
* [[css/properties/border-left-color|border-left-color]]

The default color is the currentColor of each of these values.

If you provide one value, it sets the color for the element. Two values set the horizontal and vertical values, respectively. Providing three values sets the top, vertical, and bottom values, in that order. Four values set all for sides: top, right, bottom, and left, in that order.
}}
{{CSS Property
|Initial value=color: The value of the 'color' property for each of the border sides border-top-color, border-right-color, border-bottom-color, and border-left-color.
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=See individual properties
|Animatable=Yes
|CSS object model property=borderColor
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<color>
|Description=Specify the color to use on all borders. This can be anywhere from one to four values representing the top, right, bottom, and left border respectively.
}}{{CSS Property Value
|Data Type=inherit
|Description=Is a keyword indicating that all four values are inherited from their parent's element calculated value.
}}{{CSS Property Value
|Data Type=transparent
|Description=This will apply a border that is not visible but it can have a width applied.
}}{{CSS Property Value
|Data Type=currentColor
|Description=The same as ‘color: inherit’, the color value inherited from parent object.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=A simple example showing how to use the border-color property on HTML div elements.
|Code=.one {
		  color: #6CC644;
		  border: medium solid;
		}

		/* You can use other color on each side */
		.two {
		  border: 10px solid;
		  border-color: #6CC644 #FFC621 #DE6525 #256A84;
		}

		/* You can use other color for other styles */
		.three {
		  border-width: 5px;
		  border-style: ridge dashed solid;
		  border-color: #6CC644 #DE6525;
		}
		
		/* You can set horizontal and vertical using just two color values (horizontal is first then vertical) */
		.four {
			border-width: 3px;
			border-style: solid;
			border-color: #ccc #666;
		}
|LiveURL=http://code.webplatform.org/gist/5546053
}}
}}
{{Notes_Section
|Usage=The color value can be a property keyword, an extended keyword, or a numerical value. The two property keywords are currentColor and transparent. currentColor is the ‘color’ property value from the parent object. transparent is shorthand for transparent black, rgba(0,0,0,0).

The color value can also be a numerical value, such as one of the following:

* a basic color keyword, such as "red"
* a hex value, such as #ff0000
* an red-green-blue (RGB) value, such as rgb(255,0,0)
* an RGB-alpha (RGBA) that includes color opacity, such as rgba(255,0,0,1) or rgba(100%,0%,0%,1)
* a hue-saturation-lightness (HSL), such as hsl(0, 100%, 50%)
* HSLa, such as hsl(0, 100%, 50%, 1)

The color value can also be an extended keyword, such as aliceblue or lavenderblush. For a full list of extended keywords, see the [http://www.w3.org/TR/css3-color/#svg-color CSS Color Module Level 3 spec], which is the consolidation of various specifications.
}}
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
|Manual_sections====Related pages===
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
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/border-color
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}