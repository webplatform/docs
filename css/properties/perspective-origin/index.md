{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=50% 50%
|Applies to=block-level and inline-level elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=length
|Description=A floating-point number, followed by either an absolute units designator
(<code>cm</code>,
<code>mm</code>,
<code>in</code>,
<code>pt</code>,
or <code>pc</code>)
or a relative units designator
(<code>em</code>,
<code>ex</code>,
or <code>px</code>), that indicates the origin of transformation.
For more information about the supported length units,
see CSS Values and Units.
}}{{CSS Property Value
|Data Type=percentage
|Description=An integer, followed by a %. The value is a percentage of the total box length (for the first value) or the total box height (for the second value, if specified).
}}{{CSS Property Value
|Data Type=left
|Description=First value only. Equal to 0% or a zero length.
}}{{CSS Property Value
|Data Type=center
|Description=First value only. Equal to 50% or half the length of the box.
}}{{CSS Property Value
|Data Type=right
|Description=First value only. Equal to 100% or the full box length.
}}{{CSS Property Value
|Data Type=top
|Description=Second value only. Equal to 0% or a zero height.
}}{{CSS Property Value
|Data Type=center
|Description=Second value only. Equal to 50% or a half the height of the box.
}}{{CSS Property Value
|Data Type=bottom
|Description=Second value only. Equal to 100% or the full box height.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The version of this property using a vendor prefix, '''-ms-perspective-origin''', has been deprecated. To ensure compatibility in the future, applications using this property with a vendor prefix should be updated accordingly.
This property does not affect how the object is rendered.
This property has no effect on the child elements if the [[css/properties/perspective|'''perspective''']] property is not set for the object.
|Import_Notes====Syntax===
<code>'''perspective-origin: ''''''[''' '''[''' ''
&lt;percentage&gt;
'' '''{{!}}''' ''
&lt;length&gt;
'' '''{{!}}''' left '''{{!}}''' center '''{{!}}''' right ''']''' '''[''' ''
&lt;percentage&gt;
'' '''{{!}}''' ''
&lt;length&gt;
'' '''{{!}}''' top '''{{!}}''' center '''{{!}}''' bottom ''']''' ? ''']''' '''{{!}}''' '''[''' '''[''' left '''{{!}}''' center '''{{!}}''' right ''']''' {{!}}{{!}} '''[''' top '''{{!}}''' center '''{{!}}''' bottom ''']''' ''']'''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223145 CSS Transforms Module, Level 3], Section 11
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