{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/events/error
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
|Description=Setting the onerror property.
|LiveURL=
|Code=
&lt;script type{{=}}"text/javascript"&gt;
function err()
{
    alert("XDR onerror");
}
...
xdr.onerror {{=}} err; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
The document can respond to the error, but there is no way to determine the cause or nature of the error.
The '''onerror''' event does not occur when the [[apis/xhr/events/timeout|'''ontimeout''']] event occurs.
To invoke this event, do one of the following:
*Cannot invoke.
The '''onerror''' event occurs when the request could not be completed because of an error.

|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

===Event handler parameters===
This method has no parameters.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>XDomainRequest</code>
*<code>Reference</code>
*<code>[[apis/xhr/events/load|onload]]</code>
*<code>[[apis/xhr/events/progress|onprogress]]</code>
*<code>Conceptual</code>
*<code>XMLHttpRequest Enhancements in Internet Explorer 8</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}