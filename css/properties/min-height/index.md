{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the minimum [[css/properties/height|height]] for an element. It prevents the height of the element to exceed the specified value.
It overrides both the height & the max-height property if any them is specified below the min-height value.
}}
{{CSS Property
|Initial value=auto (0 for non-flex elements)
|Applies to=All elements but non-replaced inline elements, table columns, and column groups
|Inherited=No
|Media=visual
|Computed value=The percentage as specified or the absolute length
|Animatable=Yes
|CSS object model property=min-height
|CSS percentages=Of the height of containing block. If the height of the containing block depends on the content & the element does not have position as absolute, then this value becomes 0.
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. Behaves as 0 for non-flexbox elements. On [[css/flexbox|flexbox]]  acts as min-content.
}}{{CSS Property Value
|Data Type=length
|Description=Specifies a fixed height. Negative values are not allowed. See [[css/data_types/length|length]] for possible units.
}}{{CSS Property Value
|Data Type=percentage
|Description=A <percentage> relative to the height of the containing block. If the containing block has no height explicitly set then is is treated as 0. Negative values are not allowed
}}{{CSS Property Value
|Data Type=calc
|Description=See [[css/functions/calc|css calc function]] for mode details.
}}{{CSS Property Value
|Data Type=inherit
|Description=Takes the same specified value as the property for the element's parent.
}}{{CSS Property Value
|Data Type=max-content
|Description=The narrowest space a box could take while fitting around its contents if none of the soft wrap opportunities within the box were taken.(Space/Punctuation in text are examples of a soft-wrap opportunity). Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.
}}{{CSS Property Value
|Data Type=min-content
|Description=The narrowest measure a box could take that doesn't lead to inline-dimension overflow that could be avoided by choosing a larger measure. Roughly, the measure that would fit around its contents if all soft wrap opportunities within the box were taken. Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.
}}{{CSS Property Value
|Data Type=fill-available
|Description=Fill the entire available space of from the containing block (Height minus horizontal margin, border and padding of the containing block). Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.
}}{{CSS Property Value
|Data Type=fit-content
|Description=If the total available space is finite, equals to min(max-content, max(min-content, fill-available)). Otherwise, equal to the max-content measure. Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Use min-height with any CSS selector to apply it.
|Code=/* Ensure all div elements are a min-height of 100px */
div { min-height: 100px }
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=min-height property overrides the height of an element.
|Code=&lt;style&gt;
/* min-height example */

/*Default width. Height is based on the content*/
.without-min-height, .with-min-height {
    width: 100px;
}

/*Max height overrides height*/
.with-min-height {
    background: cyan;
    min-height: 300px;
}

.without-min-height {
	background: red;
}

.content {
	border: 1px solid black;
	padding: 10px;
}
&lt;/style&gt;

&lt;div class="without-min-height"&gt;&lt;p class="content"&gt;Without Min Height. Height taken from content (with black border).&lt;/p&gt;&lt;/div&gt;
&lt;br /&gt;
&lt;div class="with-min-height"&gt;&lt;p class="content"&gt;With Min Height. Content (with black border) may not fill entirety of element.&lt;/p&gt;&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5842440
}}
}}
{{Notes_Section
|Usage=CSS min height is well supported across most browsers. A few things to consider while usage:
* min-height overrides [[css/properties/max-height|max-height]]. If min-height supplied is greater than max-height, max-height does not have an impact.
* max-content, min-content, fit-content, and fill-available are in W3C draft stage and not supported across all browsers.
* Support for [[css/functions/calc|calc]] is better across browsers. Vendor prefixes may be needed.
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1 (Section 10.7)
|URL=http://www.w3.org/TR/CSS2/visudet.html#min-max-heights
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=CSS Intrinsic & Extrinsic Sizing Module Level 3
|URL=http://dev.w3.org/csswg/css3-sizing/#width-height-keywords
|Status=Working Draft
|Relevant_changes=Adds max-content, min-content, fit-content, and fill-available.
}}
}}
{{See_Also_Section
|Topic_clusters=Box Model
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[html/attributes/height|height]]</code>
*<code>Other Resources</code>
*<code>Cascading Style Sheet Compatibility in Internet Explorer 7</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=length, percentage, inherit
|Chrome_supported=Yes
|Chrome_version=1
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=7
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=4
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Safari
|Version=1
|Note=Does not support min-height for positional elements. It was added in Safari 2.0.2 (416).
}}
}}