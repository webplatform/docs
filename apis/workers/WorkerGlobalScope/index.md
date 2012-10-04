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
The '''WorkerGlobalScope''' object is accessed by using the '''self'''     or '''this''' property and is accessed only inside a worker. A worker has the following functionality within its scope:
*It can use the  '''XMLHttpRequest''' method.
*It has a '''self''' property, which contains a reference to the worker object.
*It can call all global JavaScript core methods.
*It has a '''navigator''' object, which provides the '''appName''', '''appVersion''', '''onLine''',  '''userAgent''', and '''platform''' properties but no others.
*The [[apis/workers/properties/location|'''location''']]  property creates the [[apis/workers/objects/WorkerLocation|'''WorkerLocation''']]  object, which contains URL information on the worker's location. This property is similar to the '''Window.location''' property, but is read-only.
*It supports the worker versions of the [[apis/workers/methods/setTimeout|'''setTimeout''']], [[apis/workers/methods/setInterval|'''setInterval''']], [[apis/workers/methods/clearTimeout|'''clearTimeout''']], and [[apis/workers/methods/clearInterval|'''clearInterval''']] methods, which are similar to the methods of the same name for the '''Window''' object.
*It can load other JavaScript files into the scope of the worker using the [[apis/workers/methods/importScripts|'''importScripts''']] method.

Workers do not have access to the Document Object Model (DOM), nor the '''window''', '''document''', and '''parent''' objects.
To terminate a worker thread from inside, use the [[apis/workers/methods/close|'''close''']]  method. From the main document, use the [[apis/workers/methods/terminate|'''terminate''']]  method to terminate the worker thread.
You can send messages to the main document using [[apis/workers/methods/postMessage|'''postMessage''']] and receive messages from the main document using the [[apis/workers/events/onmessage|'''onmessage''']] message handler.
You can create new child workers  from inside a worker. They must all run in the same host and their location depends on the parent worker of the new worker, not the original webpage. Because a new worker is likely to be in a separate process, you shouldn't create too many workers at once. Also, because messages between workers and their parents are copies and not shared, too many workers can use up resources quickly.
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_webworkers\ie]:%20WorkerGlobalScope object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
|Import_Notes=
===Syntax===
===Members===
The '''WorkerGlobalScope''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''WorkerGlobalScope''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[apis/workers/events/onmessage|'''message''']]
|Returns a message from the parent thread to the worker thread, or between two [[apis/web-messaging/objects/MessagePort|'''MessagePort''']] objects.
|}
 

====Methods====
The '''WorkerGlobalScope''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/workers/methods/close|'''close''']]
|Stops a worker when called inside  worker code.
|-
|[[apis/workers/methods/importScripts|'''importScripts''']]
|Loads and executes one or more scripts into the worker specified by a URL.
|-
|[[apis/timing/methods/msWriteProfilerMark|'''msWriteProfilerMark''']]
|Writes a profiling event.
|-
|[[apis/workers/methods/postMessage|'''postMessage''']]
|Sends a message from the worker  to the parent thread.
|}
 

====Properties====
The '''WorkerGlobalScope''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|'''console'''
|Returns the windows console object to use to send messages.
|-
|[[apis/indexedDB/properties/indexedDB|'''indexedDB''']]
|Allows access to the Indexed Database API, as implemented by Internet Explorer 10.
|-
|[[apis/workers/properties/location|'''location''']]
|Returns the [[apis/workers/objects/WorkerLocation|'''WorkerLocation''']] object of a worker.
|-
|[[apis/workers/properties/navigator|'''navigator''']]
|Returns a [[apis/workers/objects/WorkerNavigator|'''WorkerNavigator''']] object.
|-
|[[apis/workers/properties/onerror|'''onerror''']]
|Returns an error if a worker throws an unhandled exception.
|-
|[[apis/workers/properties/self|'''self''']]
|Contains a reference to the '''WorkerGlobalScope''' object.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}