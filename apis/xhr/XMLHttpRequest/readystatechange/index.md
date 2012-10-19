{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Fires whenever the readyState of the request changes, mostly used to determine whether the body of the response is available for handling.}}
{{Event
|Event_applies_to=apis/xhr/objects/XMLHttpRequest
|Interface=dom/objects/Event
|Target=apis/xhr/objects/XMLHttpRequest
|Default_action=
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following script demonstrates how to set an asynchronous event handler that alerts the user when the '''readyState''' property of the request reaches complete (<code>4</code>). Note that you must set the event handler after calling '''open''', which resets all properties of the '''XMLHttpRequest''' object to their initial value.
|Code=function reportStatus() {
    if (xhr.readyState {{=}}{{=}} 4 /* complete */) {
        if (xhr.status {{=}}{{=}} 200 {{!}}{{!}} xhr.status {{=}}{{=}} 304) {
            console.log("Transfer complete.");
        }
        else {
            // error occurred
        }
    }
}
var xhr {{=}} new XMLHttpRequest();
xhr.open("GET", "http://localhost/test.xml", true);
xhr.onreadystatechange {{=}} reportStatus;
xhr.send();
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*[[apis/xhr/objects/XMLHttpRequest]]
*[[apis/xhr/properties/readyState]]
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}