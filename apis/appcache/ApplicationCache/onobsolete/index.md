{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=apis/appcache/ApplicationCache
|Read_only=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
If the manifest file can't be found, the cache is considered to be deleted.
If there is more than one event, the '''obsolete''' event will be the last one in the sequence.
Alternatively, you could use an anonymous delegate function such as
 <code>object.onobsolete {{=}} function (e) { … }</code>
where e is the cached event.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/appcache/ApplicationCache|ApplicationCache]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}