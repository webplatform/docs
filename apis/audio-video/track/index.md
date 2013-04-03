{{Page_Title}}
{{Flags
|High-level issues=Merge Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
|Editorial notes=Duplicate info of that in apis/audio-video/TextTrack
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object
|Subclass_of=dom/HTMLMediaElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The '''HTMLTrackElement''' represents a timed text file to provide users with multiple languages or commentary for videos. You can use multiple tracks, and set one as default to be used when the video starts.
The text is displayed in the lower portion of the video player. At this time the position and color can't be controlled, but you can retrieve text through script and display it in your own way. 
The user can choose alternate tracks, or turn tracks off through a built-in user interface or script.
Text tracks use a simplified version of the Web Video Text Track (WebVTT) or Timed Text Markup Language (TTML) timed text file formats.Internet Explorer 10 and Metro style apps using JavaScript currently support only timing cues and text captions.
'''Note'''  To create timed text files in both WebVTT and TTML formats, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251121 HTML5 Video Caption Maker] on the Windows Internet Explorer test drive site.

====WEBVTT====
WebVTT files are 8-bit Unicode Transformation Format (UTF-8) format text files that look like the following.
 <code>WEBVTT
 
 00:00:01.878 --&gt; 00:00:05.334
 Good day everyone, my name is John Smith
 
 00:00:08.608 --&gt; 00:00:15.296
 This video will teach you how to 
 build a sand castle on any beach
 </code>
The file starts with the tag "WEBVTT" as the first line, followed by a line feed. The timing cues are in the format "HH:MM:SS.sss". The start and end time cues are separated by a space, two hyphens and a greater-than sign ( --&gt; ), and another space. The timing cues are on a line by themselves followed by a line feed. Immediately following the cue is the caption text. Text captions can be one or more lines. The only restriction is that there must be no blank lines between lines of text. The MIME type is "text/vtt".

====TTML====
Internet Explorer 10 and Metro style apps using JavaScript use a subset of the TTML file format, which is defined in the TTML specification. Internet Explorer and Metro style apps using JavaScript support the following structure.
The TTML file includes XML version, encoding type,  namespace declaration, and the language in the root element ("&lt;tt&gt;"). This is followed by the" &lt;body&gt;" and a "&lt;div&gt;" element. Within the "&lt;div&gt;" element are the timing cues. The actual times are set as attributes  (begin, end) of the opening paragraph tag (&lt;p&gt;) and the text is delineated by the closing &lt;/p&gt; tag. Blank lines and white space are ignored. If there are multiple lines, they are defined by &lt;br/&gt; tags. 
The MIME type for TTML files is '''application/ttml+xml'''. See [http://go.microsoft.com/fwlink/p/?LinkId{{=}}234037 Section 5.2] of the TTML specification for more information.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML]


===Members===
The '''track''' object has these types of members:
*[#properties Properties]


====Properties====
The '''track''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/audio-video/properties/default|'''default''']]
|Gets or sets the default timed text track to use when multiple track elements are specified for a '''video''' element.
|-
|[[apis/audio-video/properties/kind|'''kind''']]
|Gets or sets the type or category of the timed text track associated with a '''track''' element.
|-
|[[apis/audio-video/properties/label|'''label''']]
|Gets or sets the label attribute to give a user a readable title for a text track.
|-
|[[apis/audio-video/properties/src|'''src''']]
|The address or URL of the a media resource ('''video''', '''audio''') that is to be considered.
|-
|[[apis/audio-video/properties/srclang|'''srclang''']]
|Gets or sets the language of the text track data. This attribute is required if "subtitles" is specified in the [[apis/audio-video/properties/kind|'''kind''']] attribute.
|}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}