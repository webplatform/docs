---
title: WebSocket
tags:
  0: API
  1: Objects
  3: WebSocket
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Object for creating and managing a WebSocket connection to a server, as well as for sending and receiving data on the connection.'
uri: apis/websocket/WebSocket

---
# WebSocket Object API Details

## Summary

Object for creating and managing a WebSocket connection to a server, as well as for sending and receiving data on the connection.

## Properties

API Name
:   Summary
[binaryType](/apis/websocket/WebSocket/binaryType)
:   Indicates the type of binary data being transmitted by the connection.
[bufferedAmount](/apis/websocket/WebSocket/bufferedAmount)
:   The number of bytes of data that have been queued using calls to send() but not yet transmitted to the network.
[extensions](/apis/websocket/WebSocket/extensions)
:   The extensions selected by the server.
[onclose](/apis/websocket/WebSocket/onclose)
:   An event listener to be called when the WebSocket connection's readyState changes to CLOSED. Receives a [CloseEvent](/apis/websocket/CloseEvent) named "close".
[onerror](/apis/websocket/WebSocket/onerror)
:   An event listener to be called when an error occurs. Receives an event named "error".
[onmessage](/apis/websocket/WebSocket/onmessage)
:   An event listener to be called when a message is received from the server. Receives a MessageEvent named "message".
[onopen](/apis/websocket/WebSocket/onopen)
:   An event listener to be called when the WebSocket connection's readyState changes to OPEN. Receives an event named "open".
[protocol](/apis/websocket/WebSocket/protocol)
:   Indicates the name of the sub-protocol the server selected.
[readyState](/apis/websocket/WebSocket/readyState)
:   The current state of the connection, represented as a numeric constant.
[url](/apis/websocket/WebSocket/url)
:   The absolute URL as resolved by the constructor.

## Methods

API Name
:   Summary
[close](/apis/websocket/WebSocket/close)
:   Closes the WebSocket connection or connection attempt, if any.
[send](/apis/websocket/WebSocket/send)
:   Transmits data to the server over the WebSocket connection.

## Events

*No events.*

## Examples

The following function can be used to detect WebSocket support.

``` {.js}


function webSocketSupported() {
  return "WebSocket" in window;
}
```

</pre>

WebSockets are created via the WebSocket() constructor function.

``` {.js}


WebSocket( url[, protocols] )
```

</pre>

Complete example

``` {.js}


if (window["WebSocket"]) {
        conn = new WebSocket("ws://localhost:12345/wsendpoint", "myProtocol");
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
```

</pre>

## Usage

     Use the WebSocket API to interface with the WebSocket protocol (RFC 6455). When you create a WebSocket connection, you upgrade the HTTP protocol to the WebSocket protocol during the initial handshake between the client and the server. You can use the WebSocket API to program your client to initiate the WebSocket handshake.

The first argument in the WebSocket constructor is the URL of the server to which you want to connect your client; the second argument is an optional argument where you can specify a subprotocol you want your client to use over WebSocket, when communicating with the server. The server must be WebSocket-enabled. When the client sends the WebSocket connection request to the server, the server acknowledges that it can speak WebSocket, and chooses the one (and only one) subprotocol to use on top of WebSocket. For example, a chat client might use XMPP over WebSocket, and therefore choose XMPP as the subprotocol.

    When a WebSocket is constructed, it immediately attempts to connect to the given URL. There is no way to prevent or postpone the connection attempt. After construction, the WebSocket’s URL is accessible via its url property.

## Notes

The WebSocket API specification defines two URI schemes, ws:// and wss://, foWebSocket Object r unencrypted and encrypted connections, respectively. For example, you could create a new WebSocket connection with the string "ws://example.com:1234/resource". The URL specifies the host to connect to, the port, and (optionally) the protocols you want to use.

**Note**  Secure connections (wss://) use WebSocket with TLS, and are recommended in most cases because they are more likely to work with proxy servers, which can buffer unencrypted traffic and close long-lived WebSocket connections without warning. WebSocket connections are bidirectional; communication can flow in either direction without specific requests and responses. Data can be text or binary.

To open a use a WebSocket connection, you must follow this procedure:

-   Create a WebSocket connection with a specific URL and one or more optional subprotocols, such as "chat". You can use the *url* property to see how the URL was parsed.
-   Determine the state of the connection with the *readyState* property. This state will change as the communication proceeds.
-   Check the type of data that will be sent using the *binaryType*, *protocol*, and *extensions* properties.
-   Set up event handlers for the connection. Event handlers include **onopen**, **onmessage**, **onerror**, and **onclose**. Use **addEventListener** to listen for events and **removeEventListener** when you no longer want to listen.
-   Send data to the host using the **send** method.
-   Determine the rate at which your data is moving with the *bufferedAmount* property.
-   Check to see whether data was sent to you.
-   Close the connection when you are finished with the **close** method.

## Related specifications

Specification
:   Status
[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation

## See also

### External resources

-   [How to Use WebSockets by Colin Ihrig](http://cjihrig.com/blog/how-to-use-websockets/)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/WebSocket)

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

}

 }

 }

}}}