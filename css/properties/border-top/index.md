{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets all the top border properties in one declaration.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=See individual properties
|Animatable=No
|CSS object model property=borderTop
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<border-width> <border-style> <color>
|Description=Any of the range of width values available to the [[css/properties/border-top-width|'''border-top-width''']] property.
The <tt>border-top</tt> property is a shorthand property for setting the same width, color, and style for top border of a box.
* Width - Any of the range of width values available to the [[css/properties/border-width|'''border-width''']] property. Default value is <tt>medium</tt>.
* Style - Any of the range of style values available to the [[css/properties/border-style|'''border-style''']] property. Default value is <tt>none</tt>.
* Color - Any of the range of color values available to the [[css/properties/border-color|'''border-color''']] property. Default value is the value of the element's [[css/properties/color|'''color''']] property - i.e. text color.
}}{{CSS Property Value
|Data Type=inherit
|Description=When we set the value to <tt>inherit</tt>, the element will use border values set on its parent
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* When we don't set border-top-color, color of a text is used as a default */
.one {
  color: #6CC644;
  border-top: medium solid;
}

/* When we don't set border-top-style, default style <none> will be used - therefor no border-top will be rendered */
.two {
  border-top: 1px red;
}

/* Other border-top style example */
.three {
  border-top: dotted 2px red;
}
|LiveURL=http://marcin-wosinek.github.com/border-top
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''border-top''' property is a composite property that sets the '''width''', '''style''', and '''color''' values for the top border of an object.
All individual border properties not set by the composite '''border-top''' property are set to their default values. 

The default value for the [[css/properties/border-color|'''border-color''']] is the same as the text color, for [[css/properties/border-width|'''border-width''']] is <tt>medium</tt> and for [[css/properties/border-style|'''border-style''']] is <tt>none</tt>. Therefor you must specify a style when specifying a width or color; otherwise, the border will be invisible.
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms530739(v=vs.85).aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}