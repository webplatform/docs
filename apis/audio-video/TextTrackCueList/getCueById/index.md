{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns the first text track cue object (in text track cue order) with text track cue identifier matching ''id''. Returns null if no cue has the given identifier or if the "id" argument is the empty string.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=idString
|Data type=Blob
|Description='''id''' for a specific [[apis/audio-video/TextTrackCue|'''TextTrackCue''']] .
|Optional=No
}}
|Method_applies_to=apis/audio-video/TextTrackCueList
|Example_object_name=TextTrackCueList
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=<nowiki>//. . .
var myTrack = document.getElementById("entrack").track; // get text track from track element
var myCues = myTrack.cues;   // get list of cues
// get a specific TextTrackCue by ID
var myCueObj = myCues.getCueById("CID3");
//. . .</nowiki>
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
|Name=W3C HTML5 Specification
|URL=http://dev.w3.org/html5/spec/single-page.html
|Status=W3C Editor's Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, Audio, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}