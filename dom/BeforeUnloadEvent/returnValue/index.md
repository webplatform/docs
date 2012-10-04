{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/objects/Event
|Read_only=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The [[dom/events/beforeunload|'''onbeforeunload''']] event allows you to warn a user who is navigating away from a page or closing the browser. Set the return value to false or a '''Variant''' of type '''String''' value to cancel the document unload event. You can also return a string or '''Boolean''' value from the event handler to display a message to the user, who is asked to confirm that they want to unload the document.
The warning dialog box in Windows Internet Explorer 9 is easier to read  than in earlier versions.  In the improved dialog box, it is easier to distinguish the default text from text provided by the website, and large buttons clearly indicate  how to stay on the page or navigate away.
[[Image:ie9_onbeforeunload_dialog.png]]
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 5.10.10


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/objects/BeforeUnloadEvent|BeforeUnloadEvent]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}