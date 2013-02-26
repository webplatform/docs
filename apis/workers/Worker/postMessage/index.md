{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Posts a message to the worker with which the object is associated.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=message
|Data type=any
|Description=This argument can be structured data, e.g.:
<code>worker.postMessage({opcode: 'activate', device: 1938, parameters: [23, 102]});</code>
|Optional=No
}}{{Method Parameter
|Name=transfer
|Data type=any
|Optional=Yes
}}
|Method_applies_to=apis/workers/Worker
|Example_object_name=object
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=A message can be a JavaScript primitive, object, or array, but not a function.
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