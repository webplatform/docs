{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs example, child references
|Checked_Out=Yes
|High-level issues=Deletion Candidate, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The audio object is part of the HTML5 audio api. It extends the <audio> tag and allows users to access audio data. This enables the ability to manipulate or create new audio data.}}
{{API_Object
|Subclass_of=dom/HTMLAudioElement
|Overview=
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=Beginning with Internet Explorer 9, any audio or video content needs  the correct mime type set on the server, or the files won't play. Internet Explorer 9 and  Internet Explorer 10 support MP3 audio, and  MP4 audio and video. WebM audio and video files can be supported by installing the WebM components from [http://go.microsoft.com/fwlink/p/?LinkID{{=}}218894 The WebM project]. The following table shows the required settings for your web server to host these files correctly.
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
 
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=A vocabulary and associated APIs for HTML and XHTML
|URL=http://www.w3.org/TR/html5/embedded-content-0.html#the-audio-element
|Status=
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, Audio}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic Support
|Chrome_supported=Yes
|Chrome_version=3.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.5
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.3
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=4.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}



{{Editorial/Deletion_Candidate|MS proprietary}}