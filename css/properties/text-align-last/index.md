{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The <code>text-align-last</code> CSS property describes how the last line of a block element or a line before line break is aligned in its parent block element.}}
{{CSS Property
|Initial value=auto
|Applies to=block containers
|Inherited=Yes
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=textAlignLast
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. Text is aligned like the other lines in the object, using the value of the [[css/properties/text-align|'''text-align''']] property.
}}{{CSS Property Value
|Data Type=start
|Description=The same as <code>left</code> if direction is left-to-right and <code>right</code> if direction is right-to-left.
}}{{CSS Property Value
|Data Type=end
|Description=The same as <code>right</code> if direction is left-to-right and <code>left</code> if direction is right-to-left.
}}{{CSS Property Value
|Data Type=left
|Description=Text is aligned to the left.
}}{{CSS Property Value
|Data Type=right
|Description=Text is aligned to the right.
}}{{CSS Property Value
|Data Type=center
|Description=The text is centered within the line box.
}}{{CSS Property Value
|Data Type=justify
|Description=Text is justified if ‘text-justify’ is ‘distribute’,  and the same as <code>start</code> value if otherwise.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example shows an embedded style rule that justifies all the lines in the document's '''p''' elements.  This is sometimes found in East Asian typography.
|Code=&lt;p class="normal"&gt;Simple example with "auto" value of text-align-last property. This paragraph needs to be really long in order to show how to work with text-align-last property. It only works because we set a width for this paragraph though.&lt;/p&gt;

&lt;p class="justified"&gt;Simple example with "justify" value of text-align-last property. In this case, the last line is also justified. This paragraph needs to be really long in order to show how to work with text-align-last property.&lt;/p&gt;
|LiveURL=http://code.webplatform.org/gist/5664996
}}{{Single Example
|Language=CSS
|Code=.normal { 
	width: 300px;
	text-align: justify;
	text-align-last: auto;
}

.justified { 
	width: 300px;
	text-align: justify;
	text-align-last: justify;
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Module Level 3
|URL=http://www.w3.org/TR/css3-text/#text-align-last
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=12.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=5.5
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Yes
|Firefox_mobile_prefixed_version=12.0 (-moz)
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Text
|Manual_links=*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}