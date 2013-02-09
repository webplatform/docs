{{Page_Title}}
{{Flags}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Shorthand property that sets the properties of an element's left border.It can be used to set one or more values (of those: [[css/properties/border-left-width|'''border-left-width''']], [[css/properties/border-left-style|'''border-left-style''']], [[css/properties/border-left-color|'''border-left-color''']]).}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=See individual properties
|Animatable=No
|CSS object model property=borderLeft
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<border-width> <border-style> <color>
|Description=The <tt>border-left</tt> property is a shorthand property for setting the same width, color, and style for only one border of a box: left.
* '''Width''' - Any of the range of width values available to the [[css/properties/border-left-width|'''border-left-width''']] property. It's optional. Default value is <tt>medium</tt>.
* '''Style''' - Any of the range of style values available to the [[css/properties/border-left-style|'''border-left-style''']] property. Default value is <tt>none</tt>.
* '''Color''' - Any of the range of color values available to the [[css/properties/border-left-color|'''border-left-color''']] property. Default value is the value of the element's [[css/properties/color|'''color''']] property - i.e. text color.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* When we don't set border-left-color, color of a text is used as a default */
.one {
  color: #6CC644;
  border-left: medium solid;
}

/* When we don't set border-left-style, default style <none> will be used - therefore 
no border will be rendered */
.two {
  border-left: 1px red;
}

/* Other border-left style example */
.three {
  border-left: dotted 2px red;
}
|LiveURL=http://kamila-wosinek.github.com/border-left/
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''border-left''' property is a composite property that sets the '''width''', '''style''', and '''color''' values for the left border of an object.
All individual border properties not set by the composite '''border-left''' property are set to their default values. 

The default value for the [[css/properties/border-color|'''border-color''']] is the same as the text color, for [[css/properties/border-width|'''border-width''']] is <tt>medium</tt> and for [[css/properties/border-style|'''border-style''']] is <tt>none</tt>. Therefor you must specify a style when specifying a width or color; otherwise, the border will be invisible.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.21
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
*<code>Reference</code>
*<code>[[css/properties/border|border]]</code>
*<code>Other Resources</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/border-left
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}