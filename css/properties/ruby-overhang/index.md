{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
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
|Desktop_rows=
|Mobile_rows=
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