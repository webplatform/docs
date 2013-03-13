{{Page_Title}}
{{Flags
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The user agent is downloading resources listed by the manifest. The event object's total attribute returns the total number of files to be downloaded. The event object's loaded attribute returns the number of files processed so far.}}
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
|Description=Registering an progress event handler to keep track of the number of items that need to be fetched and that are already fetched
|Code=CACHE MANIFEST
# Example manifest
CACHE:
afile.css
anotherfile.js

// will be called two times in total, because there are two files to fetch (afile.css, anotherfile.js)
window.applicationCache.addEventListener('progress', function (event) {
   console.log('Item', event.loaded, 'of', event.total, 'fetched');
}, false);
}}
}}
{{Notes_Section
|Notes=If more than one event is triggered and the '''progress''' event is included, the next events may include '''progress''', '''error''', '''cached''', or '''updateready'''.
Alternatively, you could use an anonymous delegate function such as
 <code>object.onprogress {{=}} function (e) { … }</code>
where e is the cached event.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C ApplicationCache Specification
|URL=http://dev.w3.org/html5/spec/single-page.html#application-cache-api
|Status=W3C Editor's Draft
}}
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