{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=callback|Data type=Function|Description=The animation code to be run when the system is ready.|Optional=}}
{{Method Parameter|Name=handle|Data type=Integer|Description=A handle or ID to the animationFrame request that can be used to cancel the request if needed.|Optional=}}
|Method_applies_to=dom/window
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=This method does not return a value.

'''Integer'''

A handle or ID to the animationFrame request that can be used to cancel the request if needed.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
Unlike older animation techniques based on [[dom/methods/setTimeout|'''setTimeout''']] and [[dom/methods/setInterval|'''setInterval''']] methods, '''requestAnimationFrame''' based animation occurs when the system is ready.  This leads to smoother animations and less power consumption than animations because '''requestAnimationFrame''' takes the visibility of the web application and the refresh rate of the display  into account,
The '''requestAnimationFrame''' method creates only a single animation request.  To create continous animation, a new request must be registered for each frame.
To cancel an animation request before the animation function is called back, use [[apis/timing/methods/cancelAnimationFrame|'''cancelAnimationFrame''']].
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}229562 Timing control for script-based animations]


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/window|window]]</code>
*<code>[http://go.microsoft.com/fwlink/p/?LinkID{{=}}258428 requestAnimationFrame API demo]</code>
*<code>[[apis/timing/methods/cancelAnimationFrame|cancelAnimationFrame]]</code>
*<code>[[apis/timing/properties/animationStartTime|animationStartTime]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}