{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Sets the pace of the transition to the next keyframe of an animation}}
{{CSS Property
|Initial value=ease
|Applies to=all elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=single-animation-timing-function
|Description=A keyword or function that describes how the animation progresses between keyframes.

;<code>ease</code>
:Default. A timing function, based on a cubic-bezier curve, that gradually increases in speed at the start, animates at full speed,  and then gradually decreases in speed at the end. This function is equivalent to <code>cubic-bezier(0.25,0.1,0.25,1)</code>. [[Image:msTransition-ease-cubic.png]]
;<code>linear</code>
:A timing function, based on a cubic-bezier curve, that  has a consistent speed from start to end. This function is equivalent to <code>cubic-bezier(0,0,1,1)</code>. [[Image:msTransition-linear-cubic.png]]
;<code>ease-in</code>
:A timing function, based on a cubic-bezier curve, that  gradually increases in speed at the start. This function is equivalent to <code>cubic-bezier(0.42,0,1,1)</code>. [[Image:msTransition-ease-in-cubic.png]]
;<code>ease-out</code>
:A timing function, based on a cubic-bezier curve, that  gradually decreases in speed at the end. This function is equivalent to <code>cubic-bezier(0,0,0.58,1)</code>. [[Image:msTransition-ease-out-cubic.png]]
;<code>ease-in-out</code>
:A timing function, based on a cubic-bezier curve, that  gradually increases in speed at the start and then gradually decreases in speed at the end. This function is equivalent to <code>cubic-bezier(0.42,0,0.58,1)</code>. [[Image:msTransition-ease-in-out-cubic.png]]
;<code>steps(number, position)</code>
:The change takes place in the number of equal steps specified in the first argument. The optional second argument should be either the keyword <code>start</code> or <code>end</code>. It specifies whether the change takes place at the start or end of each step. If the second argument is omitted, it defaults to <code>end</code>.
;<code>step-start</code>
:The change takes place at the start of the keyframe. This is equivalent to <code>steps(1, start)</code>.
;<code>step-end</code>
:The change takes place at the end of the keyframe. This is equivalent to <code>steps(1, end)</code>.
;<code>cubic-bezier( x1, y1, x2, y2 )</code>
:A timing function, based on a cubic-bezier curve, that takes four parameters. The four values specify the x and y-coordinates as (x<sub>1</sub>, y<sub>1</sub>, x<sub>2</sub>, y<sub>2</sub>) of the P<sub>1</sub> and P<sub>2</sub> points of the curve, respectively.

'''Note'''  For properties other than opacity and color, the cubic-bezier curve function accepts y-coordinates outside the standard range of [0, 1]. This allows the ability to specify "elastic" effects for properties such as length and width, as shown in the following image.
[[Image:msTransition-ease-in-out-elastic-cubic.png]]
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=The <code>animation-timing-function</code> property controls how the browser calculates intermediate values between each keyframe. It does not apply to the entire animation.

This property can be added to individual keyframes in the <code>@keyframes</code> rule, or to a style rule that applies an animation to an element. When specified in a style rule, this property sets the default timing function for each keyframe, but values specified for individual keyframes in an <code>@keyframes</code> rule take precedence. If no value is set, the default <code>ease</code> is applied.

In common with other animation properties, multiple values separated by commas are applied to animations in the same order as they are listed in <code>animation-name</code>. Excess values are ignored. If there are fewer values than animations, the browser the browser cycles through them again until each animation has been assigned a timing function.
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
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=4.0
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=5.0
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=12.0
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=3.1
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Yes
|Android_prefixed_version=2.1
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=Yes
|Blackberry_prefixed_version=7.0
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Yes
|Chrome_mobile_prefixed_version=18.0
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=16.0
|Firefox_mobile_prefixed_supported=Yes
|Firefox_mobile_prefixed_version=15.0
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=12.1
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=3.2
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=10.0
|Note=The -ms- prefix property is deprecated and should not be used.
}}
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