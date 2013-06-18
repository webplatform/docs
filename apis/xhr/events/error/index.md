{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/Element
|Interface=dom/events/error
|Target=dom/Element
|Default_action=
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=Setting the onerror property.
|Code=&lt;script type{{=}}"text/javascript"&gt;
function err()
{
    alert("XDR onerror");
}
...
xdr.onerror {{=}} err;
}}
}}
{{Notes_Section
|Notes====Remarks===
The document can respond to the error, but there is no way to determine the cause or nature of the error.
The '''onerror''' event does not occur when the [[apis/xhr/events/timeout|'''ontimeout''']] event occurs.
To invoke this event, do one of the following:
*Cannot invoke.
The '''onerror''' event occurs when the request could not be completed because of an error.
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.

===Event handler parameters===
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