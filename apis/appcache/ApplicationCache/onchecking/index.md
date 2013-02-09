{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The user agent is checking for an update, or attempting to download the manifest for the first time. This is always the first event in the sequence.}}
{{API_Object_Property
|Property_applies_to=apis/appcache/ApplicationCache
|Read_only=No
|Example_object_name=window.applicationCache
|Javascript_data_type=null
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=If more than one event is triggered and the '''checking''' event is included, the next events may include '''noupdate''', '''downloading''', '''obsolete''', or '''error'''.
Alternatively, you could use an anonymous delegate function such as
 <code>object.onchecking {{=}} function (e) { … }</code>
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
{{Topics|Appcache}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx
|HTML5Rocks_link=
}}