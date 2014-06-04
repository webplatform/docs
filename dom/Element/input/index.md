{{Page_Title}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Interface=dom/Element
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following script queries the event [[dom/Event/target|'''target''']] as the text in a '''textArea''' is changed.
|Code=&lt;script type{{=}}"text/javascript"&gt;
function handleInput(ev) {
    alert(ev.target.value);
}
window.onload {{=}} function() {
    document.getElementById('myTextArea').addEventListener('input',handleInput,false);
}
&lt;/script&gt;
&lt;textarea id{{=}}"myTextArea"&gt;Edit this text.&lt;/textarea&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
You can use the '''oninput''' to detect when the contents of a '''textArea''', '''input type{{=}}text''', or '''input type{{=}}password''' have changed. This event occurs immediately after modification, unlike the [[dom/Element/change|'''change''']] event, which occurs when the element loses focus.
To invoke this event, do one of the following:
*Enter some text into a form field.
*Cut, delete, or paste content.
*Navigate to another document.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML]
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
|External_links=* [http://www.w3.org/TR/2003/REC-DOM-Level-2-HTML-20030109/html.html#ID-6043025 DOM Level 2]
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}