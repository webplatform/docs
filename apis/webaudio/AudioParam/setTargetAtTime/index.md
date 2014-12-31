{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Start exponentially approaching the target value at the given time with a rate having the given time constant. Among other uses, this is useful for implementing the ''decay'' and ''release'' portions of an ADSR envelope. Please note that the parameter value does not immediately change to the target value at the given time, but instead gradually changes to the target value.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=target
|Data type=Number
|Description=The value the parameter will start changing to at the given time.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=startTime
|Data type=Number
|Description=The time in the same time coordinate system as [[apis/webaudio/AudioContext/currentTime|'''AudioContext.currentTime''']].
|Optional=No
}}{{Method Parameter
|Index=2
|Name=timeConstant
|Data type=Number
|Description=The time-constant value of first-order filter (exponential) approach to the target value. The larger this value is, the slower the transition will be.
|Optional=No
}}
|Method_applies_to=apis/webaudio/AudioParam
|Example_object_name=AudioParam
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var gainNode = audioCtx.createGain();
gainNode.gain.setTargetAtTime(1.0, audioCtx.currentTime + 1, 0.5); //'gain' is the AudioParam
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
|Name=W3C Web Audio API
|URL=http://webaudio.github.io/web-audio-api/
|Status=W3C Editor's Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, WebAudio}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}