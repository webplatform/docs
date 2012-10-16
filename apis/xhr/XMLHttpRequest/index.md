{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|XMLHttpRequest is the most basic part of AJAX. It allows a website to dynamically request more content, without loading the page.}}
{{API_Object
|Overview=The '''XMLHttpRequest''' property is available on the '''window''' object.
 <code>var xhr {{=}} new XMLHttpRequest();</code>
With the '''XMLHttpRequest''' object, clients can retrieve and submit XML data directly to a web server without reloading the document. To convert XML data into renderable HTML content, use the client-side XML DOM or Extensible Stylesheet Language Transformations (XSLT) to compose HTML elements for presentation.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following script demonstrates how to create and use the '''XMLHttpRequest''' object. For best client-side performance, the request is asynchronous and uses an [[apis/xhr/events/readystatechange|'''onreadystatechange''']] event handler to process the data returned by the call.
|Code=function handler() {
  if (xhr.readyState {{=}}{{=}} 4 /* complete */) {
    if (xhr.status {{=}}{{=}} 200) {
            console.log(xhr.responseText);
        }
    }
}
var xhr {{=}} new XMLHttpRequest();
xhr.open("GET", "http://localhost/test.xml", true);
xhr.onreadystatechange {{=}} handler;
xhr.send();
}}
}}
{{Notes_Section
|Notes=Windows Internet Explorer earlier than version 7 does not implement the native XMLHttpRequest object. The XMLHTTP ActiveX object emulates the same functionality. While the native XMLHttpRequest object also supports the use of expandos (custom properties) and properly recognizes the 'this' notation of JavaScript, the ActiveX version does not.
To support versions of Windows Internet Explorer prior to Internet Explorer 7, use the following function to get the '''XMLHttpRequest''' object.
 <code>function getXMLHttpRequest() 
 {
     if (window.XMLHttpRequest) {
         return new window.XMLHttpRequest;
     }
     else {
         try {
             return new ActiveXObject("MSXML2.XMLHTTP.3.0");
         }
         catch (ex) {
             return null;
         }
     }
 }</code>
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203789 XMLHttpRequest], Section 3


===Members===
The '''XMLHttpRequest''' object has these types of members:
*[[#Events|Events]]
*[[#Methods|Methods]]
*[[#Properties|Properties]]


====Events====
The '''XMLHttpRequest''' object has these events.
{{{!}} class="wikitable"
{{!}}-
!Event
!Description
{{!}}-
{{!}}[[apis/xhr/events/readystatechange{{!}}'''onreadystatechange''']]
{{!}}Sets or retrieves the event handler for asynchronous requests.
{{!}}-
{{!}}[[apis/xhr/events/timeout{{!}}'''ontimeout''']]
{{!}}Raised when there is an error that prevents the completion of the request.
{{!}}}
 

====Methods====
The '''XMLHttpRequest''' object has these methods.
{{{!}} class="wikitable"
{{!}}-
!Method
!Description
{{!}}-
{{!}}'''abort'''
{{!}}Cancels the current HTTP request.
{{!}}-
{{!}}[[dom/methods/addEventListener{{!}}'''addEventListener''']]
{{!}}Registers an event handler for the specified event type.
{{!}}-
{{!}}[[dom/methods/dispatchEvent{{!}}'''dispatchEvent''']]
{{!}}Sends an event to the current element.
{{!}}-
{{!}}'''getAllResponseHeaders'''
{{!}}Returns the complete list of response headers.
{{!}}-
{{!}}'''getResponseHeader'''
{{!}}Returns the specified response header.
{{!}}-
{{!}}'''open'''
{{!}}Assigns method, destination URL, and other optional attributes of a pending request.
{{!}}-
{{!}}[[dom/methods/removeEventListener{{!}}'''removeEventListener''']]
{{!}}Removes an event handler that  the  [[dom/methods/addEventListener{{!}}'''addEventListener''']] method registered.
{{!}}-
{{!}}'''send'''
{{!}}Sends an HTTP request to the server and receives a response.
{{!}}-
{{!}}'''setRequestHeader'''
{{!}}Adds custom HTTP headers to the request.
{{!}}}
 

====Properties====
The '''XMLHttpRequest''' object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}[[dom/properties/constructor{{!}}'''constructor''']]
{{!}}Returns a reference to the constructor of an object.
{{!}}-
{{!}}'''readyState'''
{{!}}Retrieves the current state of the request operation.
{{!}}-
{{!}}[[apis/xhr/properties/response{{!}}'''response''']]
{{!}}Returns the response received from the server.
{{!}}-
{{!}}[[apis/xhr/properties/responseBody{{!}}'''responseBody''']]
{{!}}Retrieves the response body as an array of unsigned bytes. 

This property is not available for Metro style apps using JavaScript.
{{!}}-
{{!}}'''responseText'''
{{!}}Retrieves the response body as a string.
{{!}}-
{{!}}[[apis/xhr/properties/responseType{{!}}'''responseType''']]
{{!}}Describes the data type of the response associated with the request.
{{!}}-
{{!}}'''responseXML'''
{{!}}Retrieves the response body as an XML DOM object.
{{!}}-
{{!}}'''status'''
{{!}}Retrieves the HTTP status code of the request.
{{!}}-
{{!}}'''statusText'''
{{!}}Retrieves the friendly HTTP status of the request.
{{!}}-
{{!}}[[apis/xhr/properties/timeout{{!}}'''timeout''']]
{{!}}Gets or sets the time-out value.
{{!}}-
{{!}}[[apis/xhr/properties/withCredentials{{!}}'''withCredentials''']]
{{!}}Indicates whether user credentials should be included with the request.
{{!}}}
 
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=XMLHttpRequest
|URL=http://www.w3.org/TR/XMLHttpRequest/
|Status=Work
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
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