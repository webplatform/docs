{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Creates a new Animation object whose animation target is the object on which the method is called, and calls the play method of the AnimationTimeline object of the document timeline of the node document [DOM4] of the element, passing the newly created Animation as the argument to the method.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/web_animations/Animatable
|Example_object_name=myAnimationPlayer
|Return_value_name=myAnimationPlayer
|Javascript_data_type=
|Return_value_description=Returns the AnimationPlayer object returned by the play method of the AnimationTimeline.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example creates an instance of the AnimationPlayer that animates an object horizontally and vertically using computed values, and runs for 1500ms (1.5 seconds).
|Code=var player = snowFlake.animate([
  {transform: 'translate(' + snowLeft + 'px, -100%)'},
  {transform: 'translate(' + snowLeft + 'px, ' + window.innerHeight + 'px)'}
], 1500);
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