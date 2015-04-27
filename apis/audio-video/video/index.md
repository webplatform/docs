{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs example, spec reference, standardization status
|Checked_Out=No
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|HTML Video element allows creator of a HTML document or view of a Web Application to embed a video for display when a user visits the view or opens HTML document in a web browser.}}
{{API_Object
|Subclass_of=dom/HTMLMediaElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Beginning with Internet Explorer 9, any audio or video content needs  the correct mime type set on the server, or the files won't play. Internet Explorer 9 supports MP3 audio, and  MP4 audio and video. WebM audio and video files can be supported by installing the WebM components from [http://go.microsoft.com/fwlink/p/?LinkID{{=}}218894 The WebM project]. The following table shows the required settings for your web server to host these files correctly.
{{{!}} class="wikitable"
{{!}}-
!Media file to serve
!Extension setting
!Mime type setting
{{!}}-
{{!}}Audio mp3
{{!}}mp3
{{!}}audio/mpeg
{{!}}-
{{!}}Audio mp4
{{!}}m4a
{{!}}audio/mp4
{{!}}-
{{!}}Audio WebM
{{!}}webm
{{!}}audio/webm
{{!}}-
{{!}}Video mp4
{{!}}mp4
{{!}}video/mp4
{{!}}-
{{!}}Video webm
{{!}}webm
{{!}}video/webm
{{!}}}
 
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.6
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>HTMLVideoElement</code>
}}
{{Topics|API, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}