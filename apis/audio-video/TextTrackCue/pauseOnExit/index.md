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
{{Summary_Section|Returns the pause-on-exit flag on a TextTrackCue. When the flag is true, playback will pause when it reaches the cue's endTime.}}
{{API_Object_Property
|Property_applies_to=apis/audio-video/TextTrackCue
|Read_only=Yes
|Example_object_name=TextTrackCue
|Return_value_name=
|Javascript_data_type=Boolean
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example displays the cue (caption), startTime, endTime, pauseOnExit, and id for all cues in a track.
|Code=<nowiki>  <head>
    <script type="text/javascript">
      function getCues() {
        var myTrack = document.getElementById("entrack").track; // get text track from track element          
        var myCues = myTrack.cues;   // get list of cues                              
        var statusFlags = "<table><tr><th>startTime</th><th>endTime</th>";
        statusFlags += "<th>pauseOnExit</th><th>id</th>";
        statusFlags += "<th>cue text</th></tr>";

        for (var i = 0; i < myCues.length; i++) {
          statusFlags += "<tr><td>" + myCues[i].startTime + "</td><td>" + myCues[i].endTime + "</td>";
          statusFlags += "</td><td>" + +myCues[i].pauseOnExit + "</td><td>\"" + myCues[i].id + "\"</td>";
          statusFlags += "</td><td>" + myCues[i].getCueAsHTML().textContent + "</td></tr>";
          }
          statusFlags += "</table>";
          document.getElementById("display").innerHTML = statusFlags;  //append track label
        }
    </script>
  </head>
  <body>
    <video id="video1" controls  >
      <source src="video.mp4">    
      <track id="entrack" label="English subtitles" kind="captions" src="entrack.vtt" srclang="en" default>
    </video>
    <p><button onclick="getCues();">Show tracks</button></p>
    <div style="display:block; overflow:auto; height:200px; width:auto"  id="display"></div>
</body></nowiki>
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