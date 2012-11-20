{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Sets an array of arbitrary parameter values starting at the given time for the given duration. The number of values will be scaled to fit into the desired duration.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=values
|Data type=String
|Description=A Float32Array representing a parameter value curve. These values will apply starting at the given time and lasting for the given duration.
|Optional=No
}}{{Method Parameter
|Name=startTime
|Data type=Number
|Description=The time in the same time coordinate system as AudioContext.currentTime.
|Optional=No
}}{{Method Parameter
|Name=duration
|Data type=Number
|Description=The amount of time in seconds (after the time parameter) where values will be calculated according to the values parameter.
|Optional=No
}}
|Method_applies_to=apis/webaudio/AudioParam
|Example_object_name=AudioParam
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Audio}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}