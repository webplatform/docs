{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Removes all DOMHighResTimeStamp durations for the given measure name, or removes all measures and their associated DOMHighResTimeStamp durations.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=measureName
|Data type=any
|Description=Name of the measures(s) to be cleared.
|Optional=Yes
}}
|Method_applies_to=apis/user_timing/Performance
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=void
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=// set begin mark
performance.mark("startMark");
// execute a function to be measured
someFunction();
// set end mark
performance.mark("stopMark");

// save the timing information
performance.measure("functionTime", "startMark", "stopMark");
// display the measured time
var measures = performance.getEntriesByType("measure");
alert("functionTime: " + measures[0].duration);

// clear the measure "functionTime"
performance.clearMeasures("functionTime");
// clear all marks
performance.clearMarks();
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=If a value for the  ''measureName'' parameter is specified, only measures with that name are removed.  If there are no measures with the specified name, this method does nothing.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C User Timing Specification
|URL=http://www.w3.org/TR/user-timing/
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, User Timing}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}