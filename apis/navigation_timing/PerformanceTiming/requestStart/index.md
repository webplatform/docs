{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Possible example
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|Mixed}}
{{API_Name}}
{{Summary_Section|Returns the time immediately before the user agent starts requesting the current document from the server, or from relevant application caches or from local resources. If the transport connection fails after a request is sent and the user agent reopens a connection and resends the request, returns the corresponding values of the new request.}}
{{API_Object_Property
|Property_applies_to=apis/navigation timing/PerformanceTiming
|Read_only=Yes
|Example_object_name=PerformanceTiming
|Javascript_data_type=unsigned long
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=The PerformanceTiming interface does not include an attribute to represent the completion of sending the request, e.g., requestEnd.
*Completion of sending the request from the user agent does not always indicate the corresponding completion time in the network transport, which brings most of the benefit of having such an attribute.
*Some user agents have high cost to determine the actual completion time of sending the request due to the HTTP layer encapsulation.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Navigation Timing Specification
|URL=http://www.w3.org/TR/navigation-timing/
|Status=W3C Recommendation
}}{{Related Specification
|Name=Navigation Timing 2
|URL=http://www.w3.org/TR/navigation-timing-2/
|Status=W3C Working Draft
}}
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
{{See_Also_Section}}
{{Topics|API, Navigation Timing}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}