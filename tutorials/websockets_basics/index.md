---
title: websockets basics
tags:
  - Tutorials
  - Web
  - Services
readiness: 'Ready to Use'
summary: 'An introduction to WebSocket.'
uri: 'tutorials/websockets basics'

---
# Using WebSocket

**By [Malte Ubi and Eiji Kitamura](http://www.html5rocks.com/profiles/#malteubl)**
Originally published Oct 20, 2010

## Summary

An introduction to WebSocket.

## The Problem: Low Latency Client-Server and Server-Client Connections

The Web has been largely built around the so-called request/response paradigm of HTTP. A client loads up a web page and then nothing happens until the user clicks onto the next page. Around 2005, AJAX started to make the Web feel more dynamic. Still, all HTTP communication was steered by the client, which required either user interaction or periodic polling to load new data from the server.

Technologies that enable the server to send data to the client in the very moment when it knows that new data is available have been around for quite some time. They go by names such as "Push" or ["Comet"](http://en.wikipedia.org/wiki/Comet_(programming)). One of the most common hacks to create the illusion of a server-initiated connection is called *long polling*. With long polling, the client opens an HTTP connection to the server, which keeps it open until sending a response. Whenever the server actually has new data it sends the response. Other techniques involve [Flash](http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/3/flash/net/Socket.html), [XHR multipart](http://cometdaily.com/2007/12/27/a-standards-based-approach-to-comet-communication-with-rest/) requests, and so-called [htmlfiles](http://cometdaily.com/2007/10/25/http-streaming-and-internet-explorer/). Long polling and the other techniques work quite well. You use them every day in applications such as GMail chat.

However, all of these workarounds share one problem: they carry the overhead of HTTP, which doesn't make them well suited for low latency applications. Think multiplayer first-person shooter games in the browser or any other online game with a real-time component.

## Introducing WebSocket: Bringing Sockets to the Web

WebSocket is comprised of an [API](http://dev.w3.org/html5/websockets/) that enables you interact with a [protocol](http://tools.ietf.org/html/rfc6455) to create "socket" connections between a web browser and a server. In essence, there is a persistent, full-duplex connection between the client and the server, and both parties can send data at any time.

## Getting Started

In this example, we'll use a publicly available WebSocket server ([WebSockets.org](http://websockets.org)). You open up a WebSocket connection to this server simply by calling the WebSocket constructor:

``` {.js}
 var connection = new WebSocket('ws://html5rocks.websocket.org/echo', ['soap', 'xmpp']);
```

 Notice the `ws:` prefix, which the new URL schema for WebSocket connections. You can alternatively use `wss:` for secure WebSocket connections (WebSocket over TLS), used in the same way as `https:` is used for secure HTTP connections.

Immediately attaching event handlers to the connection allows you to know when the connection is opened, received incoming messages, or if there is an error.

The second argument, protocol, accepts optional subprotocols. The [WebSocket Protocol](http://tools.ietf.org/html/rfc6455) refers to protocols that you can use over WebSocket as subprotocols. This argument can be a string or an array of strings. Each string should represent a subprotocol name, and the server accepts only one of passed subprotocols in the array. The accepted subprotocol can be determined by accessing the `protocol` property of WebSocket object.

The subprotocol names must be one of the registered subprotocol names in the [IANA registry](http://www.iana.org/assignments/websocket/websocket.xml).

``` {.js}
 // When the connection is open, send some data to the server
 connection.onopen = function () {
   connection.send('Ping'); // Send the message 'Ping' to the server
 };

 // Log errors
 connection.onerror = function (error) {
   console.log('WebSocket Error ' + error);
 };

 // Log messages from the server
 connection.onmessage = function (e) {
   console.log('Server: ' + e.data);
 };
```

### Communicating with the Server

Once the connection is established to the server (when the `open` event is fired) we can start sending data to the server using the `send('your message')` method on the connection object. In the past, this method supported only strings, the latest spec allows you to send binary messages, as well. To send binary data, you can use either the `Blob` or the `ArrayBuffer` object.

``` {.js}
 // Sending a String
 connection.send('your message');

 // Sending canvas ImageData as ArrayBuffer
 var img = canvas_context.getImageData(0, 0, 400, 320);
 var binary = new Uint8Array(img.data.length);
 for (var i = 0; i < img.data.length; i++) {
   binary[i] = img.data[i];
 }
 connection.send(binary.buffer);

 // Sending a file as Blob
 var file = document.querySelector('input[type="file"]').files[0];
 connection.send(file);
```

 Similarly, the server might send us messages at any time. When this happens, the `onmessage` callback fires. The callback receives an event object and the actual message is accessible via the `data` property.

WebSocket can also receive binary messages in the latest spec. Binary frames can be received in `Blob` or `ArrayBuffer` format. To specify the format of the received binary, set the `binaryType` property of the WebSocket object to either `'blob'` or `'arraybuffer'`. The default format is `'blob'`. (You don't have to align the `binaryType` param on sending.)

``` {.js}
 // Setting binaryType to accept received binary as either 'blob' or 'arraybuffer'
 connection.binaryType = 'arraybuffer';
 connection.onmessage = function(e) {
   console.log(e.data.byteLength); // ArrayBuffer object if binary
 };
```

 Another newly added feature of WebSocket is extensions. Using extensions, it is possible to send frames [compressed](http://tools.ietf.org/html/draft-tyoshino-hybi-websocket-perframe-deflate-05), [multiplexed](http://tools.ietf.org/html/draft-tamplin-hybi-google-mux-02), etc. You can find server-accepted extensions by examining the `extensions` property of the WebSocket object after the `open` event. There is no officially published extensions spec (as of February 2012).

``` {.js}
 // Determining accepted extensions
 console.log(connection.extensions);
```

## Cross-Origin Communication

Being a modern protocol, cross-origin communication is baked right into WebSocket. While you should still make sure to only communicate with clients and servers you trust, WebSocket enables communication between parties on any domain. The server decides whether to make its service available to all clients or only to those that reside on a set of well-defined domains.

## Proxy Servers

Every new technology comes with a new set of problems. In the case of WebSocket it is the compatibility with proxy servers which mediate HTTP connections in most company networks. The WebSocket protocol uses the HTTP upgrade system (which is normally used for HTTP/SSL) to "upgrade" an HTTP connection to a WebSocket connection. Some proxy servers do not like this and will drop the connection. Thus, even if a given client uses the WebSocket protocol, it may not be possible to establish a connection. This makes the next section even more important :)

## Use WebSockets Today

WebSocket is still a young technology and not fully implemented in all browsers. However, you can use WebSocket today with libraries that use one of the fallbacks mentioned above whenever WebSocket is not available. A library that has become very popular in this domain is [socket.io](http://socket.io/), which comes with a client and a server implementation of the protocol and includes fallbacks (socket.io doesn't support binary messaging yet as of Februrary 2012). There are also commercial solutions such as [Kaazing](http://kaazing.com/), which provides WebSocket emulation, and [PusherApp](http://pusherapp.com/), which can be easily integrated into any web environment by providing an HTTP API to send WebSocket messages to clients. Due to the extra HTTP request, there will always be extra overhead compared to pure WebSocket.

## The Server Side

Using WebSocket creates a whole new usage pattern for server-side applications. While traditional server stacks such as LAMP are designed around the HTTP request/response cycle, they often do not deal well with a large number of open WebSocket connections. Keeping a large number of connections open at the same time requires an architecture that receives high concurrency at a low performance cost. Such architectures are usually designed around either threading or so-called non-blocking IO.

### Server-Side Implementations

-   Node.js
    -   [Socket.IO](http://socket.io/)
    -   [WebSocket-Node](https://github.com/Worlize/WebSocket-Node)
    -   [ws](https://github.com/einaros/ws)
-   Java
    -   [Kaazing](http://kaazing.com)
    -   [Jetty](http://www.eclipse.org/jetty/)
-   Ruby
    -   [EventMachine](http://github.com/igrigorik/em-websocket)
-   Python
    -   [pywebsocket](http://code.google.com/p/pywebsocket/)
    -   [Tornado](https://github.com/facebook/tornado)
-   Erlang
    -   [Shirasu](https://github.com/michilu/shirasu)
-   C++
    -   [libwebsockets](http://git.warmcat.com/cgi-bin/cgit/libwebsockets/)
-   .NET
    -   [SuperWebSocket](http://superwebsocket.codeplex.com/)

### Protocol Versions

The wire protocol (a handshake and the data transfer between client and server) for WebSocket is now [RFC 6455](http://tools.ietf.org/html/rfc6455). You can still use older protocol versions but it is not recommended because they are known to be vulnerable. If you have server implementations for older versions of WebSocket protocol, we recommend you upgrade to the latest version.

## Use Cases

Use WebSocket whenever you need a truly low latency, near real-time connection between the client and the server. Keep in mind that this might involve rethinking how you build your server side applications with a new focus on technologies such as event queues. Some example use cases are:

-   Multiplayer online games
-   Chat applications
-   Live sports ticker
-   Realtime updating social streams

## Demos

-   [Plink](http://labs.dinahmoe.com/plink/)
-   [Paint With Me](http://paintwith.me/)
-   [Pixelatr](http://connorhd.co.uk/project/pixelatr/)
-   [Dashed](http://www.dashed.com/)
-   [Racer with iPhone RC](http://demo.kaazing.com/racer)
-   [Massively multiplayer online crossword](http://scrabb.ly/)
-   [Ping server](http://www.websockets.org/echo.html) (used in examples above)
-   [HTML5demos sample](http://html5demos.com/web-socket)

## References

-   [The WebSocket API](http://dev.w3.org/html5/websockets/)
-   [RFC 6455 - The WebSocket Protocol](http://tools.ietf.org/html/rfc6455)
-   [The WebSocket Protocol Draft](http://tools.ietf.org/html/draft-ietf-hybi-thewebsocketprotocol-03)
-   [WebSockets - MDN](https://developer.mozilla.org/en/WebSockets)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/en/tutorials/websockets/basics/)

