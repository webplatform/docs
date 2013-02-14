{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The WebSocket object provides the API for creating and managing a WebSocket connection to a server, as well as for sending and receiving data on the connection.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following function can be used to detect WebSocket support.
|Code=<syntaxhighlight lang="javascript">
function webSocketSupported() {
  return "WebSocket" in window;
}
</syntaxhighlight>
}}{{Single Example
|Language=JavaScript
|Description=WebSockets are created via the WebSocket() constructor function.
|Code=<syntaxhighlight lang="javascript">
WebSocket( url[, protocols] )
</syntaxhighlight>
}}{{Single Example
|Language=JavaScript
|Description=Complete example
|Code=<syntaxhighlight lang="javascript">
if (window["WebSocket"]) {
        conn = new WebSocket("ws://localhost:12345/wsendpoint");
        conn.onclose = function(evt) {
            console.log("Connection closed.");
        }
        conn.onmessage = function(evt) {
            console.log(evt.data);
        }
    } else {
        console.log("Your browser does not support WebSockets");
    }
});
</syntaxhighlight>
}}
}}
{{Notes_Section
|Usage=The constructor’s first argument is the URL that the WebSocket will connect to.  When a WebSocket is constructed, it immediately attempts to connect to the given URL.  There is no way to prevent or postpone the connection attempt.  After construction, the WebSocket’s URL is accessible via its ''url'' property.
|Notes=The WebSocket API specification defines two URI schemes, ws:// and wss://, for unencrypted and encrypted connections, respectively. For example, you could create a new WebSocket connection with the string "ws://example.com:1234/resource". The URL specifies the host to connect to, the port, and (optionally) the protocols you want to use.

'''Note'''  Secure connections (wss://) are recommended in most cases because they are more likely to work with proxy servers, which can buffer unencrypted traffic and close long-lived WebSocket connections without warning.
WebSocket connections are bidirectional; communication can flow in either direction without specific requests and responses. Data can be text or binary.

To open a use a WebSocket connection, you must follow this procedure:
*Create a WebSocket connection with a specific URL and one or more optional subprotocols, such as "chat". You can use the ''url'' property to see how the URL was parsed.
*Determine the state of the connection with the ''readyState'' property. This state will change as the communication proceeds.
*Check the type of data that will be sent using the ''binaryType'', ''protocol'', and ''extensions'' properties.
*Set up  event handlers for the connection. Event handlers include '''onopen''', '''onmessage''', '''onerror''', and '''onclose'''. Use '''addEventListener''' to listen for events and '''removeEventListener''' when you no longer want to listen.
*Send data to the host using the '''send''' method.
*Determine the rate at which your data is moving with the ''bufferedAmount'' property.
*Check to see whether data was sent to you.
*Close the connection when you are finished with the '''close''' method.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C WebSocket Specification
|URL=http://www.w3.org/TR/websockets/
|Status=W3C Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|External_links=* [http://cjihrig.com/blog/how-to-use-websockets/ How to Use WebSockets by Colin Ihrig]
}}
{{Topics|WebSocket}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/WebSocket
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}
}






}






}





}}}