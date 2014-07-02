{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs example
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
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Web Audio API
|URL=https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html
|Status=W3C Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|API, WebAudio}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}