{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|This callback is triggered when the buffer used to store the list of PerformanceResourceTiming is full.}}
{{API_Object_Property
|Property_applies_to=apis/resource_timing/Performance
|Read_only=Yes
|Example_object_name=
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example uses clearResourceTimings and setResourceTimingBufferSize to set an initial buffer size. It then uses onresourcetimingbufferfull to detect when the buffer is full, and executes a function that uses clearResourceTimings to clear the buffer.
|Code=performance.clearResourceTimings();
setResourceTimingBufferSize(100);

function buffFull() {
  performance.clearResourceTimings();
  };

performance.onresourcetimingbufferfull = buffFull;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Resource Timing Specification
|URL=http://www.w3.org/TR/resource-timing/
|Status=W3C Working Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, Resource Timing}}
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