{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The user agent is downloading resources listed by the manifest. The event object's total attribute returns the total number of files to be downloaded. The event object's loaded attribute returns the number of files processed so far.}}
{{API_Object_Property
|Property_applies_to=apis/appcache/ApplicationCache
|Read_only=No
|Example_object_name=ApplicationCache
|Javascript_data_type=unsigned short
}}
{{Examples_Section
|Not_required=Yes
|Examples=
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
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}