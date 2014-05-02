{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Provides specific contextual information associated with animation events.}}
{{API_Object
|Subclass_of=dom/Event
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=AnimationEvent objects provide information about events that occur related to Cascading Style Sheets (CSS) animations. Several animation related events are available. For example, the start and end of an animation, and the end of each iteration of an animation all generate Document Object Model (DOM) events. An element can have multiple properties being animated simultaneously. This can occur either with a single [[dom/AnimationEvent/animationName|'''animationName''']] value with keyframes containing multiple properties, or with multiple '''animationName''' values. For the purposes of events, each '''animationName''' specifies a single animation. Therefore an event will be generated for each '''animationName''' value and not necessarily for each property being animated. 

The time the animation has been running is sent with each event generated. This allows the event handler to determine the current iteration of a looping animation or the current position of an alternating animation. This time does not include any time the animation was in the paused play state.

The different types of animation events that can occur are:

'''animationstart''' - The animationstart event occurs at the start of the animation. If there is an animation-delay then this event will fire once the delay period has expired. A negative delay will cause the event to fire with an elapsedTime equal to the absolute value of the delay.
*Bubbles: Yes
*Cancelable: No
*Context Info: animationName, pseudoElement

'''animationend''' - The animationend event occurs when the animation finishes.
*Bubbles: Yes
*Cancelable: No
*Context Info: animationName, elapsedTime, pseudoElement

'''animationiteration''' - The animationiteration event occurs at the end of each iteration of an animation, except when an animationend event would fire at the same time. This means that this event does not occur for animations with an iteration count of one or less.
*Bubbles: Yes
*Cancelable: No
*Context Info: animationName, elapsedTime, pseudoElement
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}