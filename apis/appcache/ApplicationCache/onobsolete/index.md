{{Page_Title}}
{{Flags
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The Webpage is associated with an application cache whose group is marked as obsolete.}}
{{API_Object_Property
|Property_applies_to=apis/appcache/ApplicationCache
|Read_only=No
|Example_object_name=window.applicationCache
|Javascript_data_type=null
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Checking fo the obsolete status
|Code=// try to trigger an application cache update
window.applicationCache.update();

// Asking the server for the manifest file returned status 404 or 410
// (results in appcache beeing deleted)
if (window.applicationCache.status === window.applicationCache.OBSOLETE) {
   console.log('The cache manifest is gone!');
}
}}{{Single Example
|Language=JavaScript
|Description=Listening for obsolete events
|Code=window.applicationCache.addEventListener('obsolete',function () {
   console.log('The cache manifest is gone!');
}, false);
}}
}}
{{Notes_Section
|Notes=If the manifest file can't be found, the cache is considered to be deleted.
If there is more than one event, the '''obsolete''' event will be the last one in the sequence.
Alternatively, you could use an anonymous delegate function such as
 <code>object.onobsolete {{=}} function (e) { … }</code>
where e is the cached event.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables={{Imported Compatibility Table
|Page=apis/appcache/ApplicationCache
}}
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Appcache, API}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx
|HTML5Rocks_link=
}}