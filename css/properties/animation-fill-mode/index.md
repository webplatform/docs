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
There is no change to the property value between the time the animation  is applied ([[css/properties/animation-name|'''animationName''']]) and the time the animation begins playing ([[css/properties/animation-delay|'''animationDelay''']]) or after the animation completes ([[css/properties/animation-duration|'''animationDuration''']]).}}
{{CSS_Property_Value|Data Type=forwards |Description=The final property value (as defined in the last [[css/atrules/@keyframes|'''@keyframes''']] at-rule) is maintained after the animation completes.
The last '''@keyframes''' is the <code>to</code> or <code>100%</code> keyframe, unless [[css/properties/animation-direction|'''animationDirection''']] is set to <code>alternate</code> and it is a finite or even iteration count in which case  the last '''@keyframes''' is the <code>from</code> or <code>0%</code> keyframe.}}
{{CSS_Property_Value|Data Type=backwards |Description=The beginning property value (as defined in the first [[css/atrules/@keyframes|'''@keyframes''']] at-rule) is applied before the animation is displayed, during the period defined by [[css/properties/animation-delay|'''animationDelay''']].}}
{{CSS_Property_Value|Data Type=both |Description=Both <code>forwards</code> and <code>backwards</code> fill modes are applied.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Notes=
===Remarks===
The version of this property using a vendor prefix, '''-ms-animation-fill-mode''', has been deprecated. To ensure compatibility in the future, applications using this property with a vendor prefix should be updated accordingly.
|Import_Notes=
===Syntax===
<code>'''animation-fill-mode : '''none '''{{!}}''' forwards '''{{!}}''' backwards '''{{!}}''' both '''[''' ,  none '''{{!}}''' forwards '''{{!}}''' backwards '''{{!}}''' both ''']''' *</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223144 CSS Animations Module Level 3], Section 3.9


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
|Topic_clusters=Animation
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}