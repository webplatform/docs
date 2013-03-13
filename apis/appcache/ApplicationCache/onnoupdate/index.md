{{Page_Title}}
{{Flags
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Indicates the manifest has not changed.}}
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
|Description=If the currently-cached copy of the manifest is up-to-date, the browser sends a noupdate event to the applicationCache object, and the update process is complete. Note that if you change any cached resources on the server, you must also change the manifest file itself, so that the browser knows it needs to fetch all the resources again.
|Code=window.applicationCache.addEventListener('noupdate',function () {
  console.log('The manifest file is up to date');
}, false);
}}
}}
{{Notes_Section
|Notes=If there is more than one event, the '''onupdate''' event will be the last one in the sequence.
Alternatively, you could use an anonymous delegate function such as
 <code>object.onnoupdate {{=}} function (e) { … }</code>
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