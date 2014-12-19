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
{{Summary_Section|Stores the DOMHighResTimeStamp duration between two marks along with the associated name (a "measure").}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=name
|Data type=any
|Description=Name associated with the performance measure.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=startMark
|Data type=any
|Description=Name of the start performance mark.
|Optional=Yes
}}{{Method Parameter
|Index=2
|Name=endMark
|Data type=any
|Description=Name of the end performance mark.
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
|Notes=*If neither the startMark nor the endMark argument is specified, measure() will store the duration as a DOMHighResTimeStamp from navigationStart to the current time.
*If the startMark argument is specified, but the endMark argument is not specified, measure() will store the duration as a DOMHighResTimeStamp from the most recent occurrence of the start mark to the current time.
*If both the startMark and endMark arguments are specified, measure() will store the duration as a DOMHighResTimeStamp from the most recent occurrence of the start mark to the most recent occurrence of the end mark.
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