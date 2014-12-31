{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Given the current filter parameter settings, calculates the frequency response for the specified frequencies.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=frequencyHz
|Data type=void
|Description=Specifies an array of frequencies at which the response values will be calculated.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=magResponse
|Data type=void
|Description=Specifies an output array receiving the linear magnitude response values.
|Optional=No
}}{{Method Parameter
|Index=2
|Name=phaseResponse
|Data type=void
|Description=Specifies an output array receiving the phase response values in radians.
|Optional=No
}}
|Method_applies_to=apis/webaudio/BiquadFilterNode
|Example_object_name=BiquadFilterNode
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var audioCtx = new AudioContext();
var biquadFilter = audioCtx.createBiquadFilter();
biquadfilter.getFrequencyResponse(myFrequencyArray,magResponseOutput,phaseResponseOutput);
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