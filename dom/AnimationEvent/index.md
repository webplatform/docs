{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=dom/Event
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
AnimationEvent objects provide information about events that occur related to Cascading Style Sheets (CSS) animations. Several animation related events are available. For example, the start and end of an animation, and the end of each iteration of an animation all generate Document Object Model (DOM) events. An element can have multiple properties being animated simultaneously. This can occur either with a single [[dom/properties/animationName|'''animationName''']] value with keyframes containing multiple properties, or with multiple '''animationName''' values. For the purposes of events, each '''animationName''' specifies a single animation. Therefore an event will be generated for each '''animationName''' value and not necessarily for each property being animated. 

The time the animation has been running is sent with each event generated. This allows the event handler to determine the current iteration of a looping animation or the current position of an alternating animation. This time does not include any time the animation was in the paused play state.
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_dom_events\ie]:%20AnimationEvent object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
|Import_Notes=
===Members===
The '''AnimationEvent''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''AnimationEvent''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/initAnimationEvent|'''initauthor{{=}}"jaymunro" time{{=}}"20120418T100841-0800" data{{=}}"MS"AnimationEvent''']]
|Initializes the values of an animation event.
|}
 

====Properties====
The '''AnimationEvent''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/animationName|'''animationName''']]
|The name of a [[css/atrules/@keyframes|'''keyframe''']] rule that defines the style rules applied by the animation.
|-
|[[dom/properties/elapsedTime (AnimationEvent)|'''elapsedTime''']]
|The amount of time the animation has been running, in seconds.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}