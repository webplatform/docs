{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=apis/timing/properties
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to calculate the time required to load the document, which this example defines as the time between the initial navigation action and the time when the document is presented to the user.
|LiveURL=
|Code=
var oTiming {{=}} window.performance.timing;
var iTimeMS {{=}} oTiming.msFirstPaint - oTiming.navigationStart;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The value reported by the '''navigationStart''' property represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}210425 Navigation Timing], Section 4.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/timing/objects/performanceTiming|performanceTiming]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}