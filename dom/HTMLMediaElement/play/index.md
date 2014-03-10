{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Loads and starts playback of a media resource.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/HTMLMediaElement
|Example_object_name=object
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Play method example.
|Code=<!DOCTYPE html>
<html>
  <head>
    <title>Simple Video Example</title>
     <script>
         function hidecontrol(e) {
           // Set controls to true or false based on their current state
           var video = document.getElementById('video1');
           if (video.controls == true) {
             // Controls are binary, true if there, false if not
             video.removeAttribute("controls"); 
             e.innerHTML = "Show controls";
           } else {
             // Controls are binary, true if there, false if not
             video.setAttribute("controls", true); 
             e.innerHTML = "Hide controls";
           }
         }

         function playVideo(e) {
           var video = document.getElementById('video1');      //video element
           //  Toggle between play and pause based on the paused property
           if (video.paused) {
             var input = document.getElementById('videoFile');   //text box
             if (input.value) {
               //  Only load a video file when the text field changes
               if (input.value != video.src) {
                 video.src = input.value;
               }
               video.play();
               e.innerHTML = "Pause";
             }
           } else {
             video.pause();
             e.innerHTML = "Play";
           }
           
         }
     </script>
</head>
<body>
<video id="video1" controls >HTML5 video is not supported</video><br />
<input type="text" id="videoFile" size="60" placeholder="Enter video file URL here"/>
  <button onclick="playVideo(this);">Play</button>
  <button onclick="hidecontrol(this);">Hide controls</button>
</body>
</html>
}}
}}
{{Notes_Section
|Notes====Remarks===
To change the URL that is currently playing, assign it to [[dom/HTMLMediaElement/src|'''src''']]. This method sets [[dom/HTMLMediaElement/paused|'''paused''']] to false. To change the URL using the '''source''' element, or if the original video was specified by the '''source''' element, call [[dom/HTMLMediaElement/load|'''load''']] before calling '''play'''.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.9.8
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[html/elements/media|media]]</code>
*<code>audio</code>
*<code>audio</code>
*<code>video</code>
}}
{{Topics|API, Audio, DOM, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}