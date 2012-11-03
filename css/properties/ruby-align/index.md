{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. Browser determines how the ruby text is aligned. The recommended behavior for an ideographic (Asian character) ruby is to be aligned in the <code>distribute-space</code> mode. The recommended behavior for a Latin character ruby is to be aligned in the <code>center</code> mode.
}}{{CSS Property Value
|Data Type=left
|Description=Ruby text is left-aligned with the base.
}}{{CSS Property Value
|Data Type=center
|Description=Ruby text is centered within the width of the base. If the length of the base is smaller than the length of the ruby text, the base is centered within the width of the ruby text.
}}{{CSS Property Value
|Data Type=right
|Description=Ruby text is right-aligned with the base.
}}{{CSS Property Value
|Data Type=distribute-letter
|Description=Ruby text is evenly distributed across the width of the base if the width of the ruby text is smaller than the width of the base. If the width of the ruby text is at least the width of the base, the ruby text is center-aligned.
}}{{CSS Property Value
|Data Type=distribute-space
|Description=Ruby text is evenly distributed across the width of the base if the width of the ruby text is smaller than the width of the base. White space precedes the first and follows the last character in the ruby text, equal to half the kerning of the ruby text. If the width of the ruby text is at least the width of the base, the ruby text is centered.
}}{{CSS Property Value
|Data Type=line-edge
|Description=Ruby text is centered if it is not adjacent to a line edge. If it is adjacent to a line edge, the side of the ruby text lines up with the side of the base text.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''ruby-align''' attribute and the '''ruby-align''' property to set the alignment of the ruby text. It uses an inline style sheet to set the '''ruby-align''' attribute to <code>right</code>.
|Code=&lt;RUBY ID{{=}}oRuby STYLE {{=}} "ruby-align: right"&gt;
Ruby base.
&lt;RT&gt;Ruby text.
&lt;/RUBY&gt;
&lt;INPUT
TYPE{{=}}button VALUE{{=}}"Center"
onclick{{=}}"oRuby.style.rubyAlign{{=}}'center';"
&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rubyAlign.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''ruby-align''' property specifies the alignment of the ruby text defined by the '''rt''' object, and is set on the '''ruby''' object.
|Import_Notes====Syntax===
<code>'''ruby-align: '''auto '''{{!}}''' left '''{{!}}''' center '''{{!}}''' right '''{{!}}''' distribute-letter '''{{!}}''' distribute-space '''{{!}}''' line-edge</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203763 CSS3 Ruby Module], Section 4.2
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=5.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
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
|Safari_supported=Yes
|Safari_version=5.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=18.0
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=10.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=5.1
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Ruby
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/ruby-position|ruby-position]]</code>
*<code>[[css/properties/ruby-overhang|ruby-overhang]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}