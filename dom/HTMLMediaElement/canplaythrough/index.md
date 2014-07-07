{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary, examples, clean-up of MSDN import
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Fires when enough data is available to determine whether a media is playable at a normal rate without interruptions.}}
{{Event
|Event_applies_to=dom/HTMLMediaElement
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Interface=dom/HTMLMediaElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=The '''oncanplaythrough''' event is raised when data is being fetched at a rate that would allow playback without interruption at the [[dom/HTMLMediaElement/defaultPlaybackRate|'''defaultPlaybackRate''']]. If the [[dom/HTMLMediaElement/autoplay|'''autoplay''']] attribute is specified, the video starts playing when '''oncanplaythrough''' is received.
This event occurs after [[dom/HTMLMediaElement/canplay|'''oncanplay''']] and before the first [[dom/HTMLMediaElement/progress|'''onprogress''']] event is received.
To invoke this event, load a media resource.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.9.12


===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage
|Status=Living Standard
|Relevant_changes=Section 4.8.9.12
}}{{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html5/
|Status=Working Draft
|Relevant_changes=Section 4.8.9.12
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
{{Topics|API, Audio, DOM, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}