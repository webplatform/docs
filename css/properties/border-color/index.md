{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The CSS border-color property sets the color of an element's four borders. This property can have from one to four values.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=See individual properties
|Animatable=No
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
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
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
}}
}}
{{Notes_Section
|Usage=Always declare the border-style property before the border-color property. An element must have borders before you can change the color.
|Notes====Remarks===
Up to four different colors can be specified in the following order: top, right, bottom, left. If one color is supplied, it is used for all four sides. If two colors are supplied, the first is used for the top and bottom, and the second is used for left and right. If three colors are supplied, they are used for top, right and left, and bottom, respectively.

The '''border-color''' property does not render if the [[css/properties/border-style|'''border-style''']] property is set to '''none'''.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.16
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
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/border-color
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}