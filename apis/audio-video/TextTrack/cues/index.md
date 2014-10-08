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
{{Summary_Section|Returns the text track list of cues, as a TextTrackCueList object.}}
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
|Code=&lt;!DOCTYPE HTML>
&lt;html>
&lt;head>
    &lt;title>Get track example&lt;/title>
&lt;/head>
&lt;body>
    &lt;h1>Get track example&lt;/h1>
    &lt;video id="video1" controls>
        &lt;source src="http://ie.microsoft.com/testdrive/Videos/BehindIE9ModernWebStandards/Video.mp4">
        &lt;track id="entrack" label="English subtitles" kind="captions" src="entrack.vtt" srclang="en" default>
    &lt;/video>
    &lt;p>
        &lt;button id="mybutton">Show tracks&lt;/button>
    &lt;/p>
    &lt;div style="display:block; overflow:auto; height:200px; width:650px;" id="display">&lt;/div>

    &lt;script>
      document.getElementById("mybutton").addEventListener("click", function () {
        var myTrack = document.getElementById("entrack").track; // get text track from track element
        var myCues = myTrack.cues;   // get list of cues
        for (var i = 0; i &lt; myCues.length; i++) {
        // append track label
        document.getElementById("display").innerHTML += (myCues[i].getCueAsHTML().textContent + "&lt;br/>");
        }
     }, false);
    &lt;/script>
&lt;/body>
&lt;/html>
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