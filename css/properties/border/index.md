{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Shorthand property that defines the different properties of all four sides of an element's border in a single declaration. It can be used to set [[css/properties/border-width|'''border-width''']], [[css/properties/border-style|'''border-style''']] and [[css/properties/border-color|'''border-color''']], or a subset of these. Note that as well as defining properties for all four sides of an element's border at once, you can also target borders on specific sides individually — for example [[css/properties/border-top|'''border-top''']] and [[css/properties/border-right|'''border-right''']] — or even specific properties of individual borders — for example [[css/properties/border-top-color|'''border-top-color''']] and [[css/properties/border-right-color|'''border-right-color''']].}}
{{CSS Property
|Initial value=medium none currentColor
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=concatenation of <code>width</code> (the default <code>medium</code> is 3px in most browsers), <code>style</code> (<code>none</code> or <code>hidden</code>), and <code>color</code> (the equivalent RGB or RGBA value of the color).
|Animatable=Yes
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
|Language=HTML
|Description=A simple example showing multiple <code>&lt;div&gt;</code>s, identical in style except that they have different <code>border</code> properties applied to them.
|Code=&lt;div class="one"&gt;&lt;p&gt;One&lt;/p&gt;&lt;/div&gt;
&lt;div class="two"&gt;&lt;p&gt;Two&lt;/p&gt;&lt;/div&gt;
&lt;div class="three"&gt;&lt;p&gt;Three&lt;/p&gt;&lt;/div&gt;
&lt;div class="four"&gt;&lt;p&gt;Four&lt;/p&gt;&lt;/div&gt;
&lt;div class="five"&gt;&lt;p&gt;Five&lt;/p&gt;&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5534182
}}{{Single Example
|Language=CSS
|Code=/**
 * border example
**/

div {
  width: 150px;
  height: 150px;
  margin: 1rem;
  float: left;
}

p {
  padding: 2rem;
}

.one {
  /* The most basic border example you can show. */ 
  border: 1px solid black;
}

.two {
  /* If you don't explicitly set a color, currentColor is used, which
     equates to the text colour of the element, in this case black.   */
  border: 4px dashed;
}

.three {
  /* When no width is specified, the default width medium is used,
     which computes to about 3px in most browsers */
  border: dotted red;
}

.four {
  /* When no border style is specified, the border won't appear,
     as the default border style is none. */
  border: 10px black;
}

.five {
  /* A more interesting border example to round things off. */
  border: 10px inset rgba(234,190,50,0.75);
}
|LiveURL=http://code.webplatform.org/gist/5534182
}}
}}
{{Notes_Section
|Usage=
* The initial value is the concatenated result of the 3 component values. For <code>border-width</code> the initial value is <code>medium</code>, which is computed as about 3px in most browsers. For <code>color</code>, the initial value is <code>currentColor</code>. For <code>boder-style</code>, the initial value is <code>none</code>.
* It is usual to use the <code>border</code> property (or properties for individual sides, e.g. <code>border-left</code>) to set the default state of a box, and then override individual values using more specific propreties, such as <code>border-width</code> or <code>border-top-color</code>.
* individual border properties such as <code>border-bottom</code> can be used as a divider between horizontally or vertically laid out items, such as a navigation menu items, or table cells.
* A common technique is to use <code>border-bottom</code> properties for link underlining rather than <code>text-decoration: underline</code>, as it affords the designer more control.
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
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}