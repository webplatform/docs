{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Controls whether an animation is running or paused}}
{{CSS Property
|Initial value=running
|Applies to=all elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=running
|Description=Default. 
Play the animation.
If restarting a paused animation, the animation resumes from the current (paused) property value.
}}{{CSS Property Value
|Data Type=paused
|Description=Pause the animation. The object is displayed with the current property value until '''animation-play-state''' is set to '''running''' and the animation resumes.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The CSS uses the Animation property and the @keyframes property as well as the animation-play-state propery and more.

The example show how to create a counter like function.
By using the ":checked" selector for radio buttons we toggle the animation states for the counter
|Code=/* position the handles */
#stopwatch_handles {
	margin-top: 0px;
}
/* Style the labels itself, at the bottom we hide the radio buttons itself */
#stopwatch_handles label {
	cursor: pointer;
	padding: 5px 5px;
	font-family: Verdana, sans-serif;
	font-size: 12px;
}
input[name="handles"] {display: none;}

/*Actual handles  this triggers the stopwatch to start and stop based on the state of the radio buttons */
#stopbtn:checked~.stopwatch .numbers {animation-play-state: paused;-webkit-animation-play-state: paused;-moz-animation-play-state: paused;-o-animation-play-state: paused;}
#startbtn:checked~.stopwatch .numbers {animation-play-state: running;-webkit-animation-play-state: running;-moz-animation-play-state: running;-o-animation-play-state: running;}

/* we set the animation in 10 steps of 1 second, and set the play state to paused by default */
.moveten {
	animation: moveten 1s steps(10, end) infinite;
	-webkit-animation: moveten 1s steps(10, end) infinite;
	-moz-animation: moveten 1s steps(10, end) infinite;
	-o-animation: moveten 1s steps(10, end) infinite;
	animation-play-state: paused;
	-webkit-animation-play-state: paused;
	-moz-animation-play-state: paused;
	-o-animation-play-state: paused;
}
/* here we do the same except for six */
.movesix {
	animation: movesix 1s steps(6, end) infinite;
	-webkit-animation: movesix 1s steps(6, end) infinite;
	-moz-animation: movesix 1s steps(6, end) infinite;
	-o-animation: movesix 1s steps(6, end) infinite;
	animation-play-state: paused;
	-webkit-animation-play-state: paused;
	-moz-animation-play-state: paused;
	-o-animation-play-state: paused;
}

/* here we actualy set the duration of the seconds so that they sync up when needed */
.second {animation-duration: 10s;-webkit-animation-duration: 10s;-moz-animation-duration: 10s;-o-animation-duration: 10s;}
.tensecond {animation-duration: 60s;-webkit-animation-duration: 60s;-moz-animation-duration: 60s;-o-animation-duration: 60s;} 

/* and here are the keyframes so that the numbers animate vertically
The height is 30 and the there are 10 digits so to move up we use -300px (30x10) */
@keyframes moveten {
	0% {top: 0;}
	100% {top: -300px;} 
}
@-webkit-keyframes moveten {
	0% {top: 0;}
	100% {top: -300px;} 
}
@-moz-keyframes moveten {
	0% {top: 0;}
	100% {top: -300px;} 
}
@-o-keyframes moveten {
	0% {top: 0;}
	100% {top: -300px;} 
}
/* The same goes for this one but instead of ten we have 6 so we get 30x6 = 180px */
@keyframes movesix {
	0% {top: 0;}
	100% {top: -180px;} 
}
@-webkit-keyframes movesix {
	0% {top: 0;}
	100% {top: -180px;} 
}
@-moz-keyframes movesix {
	0% {top: 0;}
	100% {top: -180px;} 
}
@-o-keyframes movesix {
	0% {top: 0;}
	100% {top: -180px;} 
}
}}
}}
{{Notes_Section
|Usage=When set to <code>paused</code>, the animation is frozen in its current state. Changing the value back to <code>running</code> resumes the animation from the point at which it was paused.

In common with other animation properties, multiple values separated by commas are applied to animations in the same order as they are listed in <code>animation-name</code>. Excess values are ignored. If there are fewer values than animations, the browser the browser cycles through them again until each animation has been assigned a play state.
|Import_Notes====Syntax===
<code>'''animation-play-state: '''running '''{{!}}''' paused '''[''' ,  running '''{{!}}''' paused ''']''' *</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223144 CSS Animations Module Level 3], Section 3.7
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
|Firefox_mobile_supported=No
|Firefox_mobile_version=
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