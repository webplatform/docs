{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=HashChangeEvent
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Topics|Events}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=Attaching an event handler to a new '''onhashchange''' event enables the page to detect when the hash has changed and an AJAX navigation has occurred. See Introducing AJAX Navigations for a more robust example.
|LiveURL=
|Code=
&lt;body onhashchange{{=}}"HashChangeHandler();"&gt;
...
&lt;/body&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
In Asynchronous JavaScript and XML (AJAX) applications, client requests
that do not trigger traditional page navigation
should update the
[[dom/properties/hash|'''hash''']]
property. This lets the '''Back''' button
function more predictably.
The URL fragment (bookmark) can be set by script.
The value is appended to the displayed URL,
and the navigation is saved in the browser history.
Windows Internet Explorer 8. The browser's '''Back''' and '''Forward''' buttons do not generate '''onhashchange''' events for frames or '''iframe'''s; instead, the frame is refreshed each time. Web pages hosted in frames or '''iframe'''s should use their [[dom/events/load|'''onload''']] handler or equivalent to read the current URL hash information from the [[dom/location|'''location''']].[[dom/properties/hash|'''hash''']] property and set their states accordingly.
When first navigating to a page that contains a hash identifier in the URL, an '''onhashchange''' event is ''not'' fired. It is expected that the freshly loaded page can inspect the value of the [[dom/location|'''location''']].[[dom/properties/hash|'''hash''']] property to extract the current hash value. After this first page loads, setting the '''hash''' property will fire the '''onhashchange''' event as expected. This behavior avoids any negative impact on Web page load performance by removing a possible redundant event.
To invoke this event, do one of the following:
*Set the
[[dom/location|'''location''']].[[dom/properties/hash|'''hash''']]
(bookmark) property.
*Navigate to the same page with a different bookmark.

The ''pEvtObj'' parameter is required for the following interfaces:
*'''HTMLWindowEvents3'''

|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>window</code>
*<code>body</code>
*<code>frameSet</code>
*<code>Introducing AJAX Navigations</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}