{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/Document
|Interface=dom/Document
|Target=dom/Element
|Default_action=
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The [[dom/Window/url|'''url''']] property specifies the URL of the Web page that made the update.
For Windows Internet Explorer 9 standards mode, '''onstorage''' will only fire on window objects. Handlers attached to document.body or document objects will not receive the event. (Note this does not apply to the [[dom/Document/storagecommit|'''storagecommit''']] event.)
The '''onstorage''' event will only fire on window objects. Handlers attached to document.body or document objects will not receive the event. (Note this does not apply to the [[dom/Document/storagecommit|'''storagecommit''']] event.)
The '''onstorage''' event is specified in the W3C [http://go.microsoft.com/fwlink/?LinkId{{=}}217507 Web Storage] specification.
To invoke this event, do one of the following:
*Set or update a session or local storage value with [[apis/web-storage/Storage/setItem|'''setItem''']].
*Remove a session or local storage value with [[apis/web-storage/Storage/removeItem|'''removeItem''']].
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML]


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
|Manual_sections====Related pages (MSDN)===
*<code>frameSet</code>
*<code>window</code>
*<code>Introduction to Web Storage</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}