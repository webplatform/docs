{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The parameter's floating-point value. If a value is set outside the allowable range no exception is thrown, because these limits are nominal and may be exceeded. If a value is set during a time when there are any automation events scheduled then it will be ignored and no exception will be thrown.}}
{{API_Object_Property
|Property_applies_to=apis/webaudio/AudioParam
|Read_only=No
|Example_object_name=AudioParam
|Return_value_name=
|Javascript_data_type=Number
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var gainNode = audioCtx.createGain();
gainNode.gain.value = 0; //'gain' is the AudioParam
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
|Topic_clusters=Audio
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