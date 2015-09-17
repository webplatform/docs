---
title: 'XMLHttpRequest'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
  - 'Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/en/tutorials/cors/)'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'XMLHttpRequest allows JavaScript to make HTTP requests, and is the most basic part of AJAX. It allows a website to dynamically request more content, without reloading the entire page.'
tags:
  - API_Objects
  - XHR
uri: apis/xhr/XMLHttpRequest

---
## Summary

XMLHttpRequest allows JavaScript to make HTTP requests, and is the most basic part of AJAX. It allows a website to dynamically request more content, without reloading the entire page.

## Overview

The **XMLHttpRequest** property is available on the **window** object.

    var xhr = new XMLHttpRequest();

With the **XMLHttpRequest** object, clients can make HTTP requests to a URL without reloading the entire page. Despite the term "XML" in the name, this object can be used to retrieve any type of data.

## Properties

[readyState](/apis/xhr/XMLHttpRequest/readyState)
:   Returns the current state of the XMLHttpRequest.

[response](/apis/xhr/XMLHttpRequest/response)
:   Returns the response entity body, which is the fragment of the entity body of the response received so far (if LOADING) or the complete entity body of the response (if DONE).

[responseText](/apis/xhr/XMLHttpRequest/responseText)
:   Returns the text response entity body, a string representing the response entity body, which is the fragment of the entity body of the response received so far (if LOADING) or the complete entity body of the response (if DONE).

[responseType](/apis/xhr/XMLHttpRequest/responseType)
:   Returns or sets the format the response will be returned in.

[responseXML](/apis/xhr/XMLHttpRequest/responseXML)
:   Returns the response to the request as a DOM Document object, or null if the request was unsuccessful, has not yet been sent, or cannot be parsed as XML or HTML.

[status](/apis/xhr/XMLHttpRequest/status)
:   Returns the HTTP result code (status) of the response to the request.

[statusText](/apis/xhr/XMLHttpRequest/statusText)
:   Returns the HTTP status text.

[timeout](/apis/xhr/XMLHttpRequest/timeout)
:   Returns or sets the number of milliseconds a request can take before automatically being terminated.

[upload](/apis/xhr/XMLHttpRequest/upload)
:   Returns the associated XMLHttpRequestUpload object. It can be used to gather transmission information when data is transferred to a server.

[withCredentials](/apis/xhr/XMLHttpRequest/withCredentials)
:   Returns or sets whether cross-site Access-Control requests should be made using credentials such as cookies or authorization headers.

## Methods

[abort](/apis/xhr/XMLHttpRequest/abort)
:   Stops an asynchronous XMLHttpRequest in progress.

[getAllResponseHeaders](/apis/xhr/XMLHttpRequest/getAllResponseHeaders)
:   Returns all the response headers as a string, or null if no response has been received.

[getResponseHeader](/apis/xhr/XMLHttpRequest/getResponseHeader)
:   Returns the string containing the text of the specified header, or null if the response has not been received or the header does not exist.

[open](/apis/xhr/XMLHttpRequest/open)
:   Initializes an XMLHttpRequest.

[overrideMimeType](/apis/xhr/XMLHttpRequest/overrideMimeType)
:   Overrides the MIME type returned by the server.

[send](/apis/xhr/XMLHttpRequest/send)
:   Initiates the request defined by the XMLHttpRequest.

[setRequestHeader](/apis/xhr/XMLHttpRequest/setRequestHeader)
:   Sets the value of an XMLHttpRequest header.

## Events

[abort](/apis/xhr/XMLHttpRequest/abort-event)
:   When the request has been aborted. For instance, by invoking the abort() method.

[error](/apis/xhr/XMLHttpRequest/error)
:   When the request has failed.

[load](/apis/xhr/XMLHttpRequest/load)
:   When the request has successfully completed.

[loadend](/apis/xhr/XMLHttpRequest/loadend)
:   When the request has completed (either in success or failure).

[loadstart](/apis/xhr/XMLHttpRequest/loadstart)
:   When the request starts.

[progress](/apis/xhr/XMLHttpRequest/progress)
:   While sending and loading data.

[readystatechange](/apis/xhr/XMLHttpRequest/readystatechange)
:   Fires whenever the readyState of the request changes. Mostly used to determine whether the body of the response is available for handling.

[timeout](/apis/xhr/XMLHttpRequest/timeout-event)
:   When the author specified timeout has passed before the request could complete.

## Examples

The following script demonstrates how to create and use the **XMLHttpRequest** object. For best client-side performance, the request is asynchronous and uses an **onreadystatechange** event handler to process the data returned by the call.

``` js
function handler() {
  if (xhr.readyState === 4 /* complete */) {
    if (xhr.status === 200) {
            console.log(xhr.responseText);
        }
    }
}
var xhr = new XMLHttpRequest();
xhr.open("GET", "http://localhost/test.xml", true);
xhr.onreadystatechange = handler;
xhr.send();
```

This script demonstrates how to access resources that sits on a different domain. Example: siteA.com gets resource from siteB.com

``` js
// Create the XHR object.
function createCORSRequest(method, url) {
  var xhr = new XMLHttpRequest();
  if ("withCredentials" in xhr) {
    // XHR for Chrome/Firefox/Opera/Safari.
    xhr.open(method, url, true);
  } else if (typeof XDomainRequest != "undefined") {
    // XDomainRequest for IE 9 and earlier.
    xhr = new XDomainRequest();
    xhr.open(method, url);
  } else {
    // CORS not supported.
    xhr = null;
  }
  return xhr;
}

// Helper method to parse the title tag from the response.
function getTitle(text) {
  return text.match('<title>(.*)?</title>')[1];
}

// Make the actual CORS request.
function makeCorsRequest() {
  // All HTML5 Rocks properties support CORS.
  var url = 'http://updates.html5rocks.com';

  var xhr = createCORSRequest('GET', url);
  if (!xhr) {
    alert('CORS not supported');
    return;
  }

  // Response handlers.
  xhr.onload = function() {
    var text = xhr.responseText;
    var title = getTitle(text);
    alert('Response from CORS request to ' + url + ': ' + title);
  };

  xhr.onerror = function() {
    alert('Woops, there was an error making the request.');
  };

  xhr.send();
}
```

## Usage

     The XMLHttpRequest object can be used to make either same-origin or cross-origin requests.

Same-origin requests are subject to the browser's same-origin policy: <http://en.wikipedia.org/wiki/Same_origin_policy> This basically says that an XMLHttpRequest instance can make a request to a resource that lives on the same origin as the calling page.

Requests that go across origins (for example, a request from originA.com to originB.com) can also be made. But in order for them to work, the destination server must support Cross-Origin Resource Sharing (CORS, <http://www.w3.org/TR/cors/>). These are a set of headers included in the response that indicate how a resource can be accessed across domains.

## Related specifications

[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft

[Cross-Origin Resource Sharing](http://www.w3.org/TR/cors/)
:   W3C Candidate Recommendation 29 January 2013

## See also

### Related articles

#### XHR

-   [XMLHttpRequest (XHR) API](/apis/xhr)

-   **XMLHttpRequest**

-   [FormData](/dom/FormData)

-   [MSEPrimer](/tutorials/MSEPrimer)

-   [file xhr](/tutorials/file_xhr)
