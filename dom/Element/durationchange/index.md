{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, compat, better spec link
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Default_action=
|Content=
|Interface=dom/Element
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=The following example reads the total duration when the video is loaded and updates the current playback position as the video plays.
|Code=function timeUpdate()
{
    document.getElementById('time').innerHTML {{=}} v1.currentTime;
}
function durationChange()
{
    document.getElementById('duration').innerHTML {{=}} v1.duration;
}
&lt;video id{{=}}"v1" controls{{=}}"true" autoplay{{=}}"1" src{{=}}"video.aac"
    ontimeupdate{{=}}"timeUpdate()" ondurationchange{{=}}"durationChange()"/&gt;
&lt;div&gt;Time: &lt;span id{{=}}"time"&gt;0&lt;/span&gt; of &lt;span id{{=}}"duration"&gt;0&lt;/span&gt; seconds.&lt;/div&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
Use the [[dom/HTMLMediaElement/duration|'''duration''']] property to determine the new duration of the clip.
This event occurs immediately after [[dom/Element/loadstart|'''loadstart''']] and before [[dom/Element/loadedmetadata|'''loadedmetadata''']].
To invoke this event, do one of the following:
*Load a media resource.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.9.12


===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>
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
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[html/elements/audio|audioElement]]</code>
*<code>[[apis/audio-video/audio|audioApi]]</code>
*<code>[[dom/Document|Document]]</code>
*<code>[[html/elements/source|source]]</code>
*<code>[[html/elements/video|videoElement]]</code>
*<code>[[apis/audio-video/video|videoApi]]</code>
*<code>[[dom/Window|Window]]</code>
*<code>Reference</code>
*<code>[[dom/Element/loadedmetadata|loadedmetadata]]</code>
*<code>[[dom/Element/timeupdate|timeupdate]]</code>
}}
{{Topics|API, Audio, DOM, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}