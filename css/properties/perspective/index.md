{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=none
|Applies to=block-level and inline-level elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=none
|Description=Default. 
No perspective declared.
}}{{CSS Property Value
|Data Type=number
|Description=A floating-point number, followed by a relative units designator
(<code>px</code>), that indicates the depth of the perspective.
For more information about supported length units,
see CSS Values and Units.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The version of this property using a vendor prefix, '''-ms-perspective''', has been deprecated. To ensure compatibility in the future, applications using this property with a vendor prefix should be updated accordingly.
This property does not affect how the object is rendered.
This property is only applied to child elements that have a [[css/transforms/transform|'''transform''']] specified.
The  object is the projection plane for the child elements.
This property specifies that each child is rendered relative to the specified perspective, whereas the '''perspective''' function of the [[css/transforms/transform|'''transform''']] property specifies that each child is rendered from the same perspective.
The following images illustrate the difference between this property and the '''perspective''' function of the [[css/transforms/transform|'''transform''']] property.
[[Image:msTransform-perspective-children.png]][[Image:msPerspective-children.png]]
|Import_Notes====Syntax===
<code>'''perspective: '''none '''{{!}}''' ''
&lt;number&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223145 CSS Transforms Module, Level 3], Section 10
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
|Topic_clusters=Transforms
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
*<code>[[css/transforms/transform|transform]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}