{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The '''WorkerLocation''' object is created by using the '''self'''.[[apis/workers/properties/location|'''location''']] method inside a worker thread. The '''self''' object is a reference to the [[apis/workers/objects/WorkerGlobalScope|'''WorkerGlobalScope''']] object.
The '''WorkerLocation'''  object can decompose the URL into the following component properties: [[apis/workers/properties/href|'''href''']], [[apis/workers/properties/protocol|'''protocol''']], [[apis/workers/properties/host|'''host''']], [[apis/workers/properties/hostname|'''hostname''']], [[apis/workers/properties/port|'''port''']], [[apis/workers/properties/pathname|'''pathname''']], [[apis/workers/properties/search|'''search''']], and [[apis/workers/properties/hash|'''hash''']].The '''href'''  property contains the absolute URL of the worker at its creation.
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_webworkers\ie]:%20WorkerLocation object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
|Import_Notes====Syntax===
===Members===
The '''WorkerLocation''' object has these types of members:
*[#properties Properties]


====Properties====
The '''WorkerLocation''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/workers/properties/hash|'''hash''']]
|Contains the anchor portion of the URL including the hash sign (#).
|-
|[[apis/workers/properties/host|'''host''']]
|Contains the hostname and port values of the URL.
|-
|[[apis/workers/properties/hostname|'''hostname''']]
|Contains the hostname of a URL.
|-
|[[apis/workers/properties/href|'''href''']]
|Contains the hypertext reference (HREF) of the URL.
|-
|[[apis/workers/properties/pathname|'''pathname''']]
|Contains the pathname of the URL.
|-
|[[apis/workers/properties/port|'''port''']]
|Contains the port number of the URL.
|-
|[[apis/workers/properties/protocol|'''protocol''']]
|Contains the protocol of the URL.
|-
|[[apis/workers/properties/search|'''search''']]
|Contains the query part of the URL, including the question mark.
|}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=22.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=15.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}