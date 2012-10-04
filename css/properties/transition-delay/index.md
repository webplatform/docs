{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=all elements, :before and :after pseudo elements
|Media=interactive
|Inherited=No
|Initial value=0
|Values={{CSS_Property_Value|Data Type=time |Description=Floating-point number, followed by a time units designator (<code>ms</code> or <code>s</code>). For more information about the supported time units, see '''CSS Values and Units Reference'''.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Notes=
===Remarks===
The version of this property using a vendor prefix, '''-ms-transition-delay''', has been deprecated. To ensure compatibility in the future, applications using this property with a vendor prefix should be updated accordingly.
This property accepts <code>s</code> and <code>ms</code> as valid units of time.
Values are rounded up to the second decimal place.
Each '''transition-delay''' is paired with a corresponding object property  identified in the [[css/properties/transition-property|'''transition-property''']] property.
If more '''transition-delay''' values are declared than corresponding object properties identified in the [[css/properties/transition-property|'''transition-property''']] property, the excess '''transition-delay''' values are ignored.
If fewer  '''transition-delay''' values are declared than corresponding object properties identified in the [[css/properties/transition-property|'''transition-property''']] property, the list of '''transition-delay''' values is repeated from the beginning until the object properties are exhausted.
|Import_Notes=
===Syntax===
<code>'''transition-delay: '''''
&lt;time&gt;
'' '''[''' ,  ''
&lt;time&gt;
'' ''']''' *</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223140 CSS Transitions Module Level 3], Section 2.4


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
|Topic_clusters=Transistions
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}