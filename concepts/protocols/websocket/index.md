{{Page_Title}}
{{Flags
|High-level issues=Stub
}}
{{Summary_Section|A WebSocket is a persistent, low-latency, lightweight and two-way communication channel between the server and the browser.}}
{{Basic Page}}
==What is a WebSocket?==

The web we know today is built on top of HTTP protocol which is by design a stateless, one-off request/response based protocol to reduce the load on the servers. Fast-forward to today and now web applications are much more interactive than that thanks to [[apis/xhr/XMLHttpRequest | XMLHttpRequest]] and we even see multiplayer games, online chat applications and much more. As one might guess, some of this new type of applications require low-latency and two-way communication between the servers and the browser. The solution to this need is WebSockets: a secure socket implementation, that is a persistent two-way lightweight communication channel, on top of existing HTTP protocol. The protocol allows cross-origin requests by means of [[tutorials/using_cors | CORS]].

==Getting Started==

To create a WebSocket connection, you need to call the <code>WebSocket</code> constructor with the URL to the WebSocket service:
<syntaxhighlight lang="javascript">
var connection = new WebSocket('ws://html5rocks.websocket.org/echo');
</syntaxhighlight>

Although WebSockets are based on top off HTTP, they require different handling due to the major depart from the one-off nature of HTTP. This is why WebSocket URL's have a different protocol: <code>ws</code> instead of <code>http</code> and <code>wss</code> instead of <code>https</code>. They also require a special handshake triggered by the [http://en.wikipedia.org/wiki/HTTP/1.1_Upgrade_header | HTTP Upgrade Header] which sometimes get stripped by certain proxies, causing the connection to fail.

WebSocket objects provide <code>onmessage</code> event to get the messages from the socket asynchronously and an unblocking <code>send</code> method:
<syntaxhighlight lang="javascript">
// Log messages from the server
connection.onmessage = function (e) {
  console.log('Server: ' + e.data);
};

connection.send('Hello there!');
</syntaxhighlight>

A WebSocket is not usable until gets connected and the object provides three more events to get notified about these state changes and provides a <code>readyState</code> property that reflects its current state:
<syntaxhighlight lang="javascript">
connection.onopen = function () {
  console.log('WS connection established.');
};

// Log errors
connection.onerror = function (error) {
  console.log('WebSocket connection failed:' + error);
};

connection.onclose = function () {
  console.log('WS connection closed.');
};
</syntaxhighlight>

==Data Types and Extensions==

WebSockets support sending binary messages too. To send binary data, one can use either <code>Blob</code> or <code>ArrayBuffer</code> object. Instead of calling the <code>send</code> method with string, you can simply pass an <code>ArrayBuffer</code> or a <code>Blob</code>.
<syntaxhighlight lang="javascript">
// Sending file as Blob
var file = document.querySelector('input[type="file"]').files[0];
connection.send(file);
</syntaxhighlight>

To receive data as binary <code>Blob</code> or <code>ArrayBufer</code> <code>binaryType</code> attribute of the object should be set to either <code>'blob'</code> or <code>'arraybuffer'</code>.
<syntaxhighlight lang="javascript">
// Setting binaryType to accept received binary as either 'blob' or 'arraybuffer'
connection.binaryType = 'arraybuffer';
connection.onmessage = function(e) {
  console.log(e.data.byteLength); // ArrayBuffer object if binary
};
</syntaxhighlight>

Extensions are also possible for the protocol such as "per frame compression". These are handled automatically between the browser and the server though so the only thing exposed on the object is the list of extensions that are in use.
<syntaxhighlight lang="javascript">
// Determining accepted extensions
console.log(connection.extensions);
</syntaxhighlight>

==Notes==

WebSockets is a relatively low level API that especially aims to be a two-way communication channel so it is most appropriate to use it in applications that explicitly require two way real-time communication such as a multiplayer game, chat, or real-time text editors etc. If one needs to get real-time updates from a server but don't need to send anything back such as getting stock information in real-time, he or she should consider using [[tutorials/eventsource_basics | EventSource (Server-Sent Events)]].
{{Notes_Section
|Usage=Online multiplayer games
Chat applications
Online collaborative applications
}}
{{Topics|Web Services, WebSocket}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}