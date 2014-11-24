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
{{Summary_Section|Removes the given cue from textTrack's text track list of cues.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=cue
|Data type=String
|Description="cue" is of type TextTrackCue.
|Optional=No
}}
|Method_applies_to=apis/audio-video/TextTrack
|Example_object_name=TextTrack
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=
|Code=<nowiki><!DOCTYPE html >
<html >
  <head>
    <title>Remove Cue example</title>
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
</head>
<body>

<video id="video1" controls muted autoplay>
    <source src="video.mp4">
    HTML5 Video not supported 
</video>

 <script type="text/javascript">
    var video = document.getElementById("video1");
    var beginTime, endTime, message; 
    var newTextTrack = video.addTextTrack("captions", "sample");
    newTextTrack.mode = newTextTrack.SHOWING; // set track to display
    // create some cues and add them to the new track 
    for(var i=0;i<10;i++){
        beginTime =  i * 5 ;
        endTime = ( (i * 5) +  5);
        message =  "This is number " + i; 
        newTextTrack.addCue(new TextTrackCue(beginTime, endTime, message));
    }
    //  Watch for cue change events
    newTextTrack.addEventListener("cuechange", function () {
            // get current cue, and remove it if it's number 2
            var currentCue = newTextTrack.activeCues[0];             
            if (currentCue.text == "This is number 2") {
                newTextTrack.removeCue(currentCue)
            }            
        },false);
     
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