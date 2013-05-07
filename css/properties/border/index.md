{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Shorthand property that defines the different properties of all four sides of an element's border in a single declaration. It can be used to set [[css/properties/border-width|'''border-width''']], [[css/properties/border-style|'''border-style''']] and [[css/properties/border-color|'''border-color''']], or a subset of these. Note that as well as defining properties for all four sides of an element's border at once, you can also target borders on specific sides individually — for example [[css/properties/border-top|'''border-top''']] and [[css/properties/border-right|'''border-right''']] — or even specific properties of individual borders — for example [[css/properties/border-top-color|'''border-top-color''']] and [[css/properties/border-right-color|'''border-right-color''']].}}
{{CSS Property
|Initial value=For style values, the initial value is none. For color values, the initial value is currentColor.  For width values, the initial value is 0.
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=For <code>style</code> values, the computed value is as specified. For <code>width</code> values, the computed value is the absolute pixel value, or <code>0</code> if the value is set to <code>none</code> or <code>hidden</code>. For <code>color</code> values, the computed value is the equivalent RGB value, or the equivalent RGBA value for translucent colors.
|Animatable=No
|CSS object model property=border
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=border-width border-style color
|Description=The <code>border</code> property can contain up to three components:
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
|Code=/* When we don't set border-color, color of a text is used as a default */
.one {
  color: blue;
  border: medium solid;
}

/* When we don't set border-style, default style <none> will be used - therefor no border will be rendered */
.two {
  border: 1px red;
}

/* Other border style example */
.three {
  border: dotted 2px red;
}
|LiveURL=http://marcin-wosinek.github.com/border/
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''border''' property is a shorthand property that sets the '''width''', '''style''', and '''color''' values for all four sides of an object. All individual border properties, that are not set by the composite border property are set to their default values. 

The default value for the [[css/properties/border-color|'''border-color''']] is the same as the text color, for [[css/properties/border-width|'''border-width''']] is <tt>medium</tt> and for [[css/properties/border-style|'''border-style''']] is <tt>none</tt>. Therefor you must specify a style when specifying a width or color; otherwise, the border will be invisible.

By setting '''border''', all other border properties are set to their default values; e.g. the value of [[css/properties/border-image|'''border-image''']]  is reset to default value <tt>none</tt>.
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
|Firefox_version=1.0 (1.7 or earlier)
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
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
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0(1.9.2)
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1.0
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
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
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/border
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms530744(v=vs.85).aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}