{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=block-level and inline-level elements
|Media=visual
|Inherited=No
|Initial value=none
|Values={{CSS_Property_Value|Data Type=none |Description=Default. 
No animation is applied.}}
{{CSS_Property_Value|Data Type=identifier |Description=The name of the [[css/atrules/@keyframes|'''@keyframes''']] at-rule.}}
{{CSS_Property_Value|Data Type=-ms-bar |Description=For the indeterminate '''progress''' control only, changes the appearance to a bar.}}
{{CSS_Property_Value|Data Type=-ms-ring |Description=For the indeterminate '''progress''' control only, changes the appearance to a ring.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Notes=
===Remarks===
The version of this property using a vendor prefix, '''-ms-animation-name''', has been deprecated. To ensure compatibility in the future, applications using this property with a vendor prefix should be updated accordingly.

====Controlling the progress ring style====
To change the appearance of a '''ms-fill''' pseudo-element. Here are some examples:
|Import_Notes=
===Syntax===
<code>'''animation-name: '''none '''{{!}}''' ''identifier'' '''[''' ,  none '''{{!}}''' ''identifier'' ''']''' *</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223144 CSS Animations Module Level 3], Section 3.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[html/elements/a|a]]</code>
*<code>abbr</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>b</code>
*<code>bdo</code>
*<code>big</code>
*<code>br</code>
*<code>cite</code>
*<code>code</code>
*<code>dfn</code>
*<code>em</code>
*<code>i</code>
*<code>img</code>
*<code>input</code>
*<code>kbd</code>
*<code>label</code>
*<code>q</code>
*<code>samp</code>
*<code>select</code>
*<code>small</code>
*<code>span</code>
*<code>strong</code>
*<code>sub</code>
*<code>sup</code>
*<code>textArea</code>
*<code>tt</code>
*<code>var</code>
*<code>address</code>
*<code>blockQuote</code>
*<code>div</code>
*<code>dl</code>
*<code>fieldSet</code>
*<code>form</code>
*<code>noFrames</code>
*<code>noScript</code>
*<code>ol</code>
*<code>p</code>
*<code>pre</code>
*<code>[[html/elements/table|table]]</code>
*<code>ul</code>
*<code>dd</code>
*<code>dt</code>
*<code>li</code>
*<code>tBody</code>
*<code>td</code>
*<code>tFoot</code>
*<code>th</code>
*<code>tHead</code>
*<code>tr</code>
*<code>button</code>
*<code>del</code>
*<code>ins</code>
*<code>map</code>
*<code>object</code>
*<code>script</code>
*<code>ms-fill</code>
*<code>[[css/atrules/@keyframes|@keyframes]]</code>
|Topic_clusters=Animation
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}