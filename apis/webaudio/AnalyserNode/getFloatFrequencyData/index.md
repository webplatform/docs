{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Copies the current frequency data into the passed floating-point array. If the array has fewer elements than the [[apis/webaudio/AnalyserNode/frequencyBinCount|'''frequencyBinCount''']], the excess elements will be dropped.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=array
|Data type=void
|Description=Where frequency-domain analysis data will be copied.
|Optional=No
}}
|Method_applies_to=apis/webaudio/AnalyserNode
|Example_object_name=AnalyserNode
|Return_value_name=
|Javascript_data_type=
|Return_value_description=Float32Array
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var audioCtx = new AudioContext();
var analyser = audioCtx.createAnalyser();
// Float32Array should be the same length as the frequencyBinCount 
var myDataArray = new Float32Array(analyser.frequencyBinCount); 
// fill the Float32Array with data returned from getFloatFrequencyData()
analyser.getFloatFrequencyData(myDataArray); 

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
|Name=Web Audio API
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