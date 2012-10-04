{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=No
|Initial value=
|Values={{CSS_Property_Value|Data Type=auto |Description=Default. Ruby text overhangs any other text adjacent to the base text.}}
{{CSS_Property_Value|Data Type=whitespace |Description=Ruby text overhangs only white-space characters.}}
{{CSS_Property_Value|Data Type=none |Description=Ruby text overhangs only text adjacent to its base.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''ruby-overhang''' attribute and the '''ruby-overhang''' property to set the overhang of the ruby text. It uses an inline style sheet to set the '''ruby-overhang''' attribute to '''none'''.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rubyoverhang.htm
|Code=
&lt;RUBY ID{{=}}oRuby STYLE {{=}} "ruby-overhang: none"&gt;
Ruby base.
&lt;RT&gt;Ruby text.
&lt;/RUBY&gt;
&lt;INPUT
TYPE{{=}}button VALUE{{=}}"Whitespace"
onclick{{=}}"oRuby.style.rubyOverhang{{=}}'whitespace';"
&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''ruby-overhang''' property specifies the overhang of the ruby text defined by the '''rt''' object, and is set on the '''ruby''' object.
|Import_Notes=
===Syntax===
<code>'''ruby-overhang: '''auto '''{{!}}''' whitespace '''{{!}}''' none</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203763 CSS3 Ruby Module], Section 4.3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/ruby-align|ruby-align]]</code>
*<code>[[css/properties/ruby-position|ruby-position]]</code>
|Topic_clusters=Ruby
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}