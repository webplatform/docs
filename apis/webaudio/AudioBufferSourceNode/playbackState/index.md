{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The playback state, initialized to UNSCHEDULED_STATE, progressing through SCHEDULED_STATE, PLAYING_STATE, and FINISHED_STATE.}}
{{API_Object_Property
|Property_applies_to=apis/webaudio/AudioBufferSourceNode
|Read_only=Yes
|Example_object_name=AudioBufferSourceNode
|Javascript_data_type=unsigned short
|Return_value_description=Returns one of the following constant values: UNSCHEDULED_STATE (0), SCHEDULED_STATE (1), PLAYING_STATE (2), or FINISHED_STATE (3).
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=// 1. Create an AudioBufferSourceNode and load data into it
var soundSource = …

// 2. Check to see if the sound has finished playing, once per second
var timer = setInterval(function() {
  if (soundSource.playbackState == soundSource.FINISHED_STATE) {
    console.log("The sound has finished playing.");
    clearInterval(timer);
  }
}, 1000);

// 3. Play the sound
soundSource.start(…);
}}
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