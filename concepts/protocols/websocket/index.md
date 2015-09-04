---
title: websocket
tags:
  - Basic
  - Pages
  - Web
  - Services
  - WebSocket
readiness: 'Almost Ready'
summary: 'A WebSocket is a persistent, low-latency, lightweight and two-way communication channel between the server and the browser.'
uri: concepts/protocols/websocket

---
# WebSockets concepts

## Summary

A WebSocket is a persistent, low-latency, lightweight and two-way communication channel between the server and the browser.

## What is a WebSocket?

The web we know today is built on top of HTTP, which is by design a stateless, one-off request/response-based protocol to reduce server load. But web applications have become more interactive thanks to [XMLHttpRequest](/apis/xhr/XMLHttpRequest), giving rise to multiplayer games, online chat applications and more. These new types of applications require low-latency and two-way communication between the server and the browser. Hence WebSockets: a secure socket implementation that is a persistent, two-way, lightweight communication channel, on top of existing HTTP. The protocol allows cross-origin requests by means of [CORS](/tutorials/using_cors).

## Getting Started

To create a WebSocket connection, you need to call the `WebSocket` constructor with the URL to the WebSocket service:

``` {.js}
    var connection = new WebSocket('ws://html5rocks.websocket.org/echo');
    // Just creating the object is enough to get connected.
```

 Although WebSockets are built on top of HTTP, they require different handling due to the major depart from the one-off nature of HTTP. This is why WebSocket URL's have a different protocol: `ws` instead of `http` and `wss` instead of `https`. They also require a special handshake triggered by the [| HTTP Upgrade Header](http://en.wikipedia.org/wiki/HTTP/1.1_Upgrade_header) which sometimes get stripped by certain proxies, causing the connection to fail.

WebSocket objects provide `onmessage` event to get the messages from the socket asynchronously and a non-blocking `send` method:

``` {.js}
// Log messages from the server
connection.onmessage = function (e) {
  console.log('Server says: ' + e.data);
};

// Send message to the server
connection.send('Hello there!');
```

 A WebSocket is not usable until connected and the object provides three more events to get notified about these state changes and provides a `readyState` property that reflects its current state:

``` {.js}
connection.onopen = function () {
  console.log('WS connection established.');
  // This means it is connected now.
  console.log(connection.readyState); // 1 - OPEN (from 0)
};

// Log errors
connection.onerror = function (error) {
  console.log('WebSocket connection failed:' + error);
  // This means the connection failed.
  console.log(connection.readyState); // 3 - CLOSED (probably from 0)
};

connection.onclose = function () {
  console.log('WS connection closed.');
  // This means the connection closed.
  console.log(connection.readyState); // 3 - CLOSED
};
```

## Data Types and Extensions

WebSockets support sending binary messages, too. To send binary data, one can use either `Blob` or `ArrayBuffer` object. Instead of calling the `send` method with string, you can simply pass an `ArrayBuffer` or a `Blob`.

``` {.js}
  // Sending file as Blob
  var file = document.querySelector('input[type="file"]').files[0];
  connection.send(file);
```

 To receive binary data, the `binaryType` attribute of the WebSocket object should be set to either `'blob'` or `'arraybuffer'`.

``` {.js}
  // Setting binaryType to accept received binary as either 'blob' or 'arraybuffer'
  connection.binaryType = 'arraybuffer';
  connection.onmessage = function(e) {
      console.log(e.data.byteLength); // ArrayBuffer object if binary
  };
```

 Extensions are also possible for the protocol such as "per frame compression". These are handled automatically between the browser and the server though so the only thing exposed on the object is the list of extensions that are in use.

``` {.js}
// Determining accepted extensions
console.log(connection.extensions);
```

## Notes

WebSockets is a relatively low level API that especially aims to be a two-way communication channel so it is most appropriate to use in applications that explicitly require two-way real-time communication, such as multiplayer games, chat, real-time text editors, etc. If one needs to get real-time updates from a server but does not need to send anything back such as getting stock information in real-time, [EventSource (Server-Sent Events)](/tutorials/eventsource_basics) should be considered.

## Usage

     * Online multiplayer games

-   Chat applications
-   Online collaborative applications

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from HTML5Rocks!.

