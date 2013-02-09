{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The shaping curve used for the waveshaping effect. The input signal is nominally within the range -1 -> +1. Each input sample within this range will index into the shaping curve with a signal level of zero corresponding to the center value of the curve array. Any sample value less than -1 will correspond to the first value in the curve array. Any sample value less greater than +1 will correspond to the last value in the curve array.}}
{{API_Object_Property
|Property_applies_to=apis/webaudio/WaveShaperNode
|Read_only=No
|Example_object_name=WaveShaperNode
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
{{Topics|Audio}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}