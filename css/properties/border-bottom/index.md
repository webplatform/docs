{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Shorthand property that sets the properties of an element's bottom border.It can be used to set one or more values (of those: [[css/properties/border-bottom-width|'''border-bottom-width''']], [[css/properties/border-bottom-style|'''border-bottom-style''']], [[css/properties/border-bottom-color|'''border-bottom-color''']]).}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=See individual properties
|Animatable=No
|CSS object model property=borderBottom
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<border-width> <border-style> <color>
|Description=The <tt>border-bottom</tt> property is a shorthand property for setting the same width, color, and style for only one border of a box: bottom.
* '''Width''' - Any of the range of width values available to the [[css/properties/border-bottom-width|'''border-bottom-width''']] property. It's optional. Default value is <tt>medium</tt>.
* '''Style''' - Any of the range of style values available to the [[css/properties/border-bottom-style|'''border-bottom-style''']] property. Default value is <tt>none</tt>.
* '''Color''' - Any of the range of color values available to the [[css/properties/border-bottom-color|'''border-bottom-color''']] property. Default value is the value of the element's [[css/properties/color|'''color''']] property - i.e. text color.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* When we don't set border-bottom-color, color of a text is used as a default */
.one {
  color: #6CC644;
  border-bottom: medium solid;
}

/* When we don't set border-bottom-style, default style <none> will be used - therefore no border will be rendered */
.two {
  border-bottom: 1px red;
}

/* Other border-bottom style example */
.three {
  border-bottom: dotted 2px red;
}

|LiveURL=http://kamila-wosinek.github.com/border-bottom/
}}{{Single Example
|Description=This example uses inline scripting to change the bottom border.
|Code=&lt;TD onmouseover{{=}}"this.style.borderBottom{{=}}'0.3cm groove yellow'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/borderBottom.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''border-bottom''' property is a composite property that sets the '''width''', '''style''', and '''color''' values for the bottom border of an object.
All individual border properties not set by the composite '''border-bottom''' property are set to their default values. 

The default value for the [[css/properties/border-color|'''border-color''']] is the same as the text color, for [[css/properties/border-width|'''border-width''']] is <tt>medium</tt> and for [[css/properties/border-style|'''border-style''']] is <tt>none</tt>. Therefor you must specify a style when specifying a width or color; otherwise, the border will be invisible.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.20
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0 ( 1.7 or earlier )
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0 (1.0)
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms530724(v=vs.85).aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}