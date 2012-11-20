{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Start exponentially approaching the target value at the given time with a rate having the given time constant. Among other uses, this is useful for implementing the "decay" and "release" portions of an ADSR envelope. Please note that the parameter value does not immediately change to the target value at the given time, but instead gradually changes to the target value.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=target
|Data type=Number
|Description=The value the parameter will start changing to at the given time.
|Optional=No
}}{{Method Parameter
|Name=startTime
|Data type=Number
|Description=The time in the same time coordinate system as AudioContext.currentTime.
|Optional=No
}}{{Method Parameter
|Name=timeConstant
|Data type=Number
|Description=The time-constant value of first-order filter (exponential) approach to the target value. The larger this value is, the slower the transition will be.
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