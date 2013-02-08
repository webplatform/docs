{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The 'transition-duration' property specifies the length of time a transition animation takes to complete.}}
{{CSS Property
|Initial value=0
|Applies to=all elements, :before and :after pseudo elements
|Inherited=No
|Media=interactive
|Animatable=No
|Values={{CSS Property Value
|Data Type=time
|Description=Floating-point number, followed by a time units designator (<code>ms</code> or <code>s</code>). For more information about the supported time units, see '''CSS Values and Units Reference'''.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The version of this property using a vendor prefix, '''-ms-transition-duration''', has been deprecated. To ensure compatibility in the future, applications using this property with a vendor prefix should be updated accordingly.
Transitions respect Cascading Style Sheets (CSS) box model constraints such as [[css/properties/min-width|'''min-width''']].
For example, if an element is declared with a [[css/properties/min-width|'''min-width''']] value of <code>50px</code> then a transition to a width of <code>25px</code> is not valid. In a case such as this, the transition runs for the specified duration from the start value until a valid maximum or minimum end value, as appropriate.
|Import_Notes====Syntax===
<code>'''transition-duration: '''''
&lt;time&gt;
'' '''[''' ,  ''
&lt;time&gt;
'' ''']''' *</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223140 CSS Transitions Module Level 3], Section 2.2
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=22.0
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Yes
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Yes
|Internet_explorer_prefixed_version=10.0
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=12.0
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=5.1
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Transistions
|Manual_sections====Related pages (MSDN)===
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
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}