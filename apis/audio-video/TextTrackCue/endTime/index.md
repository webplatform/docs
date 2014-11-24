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
{{Summary_Section|The text track cue end time, in seconds.}}
{{API_Object_Property
|Property_applies_to=apis/audio-video/TextTrackCue
|Read_only=No
|Example_object_name=TextTrackCue
|Return_value_name=
|Javascript_data_type=Number
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example add start times, end times, and captions to a track. 
|Code=<nowiki><!DOCTYPE html >

<html >
  <head>
    <title>Add Text Tracks example</title>
</head>
<body>

<video id="video1" controls="controls" muted="muted">
     <!-- change to your own mp4 video file -->
  <source src="http://ie.microsoft.com/testdrive/Videos/BehindIE9ModernWebStandards/Video.mp4" />   
  HTML5 Video not supported 
</video>

 <script>
   var video = document.getElementById("video1");
   var startTime, endTime, message;
   var newTextTrack = video.addTextTrack("captions", "sample");
   newTextTrack.mode = newTextTrack.SHOWING; // set track to display
   // create some cues and add them to the new track 
   for (var i = 0; i < 30; i++) {
     startTime = i * 5;
     endTime = ((i * 5) + 5);
     message = "This is number " + i;
     newTextTrack.addCue(new TextTrackCue(startTime, endTime, message));
   }
   video.play();
  </script>
</body>
</html></nowiki>
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
{{Topics}}
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