{{Page_Title}}
{{Flags
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Adds the given cue to textTrack's text track list of cues.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=cue
|Data type=String
|Description="cue" is of type TextTrackCue.
|Optional=No
}}
|Method_applies_to=apis/audio-video/TextTrack
|Example_object_name=TextTrack
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=using addCue in javascript and setting several properties:
|Code=      myTextTrack = myPlayer.addTextTrack( 'subtitles','myLabel','en' );
var cue0 = new TextTrackCue(516.517,531.532, 'it had become much easier after the so called united resistance movement');
cue0.id = 'cue0';
cue0.pauseOnExit = false;
myTextTrack.addCue(cue0);

myTextTrack.mode = "showing";

}}{{Single Example
|Language=JavaScript
|Description=This addCue does NOT work, but should.  Several things go wrong.  First of all, it does not recognize the percent sign.  Secondly, the cue text is an html symbol, which is not interpreted as html.
|Code=
var cue1 = new TextTrackCue(3.300,13.130, '&8594;');
cue1.id = 'cue1';
myTextTrack.addCue(cue1);
cue1.line = '50%';
cue1.position = '25%';

}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML5 Specification
|URL=http://dev.w3.org/html5/spec/single-page.html
|Status=W3C Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Audio, DOM, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}