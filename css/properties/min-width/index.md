{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the minimum width of an element. It limits the width property to be not smaller than the value specified in min-width.}}
{{CSS Property
|Initial value=0
|Applies to=all elements but non-replaced inline elements, tables, inline tables, table cells, table columns, and column groups
|Inherited=No
|Media=visual
|Computed value=the percentage as specified or the absolute length or 'none'
|Animatable=Yes
|CSS object model property=min-width
|CSS percentages=yes
|Values={{CSS Property Value
|Data Type=length
|Description=Specifies a fixed width. Negative values are not allowed. See [[css/data_types/length|length]] for possible units.
}}{{CSS Property Value
|Data Type=percentage
|Description=A <percentage> relative to the width of the containing block. If the containing block has no width explicitly set then is is treated as none. Negative values are not allowed.
}}{{CSS Property Value
|Data Type=calc()
|Description=See [[css/functions/calc|css calc function]] for mode details.
}}{{CSS Property Value
|Data Type=inherit
|Description=Takes the same specified value as the property for the element's parent.
}}{{CSS Property Value
|Data Type=none
|Description=Default. Clears the min-width value. The width property can have any value.
}}{{CSS Property Value
|Data Type=max-content
|Description=The narrowest space a box could take while fitting around its contents if none of the soft wrap opportunities within the box were taken.(Space/Punctuation in text are examples of a soft-wrap opportunity). Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.
}}{{CSS Property Value
|Data Type=min-content
|Description=The narrowest measure a box could take that doesn't lead to inline-dimension overflow that could be avoided by choosing a larger measure. Roughly, the measure that would fit around its contents if all soft wrap opportunities within the box were taken. Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.
}}{{CSS Property Value
|Data Type=fill-available
|Description=Fill the entire available space of from the containing block (Width minus vertical margin, border and padding of the containing block). Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.
}}{{CSS Property Value
|Data Type=fit-content
|Description=If the total available space is finite, equals to min(max-content, max(min-content, fill-available)). Otherwise, equal to the max-content measure. Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=Use min-width with any CSS selector to apply it.
|Code=/* Restrict all div elements to a min-width of 100px */
div { min-width: 100px }
}}{{Single Example
|Language=HTML
|Description=Constrain the width of a '''div''' element using '''min-width''' and [[css/properties/max-width|'''max-width''']] attributes.
|Code=&lt;style&gt;
/* Width set to 50% */
.width {
    width:50%;
    background:#eee;
}

/* min-width set to 600px */
.minwidth {
	width: 50%;
	min-width: 600px;
	background: lightblue;
}	

/* max-width set to 600px */
.maxwidth {
	width: 50%;
	max-width: 200px;
	background: lightgreen
}

/* Content with border and padding */
.content {
    border:1px solid #c00;
    padding:5px;
}
&lt;/style&gt;

&lt;h3&gt;Resize the window to grow and shrink the div from max to min width.&lt;/h3&gt;
&lt;div class="width"&gt;
        &lt;p class="content"&gt;This div also has a width of 50%. &lt;br/&gt;&lt;br/&gt;
         Note that the div height increases to accommodate the flow of text.&lt;/p&gt;
&lt;/div&gt;
&lt;div class="minwidth"&gt;
	&lt;p class="content"&gt;This div also has a width of 50%.&lt;br /&gt;&lt;br /&gt; It also has a min-width of 600px.&lt;/p&gt;
&lt;/div&gt;
&lt;div class="maxwidth"&gt;
	&lt;p class="content"&gt;This div also has a width of 50%.&lt;br /&gt;&lt;br /&gt; It also has a max-width of 200px.&lt;/p&gt;
&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5842171
}}
}}
{{Notes_Section
|Usage=CSS min width is well supported across most browsers. A few things to consider while usage:
* min-width overrides [[css/properties/max-width|max-width]]. If min-width supplied is greater than max-width, max-width does not have an impact.
* max-content, min-content, fit-content, and fill-available are in W3C draft stage and not supported across all browsers.
* Support for [[css/functions/calc|calc]] is better across browsers. Vendor prefixes may be needed.
|Notes====Remarks===
The '''min-width'''/[[css/properties/max-width|'''max-width''']] attributes apply to floating and absolutely positioned block and inline-block elements, as well as some intrinsic controls. They do not apply to non-replaced inline elements, such as table rows and row/column groups. (A "replaced" element has intrinsic dimensions, such as an '''img''' or '''textArea'''.)
This property is enabled only under the strict [[html/elements/!DOCTYPE|!DOCTYPE]].
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1 (Section 10.7)
|URL=http://www.w3.org/TR/CSS2/visudet.html#min-max-widths
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
|Feature=min-width
|Chrome_supported=Yes
|Chrome_version=4.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=2.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=7.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.0
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.1
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=min-width
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=18.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=10.0
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=5.0
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
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