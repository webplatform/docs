{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Specifies the type of list-item marker in a list.}}
{{CSS Property
|Initial value=disc
|Applies to=elements with 'display: list-item'
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=armenian
|Description=The marker is traditional Armenian numbering
}}{{CSS Property Value
|Data Type=circle
|Description=circle
}}{{CSS Property Value
|Data Type=decimal
|Description=number. This is default for &lt;ol&gt;
}}{{CSS Property Value
|Data Type=decimal-leading-zero
|Description=number with leading zeros (01, 02, 03, etc.)
}}{{CSS Property Value
|Data Type=disc
|Description=filled circle. This is default for &lt;ul&gt;
}}{{CSS Property Value
|Data Type=georgian
|Description=traditional Georgian numbering
}}{{CSS Property Value
|Data Type=inherit
|Description=The value of the listStyleType property is inherited from parent element
}}{{CSS Property Value
|Data Type=lower-alpha
|Description=lower-alpha (a, b, c, d, e, etc.)
}}{{CSS Property Value
|Data Type=lower-greek
|Description=lower-greek
}}{{CSS Property Value
|Data Type=lower-latin
|Description=lower-latin (a, b, c, d, e, etc.)
}}{{CSS Property Value
|Data Type=lower-roman
|Description=lower-roman (i, ii, iii, iv, v, etc.)
}}{{CSS Property Value
|Data Type=none
|Description=No marker is shown
}}{{CSS Property Value
|Data Type=square
|Description=square
}}{{CSS Property Value
|Data Type=upper-alpha
|Description=upper-alpha (A, B, C, D, E, etc.)
}}{{CSS Property Value
|Data Type=upper-latin
|Description=upper-latin (A, B, C, D, E, etc.)
}}{{CSS Property Value
|Data Type=upper-roman
|Description=upper-roman (I, II, III, IV, V, etc.)
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following examples use the '''list-style-type''' attribute and the '''list-style-type''' property to set the markers.

This example uses '''ul''' as a selector in an embedded (global) style sheet to change the marker type to '''circle'''.
|Code=&lt;style&gt;
    ul { list-style-type:circle }
&lt;/style&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/list-style-type.htm
}}{{Single Example
|Description=This example demonstrates the newer line-item markers added for Internet Explorer 8.
|Code=&lt;style type{{=}}"text/css"&gt;
.decleadzero {
	list-style-type: decimal-leading-zero;
}
...
&lt;/style&gt;
&lt;body&gt;
 &lt;ol class{{=}}"decleadzero"&gt;
  &lt;li&gt;This is the first item. &lt;/li&gt;
  &lt;li&gt;This is the second item. &lt;/li&gt;
  &lt;li&gt;This is the third item. &lt;/li&gt;
 &lt;/ol&gt;
    ...
&lt;/body&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/list-style-type_ie8.htm
}}{{Single Example
|Language=CSS
|Description=Using the list-style-type on ordered lists
|Code=/**
 * using list-style-type on ordered lists
 * the default for ol's is list-style-type: decimal
 */

.list-style--leading-zero {
	list-style-type:  decimal-leading-zero;
}

.list-style--roman {
	list-style-type:  upper-roman; /* you can also use lower-roman */
}
|LiveURL=http://code.webplatform.org/gist/5597602
}}{{Single Example
|Language=CSS
|Description=If the left padding of a line item is set to 0 using one of the padding properties, the list-item markers do not show. The padding should be set to a minimum of 30 points.
|Code=/*
If the left padding is set to 0 the list-item markers do not show
*/
ul {
	padding:0;
}
|LiveURL=http://code.webplatform.org/gist/5597612
}}
}}
{{Notes_Section
|Notes====Notes===
*The color of the marker will be the same as the computed color of the element it applies to.

*Some list-style-types require a suitable font installed to display as expected.

*The CSS specification does not define how alphabetic systems wrap at the end of the alphabet. For instance, after 26 list items, upper-alpha rendering is undefined. Firefox and other browsers will continue as AA, AB, AC,... For long lists, it is recommended that authors specify true numbers.

*The list styles hebrew, cjk-ideographs, hiragana, katakana, hiragana-iroha and katakana-iroha are specified in CSS2 and removed from CSS 2.1 due to lack of implementation experience. They are expected to return in the CSS3 Lists module.

* The property also supports a shorthand syntax which is list-style

* If the left padding of a line item is set to 0 using one of the padding properties, the list-item markers do not show. The padding should be set to a minimum of 30 points.
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
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0 (85)
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=9
|Note=do not support: cjk-ideographic, hebrew, hiragana, hiragana-iroha, katakana, and katakana-iroha
}}{{Compatibility Notes Row
|Browser=Opera
|Version=11
|Note=do not support: cjk-ideographic, hebrew, hiragana, hiragana-iroha, katakana, and katakana-iroha
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8, and earlier
|Note=only support the property values: decimal-leading-zero, lower-greek, lower-latin, upper-latin, armenian, georgian, and inherit if a DOCTYPE is specified.
}}
}}
{{See_Also_Section
|Topic_clusters=Generated and Replaced Content
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/list-style-type
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}