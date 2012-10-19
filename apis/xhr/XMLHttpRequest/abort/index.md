{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Aborts an ongoing asynchronous request of an XMLHttpRequest instance object.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/xhr/objects/XMLHttpRequest
|Example_object_name=xhr
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Calling it on an already aborted request throws an exception.
The '''abort''' method interrupts an asynchronous operation in progress.
Calling '''abort''' resets the object; the '''readyState''' is changed to 0 (uninitialized).
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203789 ], Section 3.6.5
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=XMLHttpRequest
|URL=http://www.w3.org/TR/XMLHttpRequest/
|Status=Working Draft
|Relevant_changes=Section 3.6.5
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*[[apis/xhr/objects/XMLHttpRequest]]
*<code>XDomainRequest]]</code>
*[[apis/xhr/methods/send]]
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}