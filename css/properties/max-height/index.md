{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets the maximum [[css/properties/height|height]] for an element. It prevents the height of the element to exceed the specified value. If [[css/properties/min-height|min-height]] is specified and is greater than max-height, max-height is overridden.}}
{{CSS Property
|Initial value=none
|Applies to=All elements but non-replaced inline elements, table columns, and column groups
|Inherited=No
|Media=visual
|Computed value=The percentage as specified or the absolute length or 'none'
|Animatable=Yes
|CSS object model property=max-height
|CSS percentages=refer to height of containing block
|Values={{CSS Property Value
|Data Type=length
|Description=Specifies a fixed height. Negative values are not allowed. See [[css/units/length|length]] for possible units.
}}{{CSS Property Value
|Data Type=percentage
|Description=A <percentage> relative to the height of the containing block. If the containing block has no height explicitly set then is is treated as none. Negative values are not allowed.
}}{{CSS Property Value
|Data Type=calc()
|Description=See [[css/functions/calc|css calc function]] for mode details.
}}{{CSS Property Value
|Data Type=inherit
|Description=Takes the same specified value as the property for the element's parent.
}}{{CSS Property Value
|Data Type=none
|Description=Clears the max-height value. The height property can have any value.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Use max-height with any CSS selector to apply it.
|Code=/* Restrict all div elements to a max-height of 10px */
div { max-height: 10px }
}}{{Single Example
|Language=HTML
|Description=max-height property overrides the height of an element.
|Code=&lt;style&gt;
/*Default width. Height is based on the content*/
.without-max-height, .with-max-height {
    width: 100px;
}
/*Max height overrides height*/
.with-max-height {
    background: cyan;
    max-height: 50px;
}
.without-max-height {
	background: red;
}
&lt;/style&gt;
&lt;div class=&quot;without-max-height&quot;&gt;Without Max Height. Height taken from content&lt;/div&gt;
&lt;br&gt;
&lt;div class=&quot;with-max-height&quot;&gt;With Max Height. Content may overflow if it goes beyond height.&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5070850
}}
}}
{{Notes_Section
|Notes====Remarks===
'''max-height''' was introduced in Windows Internet Explorer 7.
The [[css/properties/min-height|'''min-height''']]/'''max-height''' attributes apply to floating and absolutely positioned block and inline-block elements, as well as some intrinsic controls. They do not apply to non-replaced inline elements, such as table columns and row/column groups. (A "replaced" element has intrinsic dimensions, such as an '''img''' or '''textArea'''.)
This property is enabled only under the strict [[html/elements/!DOCTYPE|!DOCTYPE]].
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1 (Section 10.7)
|URL=http://www.w3.org/TR/CSS2/visudet.html#min-max-heights
|Status=W3C Recommendation
}}{{Related Specification
|Name=CSS Intrinsic & Extrinsic Sizing Module Level 3
|URL=http://dev.w3.org/csswg/css3-sizing/#width-height-keywords
|Status=Working Draft
|Relevant_changes=Adds max-content, min-content, fit-content, and fill-available.
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=4
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=2
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=7
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=CSS Intrinsic & Extrinsic Sizing.
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=3
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=0
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=10
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=5
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=7/8
|Note='inherit' is not supported in IE7. IE8 requires strict !DOCTYPE for 'inherit'
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=7/8
|Note=Known bugs when used along overflow: auto/scroll.
}}{{Compatibility Notes Row
|Browser=Chrome/Safari
|Note=Support intrinsic(max-content) & min-intrinsic(min-content)
}}
}}
{{See_Also_Section
|Topic_clusters=Box Model
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Cascading Style Sheet Compatibility in Internet Explorer 7</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}