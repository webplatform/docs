{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|An object representing the "inside" of a worker.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=The '''WorkerGlobalScope''' object is accessed by using the '''self''' or '''this''' property and is accessed only inside a worker. A worker has the following functionality within its scope:
*It can use the '''XMLHttpRequest''' method.
*It has a '''self''' property, which contains a reference to the worker object.
*It can call all global JavaScript core methods.
*It has a '''navigator''' object, which provides the '''appName''', '''appVersion''', '''onLine''',  '''userAgent''', and '''platform''' properties but no others.
*The '''location'''  property creates the '''WorkerLocation''' object, which contains URL information on the worker's location. This property is similar to the '''Window.location''' property, but is read-only.
*It supports the worker versions of the '''setTimeout''', '''setInterval''', '''clearTimeout''', and '''clearInterval''' methods, which are similar to the methods of the same name for the '''Window''' object.
*It can load other JavaScript files into the scope of the worker using the '''importScripts''' method.

Workers do not have access to the Document Object Model (DOM), nor the '''window''', '''document''', and '''parent''' objects.
To terminate a worker thread from inside, use the '''close'''  method. From the main document, use the '''terminate''' method to terminate the worker thread.
You can send messages to the main document using '''postMessage''' and receive messages from the main document using the '''onmessage''' message handler.
You can create new child workers  from inside a worker. They must all run in the same host and their location depends on the parent worker of the new worker, not the original webpage. Because a new worker is likely to be in a separate process, you shouldn't create too many workers at once. Also, because messages between workers and their parents are copies and not shared, too many workers can use up resources quickly.
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
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
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
|Safari_mobile_supported=Yes
|Safari_mobile_version=5.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
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