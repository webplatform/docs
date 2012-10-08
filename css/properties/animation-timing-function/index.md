{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=ease
|Applies to=block-level and inline-level elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=cubic-bezier( x1, y1, x2, y2 )
|Description=A timing function, based on a cubic-bezier curve, that takes four parameters. The four values specify the x and y-coordinates as (x<sub>1</sub>, y<sub>1</sub>, x<sub>2</sub>, y<sub>2</sub>) of the P<sub>1</sub> and P<sub>2</sub> points of the curve, respectively.

'''Note'''  For properties other than opacity and color, the cubic-bezier curve function accepts y-coordinates outside the standard range of [0, 1]. This allows the ability to specify "elastic" effects for properties such as length and width, as shown in the following image.
[[Image:msTransition-ease-in-out-elastic-cubic.png]]
}}{{CSS Property Value
|Data Type=ease
|Description=Default. A timing function, based on a cubic-bezier curve, that gradually increases in speed at the start, animates at full speed,  and then gradually decreases in speed at the end. This function is equivalent to <code>cubic-bezier(0.25,0.1,0.25,1)</code>.

[[Image:msTransition-ease-cubic.png]]
}}{{CSS Property Value
|Data Type=linear
|Description=A timing function, based on a cubic-bezier curve, that  has a consistent speed from start to end. This function is equivalent to <code>cubic-bezier(0,0,1,1)</code>.

[[Image:msTransition-linear-cubic.png]]
}}{{CSS Property Value
|Data Type=ease-in
|Description=A timing function, based on a cubic-bezier curve, that  gradually increases in speed at the start. This function is equivalent to <code>cubic-bezier(0.42,0,1,1)</code>.

[[Image:msTransition-ease-in-cubic.png]]
}}{{CSS Property Value
|Data Type=ease-out
|Description=A timing function, based on a cubic-bezier curve, that  gradually decreases in speed at the end. This function is equivalent to <code>cubic-bezier(0,0,0.58,1)</code>.

[[Image:msTransition-ease-out-cubic.png]]
}}{{CSS Property Value
|Data Type=ease-in-out
|Description=A timing function, based on a cubic-bezier curve, that  gradually increases in speed at the start and then gradually decreases in speed at the end. This function is equivalent to <code>cubic-bezier(0.42,0,0.58,1)</code>.

[[Image:msTransition-ease-in-out-cubic.png]]
}}{{CSS Property Value
|Data Type=steps( &lt;interval_number&gt; [, start  | end ])
|Description=A stepped timing function that takes two parameters. The first parameter specifies the number of intervals; the optional second parameter specifies the point in the interval where the property value changes. The second parameter is constrained to the values <code>start</code> or <code>end</code>, which is the default.
}}{{CSS Property Value
|Data Type=step-start
|Description=A stepped timing function that is equivalent to <code>steps(1, start)</code>.
}}{{CSS Property Value
|Data Type=step-end
|Description=A stepped timing function that is equivalent to <code>steps(1, end)</code>.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The version of this property using a vendor prefix, '''-ms-animation-timing-function''', has been deprecated. To ensure compatibility in the future, applications using this property with a vendor prefix should be updated accordingly.
|Import_Notes====Syntax===
<code>'''animation-timing-function: '''cubic-bezier( x1, y1, x2, y2 ) '''{{!}}''' ease '''{{!}}''' linear '''{{!}}''' ease-in '''{{!}}''' ease-out '''{{!}}''' ease-in-out '''{{!}}''' steps( &lt;interval_number&gt; [, start  {{!}} end ]) '''{{!}}''' step-start '''{{!}}''' step-end '''[''' ,  cubic-bezier( x1, y1, x2, y2 ) '''{{!}}''' ease '''{{!}}''' linear '''{{!}}''' ease-in '''{{!}}''' ease-out '''{{!}}''' ease-in-out '''{{!}}''' steps( &lt;interval_number&gt; [, start  {{!}} end ]) '''{{!}}''' step-start '''{{!}}''' step-end ''']''' *</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223144 CSS Animations Module Level 3], Section 3.4
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
|Topic_clusters=Animation
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