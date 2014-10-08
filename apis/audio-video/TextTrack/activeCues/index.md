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
{{Summary_Section|Returns the text track cues from the text track list of cues that are currently active (i.e. that start before the current playback position and end after it), as a TextTrackCueList object.}}
{{API_Object_Property
|Property_applies_to=apis/audio-video/TextTrack
|Read_only=Yes
|Example_object_name=TextTrack
|Return_value_name=
|Javascript_data_type=DOM Node
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=
|Code=&lt;!DOCTYPE html>
&lt;html xmlns="http://www.w3.org/1999/xhtml">
&lt;head>
    &lt;title>activeCues example&lt;/title>

    &lt;script type="text/javascript">
        // don't add this listener until all DOM content is loaded
        document.addEventListener("DOMContentLoaded", function () {
            var track = document.getElementById("track1");
            track.addEventListener("cuechange", function () {
                var myTrack = this.track;
                var myCues = myTrack.activeCues;      // array of current cues.
                //  display the start and end time, and cue text
                if (myCues.length > 0) {
                    var disp = document.getElementById("display");
                    disp.innerHTML = myCues[0].startTime + " --> " + myCues[0].endTime + "  " + myCues[0].getCueAsHTML().textContent;
                }
            }, false);
        }, false);
    &lt;/script>
&lt;/head>
&lt;body>
    &lt;video id="video1" controls>
        &lt;source src="video.mp4">
        &lt;track id="track1" label="English subtitles" kind="captions" src="entrack.vtt" srclang="en" default>
        HTML5 video is not supported
    &lt;/video>
    &lt;div id="display">&lt;/div>
&lt;/body>
&lt;</html>
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