{{Page_Title|performance.memory}}
{{Flags
|State=Not Ready
|Editorial notes=Not part of user_timing, resource_timing, or navigation_timing interfaces. Experimental; deletion candidate
|Checked_Out=No
|High-level issues=Stub, Deletion Candidate
|Content=Incomplete, Compatibility Incomplete
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Do not use. Proprietary. Chrome only. Gets quantized scripting memory usage numbers.}}
{{API_Object_Property
|Property_applies_to=apis/timing
|Read_only=Yes
|Example_object_name=window.performance
|Return_value_name=memoryInfo
|Javascript_data_type=Object
|Return_value_description=An object created with ''MemoryInfo'' constructor, containing  ''jsHeapSizeLimit'', ''totalJSHeapSize'' and ''usedJSHeapSize'' properties with numerical values.
|Example_value_name=memoryInfo
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=console.log(performance.memory)

// Would show, for example
//{
// jsHeapSizeLimit: 767557632,
// totalJSHeapSize: 58054528,
// usedJSHeapSize: 42930044
//}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=''usedJsHeapSize'' is the total amount of memory being used by JS objects including V8 internal objects, ''totalJsHeapSize'' is current size of the JS heap including free space not occupied by any JS objects. This means that ''usedJsHeapSize'' can not be greater than ''totalJsHeapSize''. Note that it is not necessarily that there has ever been ''totalJsHeapSize'' of alive JS objects.

The values are quantized as to not expose private information to attackers. If Chrome is run with the flag `--enable-precise-memory-info` the values are not quantized.


See the [https://bugs.webkit.org/attachment.cgi?id=154876&action=prettypatch WebKit Patch] for how the quantized values are exposed. The tests in particular help explain how it works.

* [https://bugs.webkit.org/show_bug.cgi?id=86636 WebKit bug]
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|DOM, Performance}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=22
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Chrome
|Version=Earlier than ~22
|Note=Needs ''--enable-memory-info'' [https://bugs.webkit.org/show_bug.cgi?id=86636 Webkit Ticket]
}}{{Compatibility Notes Row
|Browser=Chrome
|Version=~22 - 37
|Note=Use ''--enable-memory-info'' to get precise, non quantized memory usage numbers.
}}
}}