{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Returns the time immediately after the user agent finishes establishing the connection to the server to retrieve the current document.}}
{{API_Object_Property
|Property_applies_to=apis/navigation_timing/PerformanceTiming
|Read_only=Yes
|Example_object_name=PerformanceTiming
|Return_value_name=
|Javascript_data_type=unsigned long
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=<nowiki>var perftime = performance.timing;
document.write("connectEnd: " + perftime.connectEnd + "<br />");
document.write("connectStart: " + perftime.connectStart + "<br />");
document.write("domainLookupEnd: " + perftime.domainLookupEnd + "<br />");
document.write("domainLookupStart: " + perftime.domainLookupStart + "<br />");
document.write("domComplete: " + perftime.domComplete + "<br />");
document.write("domContentLoadedEventStart: " + perftime.domContentLoadedEventStart + "<br />");
document.write("domInteractive: " + perftime.domInteractive + "<br />");
document.write("domLoading: " + perftime.domLoading + "<br />");
document.write("fetchStart: " + perftime.fetchStart + "<br />");
document.write("loadEventEnd: " + perftime.loadEventEnd + "<br />");
document.write("loadEventStart: " + perftime.loadEventStart + "<br />");
document.write("navigationStart: " + perftime.navigationStart + "<br />");
document.write("redirectEnd: " + perftime.redirectEnd + "<br />");
document.write("redirectStart: " + perftime.redirectStart + "<br />");
document.write("requestStart: " + perftime.requestStart + "<br />");
document.write("responseEnd: " + perftime.responseEnd + "<br />");
document.write("responseStart: " + perftime.responseStart + "<br />");
document.write("secureConnectionStart: " + perftime.secureConnectionStart + "<br />");
document.write("unloadEventEnd: " + perftime.unloadEventEnd + "<br />");
document.write("unloadEventStart: " + perftime.unloadEventStart + "<br />");</nowiki>
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
|Name=W3C Navigation Timing Specification 2
|URL=http://www.w3.org/TR/navigation-timing-2/
|Status=W3C Working Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, Navigation Timing}}
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
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=23.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=4.0
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=10.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}