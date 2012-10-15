{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Cleanup, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The transition CSS property is a shorthand property for [[css/properties/transition-property|transition-property]], [[css/properties/transition-duration|transition-duration]], [[css/properties/transition-timing-function|transition-timing-function]], and [[css/properties/transition-delay|transition-delay]]. It allows to define the transition between two states of an element.}}
{{CSS Property
|Initial value=see individual properties
|Applies to=all elements, :before and :after pseudo elements
|Inherited=No
|Media=interactive
|Animatable=No
|Values={{CSS Property Value
|Data Type=transition-property
|Description=Value of the [[css/properties/transition-property|'''transition-property''']] property.
}}{{CSS Property Value
|Data Type=transition-duration
|Description=Value of the [[css/properties/animation-duration|'''transition-duration''']] property.
}}{{CSS Property Value
|Data Type=transition-timing-function
|Description=Value of the [[css/properties/animation-timing-function|'''transition-timing-function''']] property.
}}{{CSS Property Value
|Data Type=transition-delay
|Description=Value of the [[css/properties/animation-delay|'''transition-delay''']] property.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=When you hover on the div height property will gradually change from 100 to 500
|Code=div
{
height:100px;
transition: height 2s;
-moz-transition: height 2s; /* Firefox */
-webkit-transition: height 2s; /* Safari and Chrome */
-o-transition: height 2s; /* Opera */
}

div:hover {height:500px;}
}}
}}
{{Notes_Section
|Notes====Remarks===
Some browsers have started to remove the prefix from these properties, including Internet Explorer 10.

To ensure compatibility in the future, applications using this property with a vendor prefix should be updated accordingly.
|Import_Notes====Syntax===
<code>'''transition: ''''''[''' ''transition-property'' '''{{!}}{{!}}''' ''transition-duration'' '''{{!}}{{!}}''' ''transition-timing-function'' '''{{!}}{{!}}''' ''transition-delay'' ''']''' '''[''' ,  '''[''' ''transition-property'' '''{{!}}{{!}}''' ''transition-duration'' '''{{!}}{{!}}''' ''transition-timing-function'' '''{{!}}{{!}}''' ''transition-delay'' ''']''' ''']''' *</code>
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=1
|Firefox_supported=Yes
|Firefox_version=16
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=4
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=11.6
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=3
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Yes
|Android_prefixed_version=2
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=16
|Firefox_mobile_prefixed_supported=Yes
|Firefox_mobile_prefixed_version=4
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=12.10
|Opera_mobile_prefixed_supported=Yes
|Opera_mobile_prefixed_version=10
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=3.2
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Transistions, Animation
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
{{Topics|Vendor Prefix, CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/transition
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}