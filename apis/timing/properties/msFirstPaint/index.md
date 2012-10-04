{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=apis/timing/objects/performanceTiming
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to calculate the time that is required to request the document before the document begins to display for the user.
|LiveURL=
|Code=
var oTiming {{=}} window.performance.timing;
var iTimeMS {{=}} oTiming.msFirstPaint - oTiming.navigationStart;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The value reported by the '''msFirstPaint''' property represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).
Windows Internet Explorer 9.  This property is supported only for documents displayed in IE9 Standards mode.  For more information, please see Defining Document Compatibility.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/timing/objects/performanceTiming|performanceTiming]]</code>
*<code>[[apis/timing/properties/navigationStart|navigationStart]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}