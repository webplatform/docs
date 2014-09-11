{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''onerror''' event occurs when the request could not be completed because of an error.}}
{{Event
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Default_action=
|Content=
|Interface=dom/events/error
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Setting the onerror property.
|Code=&lt;script type{{=}}"text/javascript"&gt;
function err()
{
    alert("XDR onerror");
}
...
xdr.onerror {{=}} err;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The document can respond to the error, but there is no way to determine the cause or nature of the error.
The '''onerror''' event does not occur when the [[apis/xhr/events/timeout|'''ontimeout''']] event occurs.
To invoke this event, do one of the following:
*Cannot invoke.
|Import_Notes====Event handler parameters===
This method has no parameters.
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
*<code>XDomainRequest</code>
*<code>Reference</code>
*<code>[[apis/xhr/events/load|onload]]</code>
*<code>[[apis/xhr/events/progress|onprogress]]</code>
*<code>Conceptual</code>
*<code>XMLHttpRequest Enhancements in Internet Explorer 8</code>
}}
{{Topics|API}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}