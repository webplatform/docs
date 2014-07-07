{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Not part of user_timing, resource_timing, or navigation_timing interfaces. Non-standard; deletion candidate
|Checked_Out=No
|High-level issues=Deletion Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Deletion candidate.}}
{{API_Object_Property
|Property_applies_to=apis/timing/objects/performanceTiming
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to calculate the time that is required to request the document before the document begins to display for the user.
|Code=var oTiming {{=}} window.performance.timing;
var iTimeMS {{=}} oTiming.msFirstPaint - oTiming.navigationStart;
}}
}}
{{Notes_Section
|Notes====Remarks===
The value reported by the '''msFirstPaint''' property represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).
Windows Internet Explorer 9.  This property is supported only for documents displayed in IE9 Standards mode.  For more information, please see Defining Document Compatibility.
|Import_Notes====Syntax===
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[apis/timing/objects/performanceTiming|performanceTiming]]</code>
*<code>[[apis/timing/properties/navigationStart|navigationStart]]</code>
}}
{{Topics|API, Navigation Timing}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}