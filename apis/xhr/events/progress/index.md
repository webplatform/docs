{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|When the '''onprogress''' event occurs, 
partial data can be retrieved using '''responseText'''.
}}
{{Event
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Default_action=
|Content=
|Interface=dom/objects/Event
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Setting the '''onprogress''' property.
|Code=function progres()
{
    alert("XDR onprogress");
    alert("Got: " + xdr.responseText);
}
...
xdr.onprogress {{=}} progres;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
When the '''onprogress''' event occurs, 
partial data can be retrieved using '''responseText'''.
The onprogress event may occur 0, 1 or many times in the time interval between 
the [[apis/xhr/events/load|'''onload''']] event.
To invoke this event, do one of the following:
*Event handlers are called as needed after a request is '''sent'''.
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
*<code>XMLHttpRequest Enhancements in Internet Explorer 8</code>
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}