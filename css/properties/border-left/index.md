{{Page_Title|border-left}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Shorthand property that defines the [[css/properties/border-width|'''border-width''']], [[css/properties/border-style|'''border-style''']] and [[css/properties/border-color|'''border-color''']] of an element's left border in a single declaration. Note that you can use the corresponding longhand properties to set specific individual properties of the left border — [[css/properties/border-left-width|'''border-left-width''']], [[css/properties/border-left-style|'''border-left-style''']] and [[css/properties/border-left-color|'''border-left-color''']].}}
{{CSS Property
|Initial value=For style values, the initial value is none. For color values, the initial value is currentColor.  For width values, the initial value is medium, which is computed as about 3px in most browsers.
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=For <code>style</code> values, the computed value is as specified. For <code>width</code> values, the computed value is the absolute pixel value, or <code>0</code> if the value is set to <code>none</code> or <code>hidden</code>. For <code>color</code> values, the computed value is the equivalent RGB value, or the equivalent RGBA value for translucent colors.
|Animatable=Yes
|CSS object model property=borderLeft
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=border-width border-style color
|Description=The <code>border-left</code> property can contain up to three components:
* <code>border-width</code>: This takes a numeric value with any of the standard length units.
* <code>border-style</code>: This takes any of the range of style values available to the [[css/properties/border-style|'''border-style''']] property, which includes <code>none</code>, <code>hidden</code>, <code>dotted</code>, <code>dashed</code>, <code>solid</code>, <code>double</code>, <code>groove</code>, <code>ridge</code>, <code>inset</code>, <code>outset</code>. For more details about each, see the [[css/properties/border-style|'''border-style''']] page.
* <code>color</code>: This can take any valid CSS color as its value.
}}{{CSS Property Value
|Data Type=inherit
|Description=When we set the value to <code>inherit</code>, the element will inherit the border values set on its parent.
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
|Usage=* It is usual to use the <code>border-left</code> property to set the default state of a box's left border, and then override individual values using more specific properties, such as <code>border-left-width</code> or <code>border-left-color</code>.
* <code>border-left</code> can be used as a divider between horizontally laid out items, such as horizontal navigation menu items, or table cells.

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
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}