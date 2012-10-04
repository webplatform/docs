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
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following script demonstrates how to create and use the '''XMLHttpRequest''' object. For best client-side performance, the XMLHTTP request is asynchronous and uses an [[apis/xhr/events/readystatechange|'''onreadystatechange''']] event handler to process the data returned by the call. The script uses the '''getXMLHttpRequest()''' function defined above to create the request object.
|LiveURL=
|Code=
function handler()
{
    if (oReq.readyState {{=}}{{=}} 4 /* complete */) {
        if (oReq.status {{=}}{{=}} 200) {
            console.log(oReq.responseText);
        }
    }
}
var oReq {{=}} getXMLHttpRequest();
if (oReq !{{=}} null) {
    oReq.open("GET", "http://localhost/test.xml", true);
    oReq.onreadystatechange {{=}} handler;
    oReq.send();
}
else {
    window.console.log("AJAX (XMLHTTP) not supported.");
}
}}
{{Single_Example
|Description=The following example demonstrates the same functionality in VBScript.
|LiveURL=
|Code=
&lt;script type{{=}}"text/vbscript"&gt;
Dim objXML
Function objXML_onreadystatechange()
    If (objXML.readyState {{=}} 4) Then
        If (objXML.status {{=}} 200) Then
            MsgBox objXML.responseText, 0, objXML.statusText
        End If
    End If
End Function
Function Window_onload()
    If IsObject(window.XmlHttpRequest) Then
        objXML {{=}} window.XmlHttpRequest
    Else
        Set objXML {{=}} CreateObject("MSXML2.XMLHTTP.3.0")
    End If
    objXML.Open "GET", "http://localhost/test.xml", True
    objXML.OnReadyStateChange {{=}} GetRef("objXML_onreadystatechange")
    objXML.Send
End Function
&lt;/script&gt; 
}}
{{Single_Example
|Description=In Internet Explorer 8, the VBScript syntax is not supported, which complicates native support detection somewhat. One way to detect Internet Explorer 8 is by using conditional comments. The following comment detects Internet Explorer 8 when it is not running in compatibility mode. The script sets a global variable that can be checked later when creating the '''XMLHttpRequest''' object.
|LiveURL=
|Code=
&lt;!--[if IE 8]&gt;&lt;script type{{=}}"text/vbscript"&gt;
vbIE8 {{=}} True
&lt;/script&gt;&lt;![endif]--&gt;
If Not vbIE8 And IsObject(window.XmlHttpRequest) Then ...
  
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''XMLHttpRequest''' property is available on the '''window''' object.
 <code>var oReq {{=}} new XMLHttpRequest;</code>
With the '''XMLHttpRequest''' object, clients can retrieve and submit XML data directly to a web server without reloading the document. To convert XML data into renderable HTML content, use the client-side XML DOM or Extensible Stylesheet Language Transformations (XSLT) to compose HTML elements for presentation.
The native scripting object also supports the use of expandos (custom properties), and properly recognizes the 'this' notation of JavaScript.
The '''XMLHttpRequest''' property is available on the '''window''' object in Windows Internet Explorer 7.
 <code>var oReq {{=}} new XMLHttpRequest;</code>
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
         catch(ex) {
             return null;
         }
     }
 }</code>
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203789 XMLHttpRequest], Section 3


===Members===
The '''XMLHttpRequest''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''XMLHttpRequest''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[apis/xhr/events/readystatechange|'''onreadystatechange''']]
|Sets or retrieves the event handler for asynchronous requests.
|-
|[[apis/xhr/events/timeout|'''ontimeout''']]
|Raised when there is an error that prevents the completion of the request.
|}
 

====Methods====
The '''XMLHttpRequest''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|'''abort'''
|Cancels the current HTTP request.
|-
|[[dom/methods/addEventListener|'''addEventListener''']]
|Registers an event handler for the specified event type.
|-
|[[dom/methods/dispatchEvent|'''dispatchEvent''']]
|Sends an event to the current element.
|-
|'''getAllResponseHeaders'''
|Returns the complete list of response headers.
|-
|'''getResponseHeader'''
|Returns the specified response header.
|-
|'''open'''
|Assigns method, destination URL, and other optional attributes of a pending request.
|-
|[[dom/methods/removeEventListener|'''removeEventListener''']]
|Removes an event handler that  the  [[dom/methods/addEventListener|'''addEventListener''']] method registered.
|-
|'''send'''
|Sends an HTTP request to the server and receives a response.
|-
|'''setRequestHeader'''
|Adds custom HTTP headers to the request.
|}
 

====Properties====
The '''XMLHttpRequest''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/constructor|'''constructor''']]
|Returns a reference to the constructor of an object.
|-
|'''readyState'''
|Retrieves the current state of the request operation.
|-
|[[apis/xhr/properties/response|'''response''']]
|Returns the response received from the server.
|-
|[[apis/xhr/properties/responseBody|'''responseBody''']]
|Retrieves the response body as an array of unsigned bytes. 

This property is not available for Metro style apps using JavaScript.
|-
|'''responseText'''
|Retrieves the response body as a string.
|-
|[[apis/xhr/properties/responseType|'''responseType''']]
|Describes the data type of the response associated with the request.
|-
|'''responseXML'''
|Retrieves the response body as an XML DOM object.
|-
|'''status'''
|Retrieves the HTTP status code of the request.
|-
|'''statusText'''
|Retrieves the friendly HTTP status of the request.
|-
|[[apis/xhr/properties/timeout|'''timeout''']]
|Gets or sets the time-out value.
|-
|[[apis/xhr/properties/withCredentials|'''withCredentials''']]
|Indicates whether user credentials should be included with the request.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}