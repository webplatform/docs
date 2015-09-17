---
title: 'websocket API'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'WebSocket is a JavaScript API and accompanying protocol that allows you to create &quot;web sockets&quot;, capable of bi-directional full-duplex communication over a persistent TCP connection (socket).'
tags:
  - API_Listings
  - API
  - WebSocket
uri: apis/websocket

---
## Summary

WebSocket is a JavaScript API and accompanying protocol that allows you to create &quot;web sockets&quot;, capable of bi-directional full-duplex communication over a persistent TCP connection (socket).

[CloseEvent](/apis/websocket/CloseEvent)
:   Object representing the close event for a WebSocket.

[WebSocket Object API Details](/apis/websocket/WebSocket)
:   Object for creating and managing a WebSocket connection to a server, as well as for sending and receiving data on the connection.

## Usage

     Writing a WebSocket application in JavaScript is quite simple. Establish a connection, and hook into the open, error, message and close events as necessary. Remember, WebSocket is subject to the same-origin policy, like AJAX. This means if you want to test your client locally, you'll need to run a web server (e.g., python -m SimpleHTTPServer or php -S localhost:8000). Here's a simple example client that should work in newer browsers:

``` js
  var socket = new WebSocket('ws://localhost:8080/');
  socket.onopen = function () {
      console.log('Connected!');
  };
  socket.onmessage = function (event) {
      console.log('Received data: ' + event.data);
      socket.close();
  };
  socket.onclose = function () {
      console.log('Lost connection!');
  };
  socket.onerror = function () {
      console.log('Error!');
  };
  socket.send('hello, world!');
```

 And to complement it, here's an example echo server in Python using Twisted:

```
  from twisted.internet import protocol, reactor
  from txws import WebSocketFactory

  class Echo(protocol.Protocol):
      def dataReceived(self, data):
          self.transport.write(data)

  class EchoFactory(protocol.Factory):
      def buildProtocol(self, addr):
          return Echo()

  reactor.listenTCP(8080, WebSocketFactory(EchoFactory()))
  reactor.run()
```

## Notes

Like standard HTTP, WebSocket by default uses port 80 in the clear and 443 over SSL. The WebSocket client establishes an HTTP connection and requests to switch the protocol using the HTTP Upgrade mechanism, and then follows a handshake protocol to ensure both client and server support WebSocket. Because WebSocket connections start off as HTTP, WebSocket can work through many existing proxies and firewalls, unlike some other protocols.

Once the connection is established, messages are sent as "frames", in either text or binary format, in both directions. These are the data strings you send and receive in JavaScript.

WebSocket URIs have the same basic format as HTTP URIs, but with a different URI scheme: ws://hostname:port/path, e.g. ws://example.com/echo or ws://example.net:8080. The path can be used to distinguish the purpose of the connection; however, some servers ignore it. Secure WebSocket (WebSocket over SSL/TLS) URIs begin with wss:// instead of ws://.

## See also

### External resources

-   <http://tools.ietf.org/html/rfc6455> - IETF WebSocket protocol
-   <http://www.w3.org/TR/websockets/> - W3C WebSocket API
-   <http://www.websocket.org/echo.html> - WebSocket echo test
-   <http://caniuse.com/#search=websockets> - Browser support
-   <http://ajf.me/websocket/> - Has a list of libraries and frameworks for most popular programming languagess
-   <http://www.html5rocks.com/en/tutorials/websockets/basics/> - Good tutorial by html5rocks
