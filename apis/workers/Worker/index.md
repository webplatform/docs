{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
In the past, if you had to do a task on a webpage that might take a long time, you forced the user to wait until the task was finished. Workers can solve that problem by packaging and running code that runs separately from the main webpage. These packages are called threads and run in the background. You can have more than one worker running at once, each with its own thread and JavaScript code file.
Workers run in a "sandbox" and have limited scope. They cannot access most of the object model of the webpage but do have access to the global core JavaScript objects. You can use the [[apis/workers/objects/WorkerGlobalScope|'''WorkerGlobalScope''']] object inside the worker to access objects in the worker's scope.
To terminate a worker thread from the main document, use the [[apis/workers/methods/terminate|'''terminate''']] method. To terminate the worker thread from inside its own code, use the [[apis/workers/methods/close|'''close''']] method.
You can send messages to a worker from the main document using [[apis/workers/methods/postMessage|'''postMessage''']]. The message will be cloned. You can receive messages from the worker by listening for message events using the [[apis/workers/events/onmessage|'''onmessage''']] event.
If a worker throws an exception and doesn't handle the exception itself, the exception will create an event you can listen for with the [[apis/workers/properties/onerror|'''onerror''']] event.
You can determine the location of a worker from inside the worker by using the [[apis/workers/objects/WorkerLocation|'''WorkerLocation''']] object.
You can determine which navigator objects are available to the worker by using the [[apis/workers/objects/WorkerNavigator|'''WorkerNavigator''']] object.
Shared workers are not supported in this release.
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_webworkers\ie]:%20Worker object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
|Import_Notes=
===Syntax===
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
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}