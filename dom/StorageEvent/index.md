{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Missing initStorageEvent
see http://msdn.microsoft.com/en-us/library/ie/ff974349(v=vs.85).aspx
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Provides event properties that are specific to the onstorage event.}}
{{API_Object
|Subclass_of=dom/Event
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following code example demonstrates how to respond to storage events.
|Code=function reportStorage(evt) {
    alert("Storage was updated for " + evt.url);
}
window.onload {{=}} function() {
if(window.sessionStorage){
    window.addEventListener('storage',reportStorage,false);
    window.sessionStorage.setItem('key','value');
}
}
}}
}}
{{Notes_Section
|Usage=Used to notify a user that data has been successfully written to their DOM Storage area of their device.
|Notes=In MSIE/Windows browsers...

1. DOM storage is user and/or administrator configurable from Internet Options and Group Policy and can be enabled/disabled in the client browser.

2. For local (x)html files that use the file: protocol, sessionStorage and localStorage are undefined.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 5.11.1.5
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/StorageEvent StorageEvent]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974349(v=vs.85).aspx StorageEvent]
|HTML5Rocks_link=
}}