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
{{Topics|Events}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=Setting the '''onprogress''' property.
|LiveURL=
|Code=

function progres()
{
    alert("XDR onprogress");
    alert("Got: " + xdr.responseText);
}
...
xdr.onprogress {{=}} progres;

}}}}
{{Notes_Section
|Notes=
===Remarks===
When the '''onprogress''' event occurs, 
partial data can be retrieved using '''responseText'''.
The onprogress event may occur 0, 1 or many times in the time interval between 
the [[apis/xhr/events/load|'''onload''']] event.
To invoke this event, do one of the following:
*Event handlers are called as needed after a request is '''sent'''.

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
*<code>XMLHttpRequest Enhancements in Internet Explorer 8</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}