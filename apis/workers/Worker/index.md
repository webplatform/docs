{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|An object representing a worker, that is used to communicate with the worker.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Spawning and communicating with a Worker (document.html)
|Code=// create worker
var worker = new Worker('script.js');
// receive data from worker
worker.onmessage = function(event) {
  console.log("Received data from worker", event.data);
  // quit worker
  this.terminate();
};
// pass data to worker
worker.postMessage("hello worker");
}}{{Single Example
|Language=JavaScript
|Description=Being spawned as a worker (script.js) and communicating with parent (document.html)
|Code=// pass data to parent
self.postMessage("ready for business");
// receive data from parent
self.onmessage = function(event) {
   self.postMessage('Worker received ' + event.data);
};
}}{{Single Example
|Language=JavaScript
|Description=Loading additional resources from within a Worker (script.js)
|Code=// (synchronously) load external scripts - URLs relative to the parent document's location
importScripts('additional.js', 'another-one.js', 'as-many-as-you-like.js' /* , ... */);
// pass data to parent, executed *after* importScripts() received all files
self.postMessage("ready for business");
}}
}}
{{Notes_Section
|Notes=In the past, if you had to do a task on a webpage that might take a long time, you forced the user to wait until the task was finished. Workers can solve that problem by packaging and running code that runs separately from the main webpage. These packages are called threads and run in the background. You can have more than one worker running at once, each with its own thread and JavaScript code file.

Workers run in a "sandbox" and have limited scope. They cannot access most of the object model of the webpage but do have access to the global core JavaScript objects. You can use the '''WorkerGlobalScope''' object inside the worker to access objects in the worker's scope.

To terminate a worker thread from the main document, use the '''terminate''' method. To terminate the worker thread from inside its own code, use the '''close''' method.

You can send messages to a worker from the main document using '''postMessage'''. The message will be cloned. You can receive messages from the worker by listening for message events using the '''onmessage''' event.
If a worker throws an exception and doesn't handle the exception itself, the exception will create an event you can listen for with the '''onerror''' event.

You can determine the location of a worker from inside the worker by using the '''WorkerLocation''' object.

You can determine which navigator objects are available to the worker by using the '''WorkerNavigator''' object.
Shared workers are not supported in this release.

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