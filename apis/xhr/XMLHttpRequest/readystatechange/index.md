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
|Description=The following script demonstrates how to set an asynchronous event handler that alerts the user when the '''readyState''' property of the request reaches complete (<code>4</code>). Note that you must set the event handler after calling '''open''', which resets all properties of the '''XMLHttpRequest''' object to their initial value.
|LiveURL=
|Code=
function reportStatus()
{
    if (oReq.readyState {{=}}{{=}} 4 /* complete */) {
        if (oReq.status {{=}}{{=}} 200 {{!}}{{!}} oReq.status {{=}}{{=}} 304) {
            alert('Transfer complete.');
        }
        else {
            // error occurred
        }
    }
}
var oReq {{=}} new XMLHttpRequest();
oReq.open("GET", "http://localhost/test.xml", true);
oReq.onreadystatechange {{=}} reportStatus;
oReq.send();
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''onreadystatechange''' event was introduced in Windows Internet Explorer 7.
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
*<code>XMLHttpRequest</code>
*<code>readyState</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}