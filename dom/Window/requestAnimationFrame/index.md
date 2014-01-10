{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections
|Content=Incomplete, Compatibility Incomplete
|Editorial notes=Not part of user_timing, resource_timing, or navigation_timing interfaces.
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|A method to invoke at the optimal time a callback to update the frame of an animation}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=callback
|Data type=function
|Description=The animation code to be run when the system is ready.
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=window
|Return_value_name=handle
|Javascript_data_type=Number
|Return_value_description=A handle or ID to the animationFrame request that can be used to cancel the request if needed.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Unlike older animation techniques based on [[dom/methods/setTimeout|'''setTimeout''']] and [[dom/methods/setInterval|'''setInterval''']] methods, '''requestAnimationFrame''' based animation occurs when the system is ready.  This leads to smoother animations and less power consumption than animations because '''requestAnimationFrame''' takes the visibility of the web application and the refresh rate of the display  into account,
The '''requestAnimationFrame''' method creates only a single animation request.  To create continous animation, a new request must be registered for each frame.
To cancel an animation request before the animation function is called back, use [[apis/timing/methods/cancelAnimationFrame|'''cancelAnimationFrame''']].
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Timing control for script-based animations
|URL=http://www.w3.org/TR/animation-timing/
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=24
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=21
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=14
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=6
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Animation
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}