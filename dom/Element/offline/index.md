{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/Element
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
|Description=The following example sets an event handler that responds to both [[dom/events/online|'''ononline''']] and '''onoffline''' events using the '''type''' property of the '''event''' object.
|LiveURL=
|Code=
function reportConnectionEvent(e)
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
}}}}
{{Notes_Section
|Notes=
===Remarks===
If Asynchronous JavaScript and XML (AJAX) Connection Services are disabled, this event is not raised. (These services are enabled by default.)
To invoke this event, do one of the following:
*Set the browser to "Work Offline" on the '''File''' menu.

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
*<code>body</code>
*<code>frameSet</code>
*<code>window</code>
*<code>Reference</code>
*<code>[[dom/properties/onLine|onLine]]</code>
*<code>[[dom/events/online|ononline]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}