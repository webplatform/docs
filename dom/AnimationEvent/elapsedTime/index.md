{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The amount of time the animation has been running, in seconds, since the event fired, excluding any time the animation was paused.}}
{{API_Object_Property
|Property_applies_to=dom/AnimationEvent
|Read_only=Yes
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//for a predefined animation event that is running
var myAnimEvent = new AnimationEvent();
// . . .
//retrieve the elapased time
var myAnimTime = myAnimEvent.elapsedTime;
}}
}}
{{Notes_Section
|Notes=For an '''animationstart''' event, the elapsedTime is zero (0.0) unless there was a negative value for ''animation-delay'', in which case the event will be fired with an elapsedTime of ''(-1 * delay)''.
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