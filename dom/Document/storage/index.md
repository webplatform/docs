{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/objects/Event
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Topics|Event}}
{{Notes_Section
|Notes=
===Remarks===
The [[dom/properties/url|'''url''']] property of the event specifies the URL of the Web page that made the update.
For Windows Internet Explorer 9 standards mode, '''onstorage''' will only fire on window objects. Handlers attached to document.body or document objects will not receive the event. (Note this does not apply to the [[dom/events/storagecommit|'''onstoragecommit''']] event.)
The '''onstorage''' event will only fire on window objects. Handlers attached to document.body or document objects will not receive the event. (Note this does not apply to the [[dom/events/storagecommit|'''onstoragecommit''']] event.)
The '''onstorage''' event is specified in the W3C [http://go.microsoft.com/fwlink/?LinkId{{=}}217507 Web Storage] specification.
To invoke this event, do one of the following:
*Set or update a session or local storage value with [[apis/web-storage/methods/setItem|'''setItem''']].
*Remove a session or local storage value with [[apis/web-storage/methods/removeItem|'''removeItem''']].

|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML]


===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>frameSet</code>
*<code>window</code>
*<code>Introduction to Web Storage</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}