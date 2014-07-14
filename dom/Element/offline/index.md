{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, spec, and compat
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
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
|Description=The following example sets an event handler that responds to both [[dom/Element/online|'''ononline''']] and '''onoffline''' events using the '''type''' property of the '''event''' object.
|Code=function reportConnectionEvent(e)
{
    if (!e) e {{=}} window.event;
    
    if ('online' {{=}}{{=}} e.type) {
        alert( 'The browser is ONLINE.' );
    }
    else if ('offline' {{=}}{{=}} e.type) {
        alert( 'The browser is OFFLINE.' );
    }
    else {
        alert( 'Unexpected event: ' + e.type );
    }
}
window.onload {{=}} function() {
    document.body.ononline {{=}} reportConnectionEvent;
    document.body.onoffline {{=}} reportConnectionEvent;
}
}}
}}
{{Notes_Section
|Notes====Remarks===
If Asynchronous JavaScript and XML (AJAX) Connection Services are disabled, this event is not raised. (These services are enabled by default.)
To invoke this event, do one of the following:
*Set the browser to "Work Offline" on the '''File''' menu.
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.

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
*<code>body</code>
*<code>frameSet</code>
*<code>window</code>
*<code>Reference</code>
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}