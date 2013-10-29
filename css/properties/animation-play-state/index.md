{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Defines whether an animation is running or paused.}}
{{CSS Property
|Initial value=running
|Applies to=All elements, &#58;&#58;before and &#58;&#58;after pseudo-elements.
|Inherited=No
|Media=visual
|Computed value=As specified.
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=running
|Description=Plays the animation. If restarting a paused animation, the animation resumes from the current (paused) state.
}}{{CSS Property Value
|Data Type=paused
|Description=Pauses the animation. A paused animation continues to display the current state of the animation.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The CSS uses the animation property and the @keyframes property as well as the animation-play-state property and more. 

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
}}{{Single Example
|Language=CSS
|Description=A mobile-like interface featuring a keyframe-animated pulsing icon.  When the application enters an interruption mode, the icon is paused and the page presents another panel to indicate that the animation is inactive.
|Code=div.selected {
    animation: pulse 0.5s infinite alternate running;
}

body.interrupt div.selected {
    animation-play-state: paused;
}

@keyframes pulse {
    from {
        transform : scale(1) translateX(0);
        opacity : 1;
    }
    to {
        transform : scale(0.75) translateX(0);
        opacity : 0.25;
    }
}
|LiveURL=http://code.webplatform.org/gist/7044978
}}
}}
{{Notes_Section
|Usage=Can also be a comma-separated list of play states, e.g., '''running, paused, running''', where each play state is applied to the corresponding ordinal position value of the [[css/properties/animation-name|animation-name]] property.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Animation
|URL=http://www.w3.org/TR/css3-animations/
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=10.0
|Note=The -ms- prefix property is deprecated and should not be used.
}}
}}
{{See_Also_Section
|Topic_clusters=Animation
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}