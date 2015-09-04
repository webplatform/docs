---
title: WorkerLocation
tags:
  0: API
  1: Objects
  3: Webworkers
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'An object representing an absolute URL, set at the worker''s creation.'
uri: apis/workers/WorkerLocation

---
# WorkerLocation

## Summary

An object representing an absolute URL, set at the worker's creation.

## Properties

API Name
:   Summary
[href](/apis/workers/WorkerLocation/href)
:   Returns the absolute URL that the object represents.

## Methods

*No methods.*

## Events

*No events.*

## Notes

The **WorkerLocation** object is created by using the **self.location** method inside a worker thread. The **self** object is a reference to the **WorkerGlobalScope** object. The **href** property contains the absolute URL of the worker at its creation.

## Related specifications

Specification
:   Status
[W3C Web Workers Specification](http://dev.w3.org/html5/workers)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

