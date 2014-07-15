{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, spec reference, standardization status
|Checked_Out=No
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
|Description=Default. Ruby text overhangs any other text adjacent to the base text.
}}{{CSS Property Value
|Data Type=whitespace
|Description=Ruby text overhangs only white-space characters.
}}{{CSS Property Value
|Data Type=none
|Description=Ruby text overhangs only text adjacent to its base.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''ruby-overhang''' attribute and the '''ruby-overhang''' property to set the overhang of the ruby text. It uses an inline style sheet to set the '''ruby-overhang''' attribute to '''none'''.
|Code=&lt;RUBY ID{{=}}oRuby STYLE {{=}} "ruby-overhang: none"&gt;
Ruby base.
&lt;RT&gt;Ruby text.
&lt;/RUBY&gt;
&lt;INPUT
TYPE{{=}}button VALUE{{=}}"Whitespace"
onclick{{=}}"oRuby.style.rubyOverhang{{=}}'whitespace';"
&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rubyoverhang.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''ruby-overhang''' property specifies the overhang of the ruby text defined by the '''rt''' object, and is set on the '''ruby''' object.
|Import_Notes====Syntax===
<code>'''ruby-overhang: '''auto '''{{!}}''' whitespace '''{{!}}''' none</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203763 CSS3 Ruby Module], Section 4.3
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
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
|Blackberry_version=18.0
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
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=5.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/ruby-align|ruby-align]]</code>
*<code>[[css/properties/ruby-position|ruby-position]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}