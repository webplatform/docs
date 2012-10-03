{{Page_Title|Introducing web sockets}}
{{Flags
|High-level issues=Needs Flags
}}
{{Byline}}
{{Summary_Section|An introduction to WebSocket.}}
{{Tutorial
|Content===The Problem: Low Latency Client-Server and Server-Client Connections==

The Web has been largely built around the so-called request/response paradigm of HTTP. A client loads up a web page and then nothing happens until the user clicks onto the next page. Around 2005, AJAX started to make the Web feel more dynamic. Still, all HTTP communication was steered by the client, which required either user interaction or periodic polling to load new data from the server.

Technologies that enable the server to send data to the client in the very moment when it knows that new data is available have been around for quite some time. They go by names such as "Push" or [http://en.wikipedia.org/wiki/Comet_(programming) "Comet"]. One of the most common hacks to create the illusion of a server-initiated connection is called ''long polling''. 
With long polling, the client opens an HTTP connection to the server, which keeps it open until sending a response. Whenever the server actually has new data it sends the response.
Other techniques involve [http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/3/flash/net/Socket.html Flash], [http://cometdaily.com/2007/12/27/a-standards-based-approach-to-comet-communication-with-rest/ XHR multipart] requests, and so-called [http://cometdaily.com/2007/10/25/http-streaming-and-internet-explorer/ htmlfiles]. Long polling and the other techniques work quite well. You use them every day in applications such as GMail chat.

However, all of these workarounds share one problem: they carry the overhead of HTTP, which doesn't make them well suited for low latency applications. Think multiplayer first-person shooter games in the browser or any other online game with a real-time component.

==Introducing WebSocket: Bringing Sockets to the Web==

WebSocket is comprised of an [http://dev.w3.org/html5/websockets/ API] that enables you interact with a [http://tools.ietf.org/html/rfc6455 protocol] to create "socket" connections between a web browser and a server. In essence, there is a persistent, full-duplex connection between the client and the server, and both parties can send data at any time.

==Getting Started==

In this example, we'll use a publicly available WebSocket server ([http://websockets.org WebSockets.org]). You open up a WebSocket connection to this server simply by calling the WebSocket constructor:

<pre>
 var connection = new WebSocket('ws://html5rocks.websocket.org/echo', ['soap', 'xmpp']);
</pre>

Notice the <code>ws:</code> prefix, which the new URL schema for WebSocket connections. You can alternatively use <code>wss:</code> for secure WebSocket connections (WebSocket over TLS), used in the same way as <code>https:</code> is used for secure HTTP connections.

Immediately attaching event handlers to the connection allows you to know when the connection is opened, received incoming messages, or if there is an error.

The second argument, protocol, accepts optional subprotocols. The [http://tools.ietf.org/html/rfc6455 WebSocket Protocol] refers to protocols that you can use over WebSocket as subprotocols. This argument can be a string or an array of strings. Each string should represent a subprotocol name, and the server accepts only one of passed subprotocols in the array. The accepted subprotocol can be determined by accessing the <code>protocol</code> property of WebSocket object.

The subprotocol names must be one of the registered subprotocol names in the [http://www.iana.org/assignments/websocket/websocket.xml IANA registry]. 

<pre>
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
</pre>

===Communicating with the Server===

Once the connection is established to the server (when the <code>open</code> event is fired) we can start sending data to the server using the <code>send('your message')</code> method on the connection object. In the past, this method supported only strings, the latest spec allows you to send binary messages, as well. To send binary data, you can use either the <code>Blob</code> or the <code>ArrayBuffer</code> object.

<pre>
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
</pre>

Similarly, the server might send us messages at any time. When this happens, the <code>onmessage</code> callback fires. The callback receives an event object and the actual message is accessible via the <code>data</code> property.

WebSocket can also receive binary messages in the latest spec. Binary frames can be received in <code>Blob</code> or <code>ArrayBuffer</code> format. To specify the format of the received binary, set the <code>binaryType</code> property of the WebSocket object to either <code>'blob'</code> or <code>'arraybuffer'</code>. The default format is <code>'blob'</code>. (You don't have to align the <code>binaryType</code> param on sending.)

<pre>
 // Setting binaryType to accept received binary as either 'blob' or 'arraybuffer'
 connection.binaryType = 'arraybuffer';
 connection.onmessage = function(e) {
   console.log(e.data.byteLength); // ArrayBuffer object if binary
 };
</pre>

Another newly added feature of WebSocket is extensions. Using extensions, it is possible to send frames [http://tools.ietf.org/html/draft-tyoshino-hybi-websocket-perframe-deflate-05 compressed], [http://tools.ietf.org/html/draft-tamplin-hybi-google-mux-02 multiplexed], etc. You can find server-accepted extensions by examining the <code>extensions</code> property of the WebSocket object after the <code>open</code> event. There is no officially published extensions spec (as of February 2012).

<pre>
 // Determining accepted extensions
 console.log(connection.extensions);
</pre>

==Cross-Origin Communication==

Being a modern protocol, cross-origin communication is baked right into WebSocket. While you should still make sure to only communicate with clients and servers you trust, WebSocket enables communication between parties on any domain. The server decides whether to make its service available to all clients or only to those that reside on a set of well-defined domains.

==Proxy Servers==

Every new technology comes with a new set of problems. In the case of WebSocket it is the compatibility with proxy servers which mediate HTTP connections in most company networks. The WebSocket protocol uses the HTTP upgrade system (which is normally used for HTTP/SSL) to "upgrade" an HTTP connection to a WebSocket connection. Some proxy servers do not like this and will drop the connection. Thus, even if a given client uses the WebSocket protocol, it may not be possible to establish a connection. This makes the next section even more important :)

==Use WebSockets Today==

WebSocket is still a young technology and not fully implemented in all browsers. However, you can use WebSocket today with libraries that use one of the fallbacks mentioned above whenever WebSocket is not available. A library that has become very popular in this domain is [http://socket.io/ socket.io], which comes with a client and a server implementation of the protocol and includes fallbacks (socket.io doesn't support binary messaging yet as of Februrary 2012). 
There are also commercial solutions such as [http://kaazing.com/ Kaazing], which provides WebSocket emulation, and [http://pusherapp.com/ PusherApp], which can be easily integrated into any web environment by providing an HTTP API to send WebSocket messages to clients. Due to the extra HTTP request, there will always be extra overhead compared to pure WebSocket.

==The Server Side==

Using WebSocket creates a whole new usage pattern for server-side applications. While traditional server stacks such as LAMP are designed around the HTTP request/response cycle, they often do not deal well with a large number of open WebSocket connections. Keeping a large number of connections open at the same time requires an architecture that receives high concurrency at a low performance cost. Such architectures are usually designed around either threading or so-called non-blocking IO.

===Server-Side Implementations===

* Node.js
** [http://socket.io/ Socket.IO]
** [https://github.com/Worlize/WebSocket-Node WebSocket-Node]
** [https://github.com/einaros/ws ws]
* Java
** [http://www.eclipse.org/jetty/ Jetty]
* Ruby
** [http://github.com/igrigorik/em-websocket EventMachine]
* Python
** [http://code.google.com/p/pywebsocket/ pywebsocket]
** [https://github.com/facebook/tornado Tornado]
* Erlang
** [https://github.com/michilu/shirasu Shirasu]
* C++
** [http://git.warmcat.com/cgi-bin/cgit/libwebsockets/ libwebsockets]
* .NET
** [http://superwebsocket.codeplex.com/ SuperWebSocket]

===Protocol Versions===

The wire protocol (a handshake and the data transfer between client and server) for WebSocket is now [http://tools.ietf.org/html/rfc6455 RFC 6455]. You can still use older protocol versions but it is not recommended because they are known to be vulnerable. If you have server implementations for older versions of WebSocket protocol, we recommend you upgrade to the latest version.

==Use Cases==

Use WebSocket whenever you need a truly low latency, near real-time connection between the client and the server. Keep in mind that this might involve rethinking how you build your server side applications with a new focus on technologies such as event queues. Some example use cases are:

* Multiplayer online games
* Chat applications
* Live sports ticker
* Realtime updating social streams

==Demos==

* [http://labs.dinahmoe.com/plink/ Plink]
* [http://paintwith.me/ Paint With Me]
* [http://connorhd.co.uk/project/pixelatr/ Pixelatr]
* [http://www.dashed.com/ Dashed]
* [http://scrabb.ly/ Massively multiplayer online crossword]
* [http://www.websockets.org/echo.html Ping server] (used in examples above)
* [http://html5demos.com/web-socket HTML5demos sample]

==References==

* [http://dev.w3.org/html5/websockets/ The WebSocket API]
* [http://tools.ietf.org/html/rfc6455 RFC 6455 - The WebSocket Protocol]
* [http://tools.ietf.org/html/draft-ietf-hybi-thewebsocketprotocol-03 The WebSocket Protocol Draft]
* [https://developer.mozilla.org/en/WebSockets WebSockets - MDN]
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Web Sockets
|Chrome_supported=Yes
|Chrome_version=20.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=12.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=6.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=Web Sockets
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_phone_supported=Unknown
|IE_phone_version=
|IE_phone_prefixed_supported=Unknown
|IE_phone_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=6.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Web Services}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/websockets/basics/
}}