{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=dom/objects/Event
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
The [[apis/audio-video/events/addtrack|'''onaddtrack''']] event listener must be added to the '''video''' object before the video source content is loaded.
The following example uses the '''TrackEvent''' object and the [[apis/audio-video/properties/track|'''track''']] property to get the language of each audio track in a multi-track video file. Note that the video [[apis/audio-video/properties/src|'''src''']] property is set (content is loaded) after the [[apis/audio-video/events/addtrack|'''onaddtrack''']] event has been specified.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML]


===Members===
The '''TrackEvent''' object has these types of members:
*[#properties Properties]


====Properties====
The '''TrackEvent''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/audio-video/properties/track|'''track''']]
|Returns the track that is loaded by the [[apis/audio-video/events/addtrack|'''onaddtrack''']] event.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}