{{Page_Title|performance.memory}}
{{Flags
|High-level issues=Stub
|Content=Incomplete, Compatibility Incomplete
}}
{{Standardization_Status|Experimental}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=apis/timing
|Read_only=Yes
|Javascript_data_type=Object
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=performance.memory

// returns

{
jsHeapSizeLimit: 767557632,
totalJSHeapSize: 58054528,
usedJSHeapSize: 42930044
}
}}
}}
{{Notes_Section
|Notes=usedJsHeapSize is the total amount of memory being used by JS objects including V8 internal objects, totalJsHeapSize is current size of the JS heap including free space not occupied by any JS objects. This means that usedJsHeapSize can not be greater than totalJsHeapSize. Note that it is not necessarily that there has ever been totalJsHeapSize of alive JS objects.

The values are quantized as to not expose private information to attackers.

See the [https://bugs.webkit.org/attachment.cgi?id=154876&action=prettypatch WebKit Patch] for how the quantized values are exposed. The tests in particular help explain how it works.

* [https://bugs.webkit.org/show_bug.cgi?id=86636 WebKit bug]
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
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
|Note=Needs `--enable-memory-info` [https://bugs.webkit.org/show_bug.cgi?id=86636 Webkit Ticket]
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[apis/timing/objects/performance|performance]]</code>
}}
{{Topics|DOM, Performance}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|HTML5Rocks_link=
}}