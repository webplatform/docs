{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Spawning and communicating with a Worker
|Code=// create worker
var worker = new Worker('script.js');
// receive data from worker
worker.onmessage = function(event) {
 console.log("Received data from worker", event.data);
};
// pass data to worker
worker.postMessage("hello worker");
}}
}}
{{Notes_Section
|Notes====Remarks===
In the past, if you had to do a task on a webpage that might take a long time, you forced the user to wait until the task was finished. Workers can solve that problem by packaging and running code that runs separately from the main webpage. These packages are called threads and run in the background. You can have more than one worker running at once, each with its own thread and JavaScript code file.
Workers run in a "sandbox" and have limited scope. They cannot access most of the object model of the webpage but do have access to the global core JavaScript objects. You can use the [[apis/workers/objects/WorkerGlobalScope|'''WorkerGlobalScope''']] object inside the worker to access objects in the worker's scope.
To terminate a worker thread from the main document, use the [[apis/workers/methods/terminate|'''terminate''']] method. To terminate the worker thread from inside its own code, use the [[apis/workers/methods/close|'''close''']] method.
You can send messages to a worker from the main document using [[apis/workers/methods/postMessage|'''postMessage''']]. The message will be cloned. You can receive messages from the worker by listening for message events using the [[apis/workers/events/onmessage|'''onmessage''']] event.
If a worker throws an exception and doesn't handle the exception itself, the exception will create an event you can listen for with the [[apis/workers/properties/onerror|'''onerror''']] event.
You can determine the location of a worker from inside the worker by using the [[apis/workers/objects/WorkerLocation|'''WorkerLocation''']] object.
You can determine which navigator objects are available to the worker by using the [[apis/workers/objects/WorkerNavigator|'''WorkerNavigator''']] object.
Shared workers are not supported in this release.
 
|Import_Notes====Syntax===
===Members===
The '''Worker''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''Worker''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[apis/workers/events/onmessage|'''message''']]
|Returns a message from the parent thread to the worker thread, or between two [[apis/web-messaging/objects/MessagePort|'''MessagePort''']] objects.
|}
 

====Methods====
The '''Worker''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/workers/methods/postMessage|'''postMessage''']]
|Sends a message from the worker  to the parent thread.
|-
|[[apis/workers/methods/terminate|'''terminate''']]
|Terminates a worker thread immediately.
|}
 

====Properties====
The '''Worker''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/indexedDB/properties/indexedDB|'''indexedDB''']]
|Allows access to the Indexed Database API, as implemented by Internet Explorer 10.
|-
|[[apis/workers/properties/onerror|'''onerror''']]
|Returns an error if a worker throws an unhandled exception.
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
|Chrome_version=4.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.5
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.6
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=4.0
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
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.50
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=11.0
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}