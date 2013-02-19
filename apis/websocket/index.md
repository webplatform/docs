{{Page_Title|websocket API}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|WebSocket is a JavaScript API and accompanying protocol that allows you to create "web sockets", capable of bi-directional full-duplex communication over a persistent TCP connection (socket).}}
{{API_Listing|Use_page_title=No
|List_all_subpages=Yes
}}
{{Concept_Listing
|Query=[[Category:WebSocket]][[Category:API_Objects]]
|Use_page_title=No
|List_all_subpages=No
}}
{{Notes_Section
|Usage=Writing a WebSocket application in JavaScript is quite simple. Establish a connection, and hook into the open, error, message and close events as necessary. Remember, WebSocket is subject to the same-origin policy, like AJAX. This means if you want to test your client locally, you'll need to run a web server (e.g., python -m SimpleHTTPServer or php -S localhost:8000). Here's a simple example client that should work in newer browsers:

<syntaxhighlight lang="javascript">
  var socket = new WebSocket('ws://localhost:8080/');
  socket.onopen = function () {
      alert('Connected!');
  };
  socket.onmessage = function (event) {
      alert('Received data: ' + event.data);
      socket.close();
  };
  socket.onclose = function () {
      alert('Lost connection!');
  };
  socket.onerror = function () {
      alert('Error!');
  };
  socket.send('hello, world!');
</syntaxhighlight>

And to complement it, here's an example echo server in Python using Twisted:

<syntaxhighlight lang="python">
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
</syntaxhighlight>
|Notes=Like standard HTTP, WebSocket by default uses port 80 in the clear and 443 over SSL. The WebSocket client establishes an HTTP connection and requests to switch the protocol using the HTTP Upgrade mechanism, and then follows a handshake protocol to ensure both client and server support WebSocket. Because WebSocket connections start off as HTTP, WebSocket can work through many existing proxies and firewalls, unlike some other protocols.

Once the connection is established, messages are sent as "frames", in either text or binary format, in both directions. These are the data strings you send and receive in JavaScript.

WebSocket URIs have the same basic format as HTTP URIs, but with a different URI scheme: ws://hostname:port/path, e.g. ws://example.com/echo or ws://example.net:8080. The path can be used to distinguish the purpose of the connection; however, some servers ignore it. Secure WebSocket (WebSocket over SSL/TLS) URIs begin with wss:// instead of ws://.
}}
{{See_Also_Section
|External_links=* http://tools.ietf.org/html/rfc6455 - IETF WebSocket protocol
* http://www.w3.org/TR/websockets/ - W3C WebSocket API
* http://www.websocket.org/echo.html - WebSocket echo test
* http://caniuse.com/#search=websockets - Browser support
* http://ajf.me/websocket/ - Has a list of libraries and frameworks for most popular programming languagess
* http://www.html5rocks.com/en/tutorials/websockets/basics/ - Good tutorial by html5rocks
}}
{{Topics|API, WebSocket}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}
[[Category:API_Listings]]