---
title: 'Worker'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'An object representing a worker, that is used to communicate with the worker.'
tags:
  0: API
  1: Objects
  3: Webworkers
uri: apis/workers/Worker

---
## Summary

An object representing a worker, that is used to communicate with the worker.

## Properties

API Name
:   Summary

[onerror](/apis/workers/Worker/onerror)
:   An event listener to be called when an error occurs.

[onmessage](/apis/workers/Worker/onmessage)
:   An event listener to be called when a message is received from the worker.

## Methods

API Name
:   Summary

[postMessage](/apis/workers/Worker/postMessage)
:   Posts a message to the worker with which the object is associated.

[terminate](/apis/workers/Worker/terminate)
:   Immediately terminates the worker with which the object is associated.

## Events

*No events.*

## Examples

Spawning and communicating with a Worker (document.html)

``` js
// create worker
var worker = new Worker('script.js');
// receive data from worker
worker.onmessage = function(event) {
  console.log("Received data from worker", event.data);
  // quit worker
  this.terminate();
};
// pass data to worker
worker.postMessage("hello worker");
```

Being spawned as a worker (script.js) and communicating with parent (document.html)

``` js
// pass data to parent
self.postMessage("ready for business");
// receive data from parent
self.onmessage = function(event) {
   self.postMessage('Worker received ' + event.data);
};
```

Loading additional resources from within a Worker (script.js)

``` js
// (synchronously) load external scripts - URLs relative to the parent document's location
importScripts('additional.js', 'another-one.js', 'as-many-as-you-like.js' /* , ... */);
// pass data to parent, executed *after* importScripts() received all files
self.postMessage("ready for business");
```

## Notes

In the past, if you had to do a task on a webpage that might take a long time, you forced the user to wait until the task was finished. Workers can solve that problem by packaging and running code that runs separately from the main webpage. These packages are called threads and run in the background. You can have more than one worker running at once, each with its own thread and JavaScript code file.

Workers run in a "sandbox" and have limited scope. They cannot access most of the object model of the webpage but do have access to the global core JavaScript objects. You can use the **WorkerGlobalScope** object inside the worker to access objects in the worker's scope.

To terminate a worker thread from the main document, use the **terminate** method. To terminate the worker thread from inside its own code, use the **close** method.

You can send messages to a worker from the main document using **postMessage**. The message will be cloned. You can receive messages from the worker by listening for message events using the **onmessage** event. If a worker throws an exception and doesn't handle the exception itself, the exception will create an event you can listen for with the **onerror** event.

You can determine the location of a worker from inside the worker by using the **WorkerLocation** object.

You can determine which navigator objects are available to the worker by using the **WorkerNavigator** object. Shared workers are not supported in this release.

## Related specifications

[W3C Web Workers Specification](http://dev.w3.org/html5/workers)
:   W3C Editor's Draft
