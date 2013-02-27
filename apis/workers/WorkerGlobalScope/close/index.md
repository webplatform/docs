{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Discards any pending tasks and immediately closes the worker.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/workers/WorkerGlobalScope
|Example_object_name=object
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=This method sets the worker's WorkerGlobalScope object's closing flag to true, preventing any further tasks from being queued.

Use the '''terminate''' method if you want to stop a worker from a parent thread.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Web Workers Specification
|URL=http://dev.w3.org/html5/workers
|Status=W3C Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Webworkers}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}