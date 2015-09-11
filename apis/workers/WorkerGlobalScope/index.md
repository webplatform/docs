---
title: WorkerGlobalScope
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'An object representing the &quot;inside&quot; of a worker.'
tags:
  0: API
  1: Objects
  3: Webworkers
uri: apis/workers/WorkerGlobalScope

---
## <span>Summary</span>

An object representing the &quot;inside&quot; of a worker.

## <span>Properties</span>

API Name
:   Summary

[location](/apis/workers/WorkerGlobalScope/location)
:   Returns the WorkerLocation object created for the WorkerGlobalScope object when the worker was created.

[navigator](/apis/workers/WorkerGlobalScope/navigator)
:   Returns an instance of the WorkerNavigator interface, which represents the identity and state of the user agent (the client).

[onerror](/apis/workers/WorkerGlobalScope/onerror)
:   An event listener to be called when an error occurs.

[onoffline](/apis/workers/WorkerGlobalScope/onoffline)
:   An event listener to be called when the worker goes offline.

[ononline](/apis/workers/WorkerGlobalScope/ononline)
:   An event listener to be called when the worker goes online.

[self](/apis/workers/WorkerGlobalScope/self)
:   Returns the WorkerGlobalScope object.

## <span>Methods</span>

API Name
:   Summary

[close](/apis/workers/WorkerGlobalScope/close)
:   Discards any pending tasks and immediately closes the worker.

[importScripts](/apis/workers/WorkerGlobalScope/importScripts)
:   Fetches one or more script resources, identified by absolute URLs.

## <span>Events</span>

*No events.*

## <span>Notes</span>

The **WorkerGlobalScope** object is accessed by using the **self** or **this** property and is accessed only inside a worker. A worker has the following functionality within its scope:

-   It can use the **XMLHttpRequest** method.
-   It has a **self** property, which contains a reference to the worker object.
-   It can call all global JavaScript core methods.
-   It has a **navigator** object, which provides the **appName**, **appVersion**, **onLine**, **userAgent**, and **platform** properties but no others.
-   The **location** property creates the **WorkerLocation** object, which contains URL information on the worker's location. This property is similar to the **Window.location** property, but is read-only.
-   It supports the worker versions of the **setTimeout**, **setInterval**, **clearTimeout**, and **clearInterval** methods, which are similar to the methods of the same name for the **Window** object.
-   It can load other JavaScript files into the scope of the worker using the **importScripts** method.

Workers do not have access to the Document Object Model (DOM), nor the **window**, **document**, and **parent** objects. To terminate a worker thread from inside, use the **close** method. From the main document, use the **terminate** method to terminate the worker thread. You can send messages to the main document using **postMessage** and receive messages from the main document using the **onmessage** message handler. You can create new child workers from inside a worker. They must all run in the same host and their location depends on the parent worker of the new worker, not the original webpage. Because a new worker is likely to be in a separate process, you shouldn't create too many workers at once. Also, because messages between workers and their parents are copies and not shared, too many workers can use up resources quickly.

## <span>Related specifications</span>

[W3C Web Workers Specification](http://dev.w3.org/html5/workers)
:   W3C Editor's Draft
