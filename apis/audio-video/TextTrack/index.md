{{Page_Title|TextTracks}}
{{Flags
|High-level issues=Needs Review
|Content=Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|A media element can have a group of associated text tracks, known as the media element's "list of text tracks".}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=The track object contains the collection of [[apis/audio-video/TextTrackCue|TextTrackCues]] (times and text) that are contained in the file that the '''track''' element represents.

====WEBVTT====
'''TextTrackCues''' within a '''TextTrack''' can be defined within a '''[http://dev.w3.org/html5/webvtt/#dfnReturnLink-1 WebVTT]''' file which is defined as an 8-bit Unicode Transformation Format (UTF-8) format text files that look like the following.
 <code>WEBVTT
 
 00:00:01.878 --&gt; 00:00:05.334
 Good day everyone, my name is John Smith
 
 00:00:08.608 --&gt; 00:00:15.296
 This video will teach you how to 
 build a sand castle on any beach
 </code>
The file starts with the tag "WEBVTT" as the first line, followed by a line feed. The timing cues are in the format "HH:MM:SS.sss". The start and end time cues are separated by a space, two hyphens and a greater-than sign ( --&gt; ), and another space. The timing cues are on a line by themselves followed by a line feed. Immediately following the cue is the caption text. Text captions can be one or more lines. The only restriction is that there must be no blank lines between lines of text. The MIME type is "text/vtt".

}}
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
{{Topics|API, Audio, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}