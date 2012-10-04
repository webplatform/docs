{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=apis/timing/objects/performanceTiming
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to calculate the amount of time to complete a domain name  request for the document.
|LiveURL=
|Code=
var oTiming {{=}} window.performance.timing;
var iTimeMS {{=}} oTiming.domainLookupEnd - oTiming.domainLookupStart;
}}}}
{{Notes_Section
|Notes=
===Remarks===
If a page is retrieved from an application cache, '''domainLookupStart''' has the same value as [[apis/timing/properties/fetchStart|'''fetchStart''']].
The value reported by the '''domainLookupStart''' property represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).
Windows Internet Explorer 9.  This property is supported only for documents displayed in IE9 Standards mode.  For more information, see Defining Document Compatibility.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}210425 Navigation Timing], Section 4.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/timing/objects/performanceTiming|performanceTiming]]</code>
*<code>[[apis/timing/properties/domainLookupEnd|domainLookupEnd]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}