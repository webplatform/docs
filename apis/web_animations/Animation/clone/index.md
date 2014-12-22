{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Creates a copy of an Animation object.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/web animations/Animation
|Example_object_name=myAnimation
|Return_value_name=myMiniMe
|Javascript_data_type=
|Return_value_description=Return a new Animation object created by calling the Animation constructor with parameters Animation(source.target, cloned effect, cloned timing).
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example creates an instance of the AnimationPlayer that animates an object horizontally and vertically using computed values, and runs for 1500ms (1.5 seconds), and then creates a copy of the player for later use.
|Code=var player = snowFlake.animate([
  {transform: 'translate(' + snowLeft + 'px, -100%)'},
  {transform: 'translate(' + snowLeft + 'px, ' + window.innerHeight + 'px)'}
], 1500);
var player2 = player.clone();

|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Web Animations 1.0
|URL=http://www.w3.org/TR/web-animations/
|Status=W3C Working Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|Web Animations}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://updates.html5rocks.com/2014/05/Web-Animations---element-animate-is-now-in-Chrome-36
}}