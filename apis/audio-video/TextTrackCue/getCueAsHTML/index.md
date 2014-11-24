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
{{Summary_Section|Returns the text track cue text as a DocumentFragment of HTML elements and other DOM nodes.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/audio-video/TextTrackCue
|Example_object_name=TextTrackCue
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=DocumentFragment: A document fragment that represents the [[apis/audio-video/TextTrackCue|TextTrackCue]] text.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The HTML nodes replace the span element that is the first child of the div.
|Code=<script type="text/javascript">
    document.addEventListener("DOMContentLoaded", function () {  // don't run this until all DOM content is loaded 
      var track = document.getElementById("track1");
      track.addEventListener("cuechange", function () {
        var myTrack = this.track;             // track element is "this" 
        var myCues = myTrack.activeCues;      // activeCues is an array of current cues.                                                    
        if (myCues.length > 0) {
          var disp = document.getElementById("display");                  
          disp.replaceChild((myCues[0].getCueAsHTML()), disp.firstChild); 
        }
      }, false);
    }, false);      
    </script>
  </head>
  <body>
    <video id="video1" controls>
      <source src="video.mp4"  >
      <track id='track1' label='English captions' src="entrack.vtt" kind='subtitles' srclang='en' default >    
    </video>
    <div id="display">
      <span></span>
    </div>

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