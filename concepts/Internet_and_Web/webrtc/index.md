{{Page_Title|WebRTC}}
{{Flags}}
{{API_Name|RTCPeerConnection}}
{{Summary_Section|WebRTC implements open standards for real-time, plugin-free video, audio and data communication.}}
{{Concept_Page
|Content=== Real-time communication without plugins ==

<blockquote>WebRTC is a new front in the long war for an open and unencumbered web.<br />
 &mdash; [http://hacks.mozilla.org/2012/03/video-mobile-and-the-open-web/ Brendan Eich], inventor of JavaScript</blockquote>
Imagine a world where your phone, TV and computer could all communicate on a common platform. Imagine it was easy to add video chat to your web application. That's the vision of WebRTC.

Want to try it out? WebRTC is available now in Google Chrome and Firefox.

A good place to begin is the simple video chat application at [http://apprtc.appspot.com apprtc.appspot.com]:

# Open the page in Chrome (you don't need to set about:flags)
# Click the Allow button to let the app use your web cam.
# Open the URL displayed at the bottom of the page in a new tab or window or, better still, on a different computer.

There is a walkthrough of the code [[#toc-simple|later in this article]].

== Quick start ==

Haven't got time to read this article, or just want code?

# Get an overview of WebRTC from [http://www.youtube.com/watch?v=E8C8ouiXHHk|Justin Uberti's Google I/O video].
# If you haven't used getUserMedia, take a look at the [http://www.html5rocks.com/en/tutorials/getusermedia/intro/ HTML5 Rocks article] on the subject, and view the source for the simple example at [http://www.simpl.info/getusermedia simpl.info/gum] and [https://plus.sandbox.google.com/118075919496626375791/posts Eric Bidelman]'s [http://html5-demos.appspot.com/static/getusermedia/photobooth.html photobooth demo].
# Get to grips with the RTCPeerConnection API by reading through the [[#simpleRTCPeerConnectionExample|simple example below]] and the demo at [http://www.simpl.info/pc simpl.info/pc], which implements WebRTC on a single web page.
# Learn more about how WebRTC uses servers for signaling, data communication, firewall and NAT traversal, by reading through the code and the console logs from the video chat demo at [http://apprtc.appspot.com apprtc.appspot.com].

== A very short history of WebRTC ==

One of the last major challenges for the web is to enable human communication via voice and video: Real Time Communication, RTC for short. RTC should be as natural in a web application as entering text in a text input. Without it, we're limited in our ability to innovate and develop new ways for people to interact.

Historically, RTC has been corporate and complex, requiring expensive audio and video technologies to be licensed or developed in house. Integrating RTC technology with existing content, data and services has been difficult and time consuming, particularly on the web.

Gmail video chat became popular in 2008, and in 2011 Google introduced Hangouts, which use the Google Talk service (as does Gmail). Google bought GIPS, a company which had developed many components required for RTC, such as codecs and echo cancellation techniques. Google open sourced the technologies developed by GIPS and engaged with relevant standards bodies at the IETF and W3C to ensure industry consensus. In May 2011, Ericsson built [https://labs.ericsson.com/developer-community/blog/beyond-html5-peer-peer-conversational-video the first implementation of WebRTC].

WebRTC has now implemented open standards for real-time, plugin-free video, audio and data communication. The need is real:

* Many web services already use RTC, but need downloads, native apps or plugins. These includes Skype, Facebook (which uses Skype) and Google Hangouts (which use the Google Talk plugin).
* Downloading, installing and updating plugins can be complex, error prone and annoying.
* Plugins can be difficult to deploy, debug, troubleshoot, test and maintain—and may require licensing and integration with complex, expensive technology. It's often difficult to persuade people to install plugins in the first place!

The guiding principles of the WebRTC project are that its APIs should be open source, free, standardized, built into web browsers and more efficient than existing technologies.

== Where are we now? ==

WebRTC implements three APIs:

* [[#toc-mediastream|<tt>MediaStream</tt>]] (aka <tt>getUserMedia</tt>)
* <tt>RTCPeerConnection</tt>
* [[#toc-rtcdatachannel|<tt>RTCDataChannel</tt>]]

<tt>getUserMedia</tt> is available in Chrome, Opera and Firefox Nightly/Aurora. Take a look at the cross-browser demo of <tt>getUserMedia</tt> at [http://www.simpl.info/gum simpl.info/gum] (though for Firefox you'll need to [https://hacks.mozilla.org/2012/11/progress-update-on-webrtc-for-firefox-on-desktop/comment-page-1/#comment-1851192 set preferences]). Also check out Chris Wilson's [http://webaudiodemos.appspot.com/ amazing examples] of using <tt>getUserMedia</tt> as input for Web Audio.

<tt>webkitRTCPeerConnection</tt> is now in Chrome stable and it's flagless. (A word of explanation about the name: after several iterations, <tt>RTCPeerConnection</tt> is currently implemented by Chrome as <tt>webkitRTCPeerConnection</tt> and by Firefox Aurora/Nightly as <tt>mozRTCPeerConnection</tt>. Other names and implementations have been deprecated. When the standards process has stabilized, the prefixes will be removed.) There's an ultra-simple demo of Chrome's RTCPeerConnection implementation at [http://www.simpl.info/peerconnection simpl.info/pc] and a great video chat application at [http://apprtc.appspot.com apprtc.appspot.com].

'''<tt>RTCDataChannel</tt>''' is supported by Chrome 25 and above, but is behind a flag before Chrome 27. <tt>RTCPeerConnection</tt> and <tt>RTCDataChannel</tt> have also been [https://hacks.mozilla.org/2012/11/progress-update-on-webrtc-for-firefox-on-desktop/comment-page-1/#comment-1851192 in desktop Firefox Nightly and Aurora].

WebRTC is also implemented by the [https://labs.ericsson.com/apps/bowser Ericsson Bowser browser] which runs on iOS and Android:

[[Image:bowser.png|The Ericsson Bowser browser running on iOS and Android]]

WebRTC functionality is available in Internet Explorer [https://groups.google.com/forum/#!topic/discuss-webrtc/tKoh1wrI8ig via Chrome Frame], and Skype (acquired by Microsoft in 2011) is reputedly [http://gigaom.com/2012/06/26/skype-webrtc-web-client/ planning to use WebRTC]. WebRTC has also been integrated with [https://labs.ericsson.com/developer-community/blog/beyond-html5-conversational-voice-and-video-implemented-webkit-gtk WebKitGTK+] and [http://www.youtube.com/watch?v=Vm5ebKWKNE8 Qt] native apps.

=== A word of warning ===

Be skeptical of reports that a platform 'supports WebRTC'. Often this actually just means that <tt>getUserMedia</tt> is supported, but not any of the other RTC components.

== My first WebRTC ==

WebRTC applications need to do several things:

* Get streaming audio, video or other data.
* Get network information such as IP address and port, and exchange this with other WebRTC clients (known as ''peers'') to enable connection, even through [http://en.wikipedia.org/wiki/NAT_traversal NATs] and firewalls.
* Coordinate signaling communication to report errors and initiate or close sessions.
* Exchange information about media and client capability, such as resolution and codecs.
* Communicate streaming audio, video or data.

To acquire and communicate streaming data, WebRTC implements the following APIs.

* [https://dvcs.w3.org/hg/audio/raw-file/tip/streams/StreamProcessing.html MediaStream]: get access to data streams, such as from the user's camera and microphone.
* [http://dev.w3.org/2011/webrtc/editor/webrtc.html#rtcpeerconnection-interface RTCPeerConnection]: audio or video calling, with facilities for encryption and bandwidth management.
* [http://dev.w3.org/2011/webrtc/editor/webrtc.html#rtcdatachannel RTCDataChannel]: peer-to-peer communication of generic data.

(There is detailed discussion of the network and signaling aspects of WebRTC [[#signaling|below]].)

== MediaStream (aka getUserMedia) ==

The [http://dev.w3.org/2011/webrtc/editor/getusermedia.html MediaStream API] represents synchronized streams of media. For example, a stream taken from camera and microphone input has synchronized video and audio tracks. (Don't confuse MediaStream tracks with the &lt;track&gt; element, which is something [http://www.html5rocks.com/en/tutorials/track/basics/ entirely different].)

Probably the easiest way to understand MediaStream is to look at it in the wild:

# In Chrome, open the demo at [http://simpl.info/getusermedia/ simpl.info/gum]
# Open the console
# Inspect the <tt>stream</tt> variable, which is in global scope.

Each MediaStream has an input, which might be a LocalMediaStream generated by <tt>navigator.getUserMedia()</tt>, and an output, which might be passed to a video element or an RTCPeerConnection.

The <tt>getUserMedia()</tt> method takes three parameters:

* A [[#toc-constraints|constraints object]].
* A success callback which, if called, is passed a LocalMediaStream.
* A failure callback which, if called, is passed an error object.

Each LocalMediaStream (i.e. a MediaStream local to the browser) has a <tt>label</tt> (such as'Xk7EuLhsuHKbnjLWkW4yYGNJJ8ONsgwHBvLQ') and <tt>audioTracks</tt> and <tt>videoTracks</tt> properties, each of which is a MediaStreamTrackList.

For the [http://simpl.info/getusermedia/ simpl.info/gum] example, <tt>audioTracks</tt> and <tt>videoTracks</tt> each have one member, i.e. one MediaStreamTrack. Each MediaStreamTrack has a kind ('video' or 'audio'), and a label (something like 'FaceTime HD Camera (Built-in)'), and represents one or more channels of either audio or video. In this case, there is only one audio and one video track, but it is easy to imagine use cases where there are more: for example, a chat application that enables input from front camera, rear camera a microphone, and a 'screenshared' application.

In Chrome, the <tt>URL.createObjectURL()</tt> method converts a LocalMediaStream to a [http://www.html5rocks.com/tutorials/workers/basics/#toc-inlineworkers-bloburis Blob URL] which can be set as the <tt>src</tt> of a video element. (In Firefox and Opera, the <tt>src</tt> of the video can be set from the stream itself.) Since version 25, Chrome allows audio data from <tt>getUserMedia</tt> to be passed to an audio or video element (but note that by default the media element will be muted in this case.



<tt>getUserMedia</tt> can also be used [http://updates.html5rocks.com/2012/09/Live-Web-Audio-Input-Enabled as an input node for the Web Audio API]:

<pre class="prettyprint">function gotStream(stream) {
  var audioContext = 'webkitAudioContext' in window ?
    new webkitAudioContext() : new AudioContext();
  var mediaStreamSource = audioContext.createMediaStreamSource(stream);
  mediaStreamSource.connect(audioContext.destination);
}

navigator.webkitGetUserMedia({audio:true}, gotStream);</pre>
Chrome apps and extensions can also incorporate <tt>getUserMedia</tt>. Adding <tt>audioCapture</tt> and/or <tt>videoCapture</tt> [https://developer.chrome.com/extensions/manifest.html#permissions permissions] to the manifest enables permission to be requested and granted only once, on installation. Thereafter the user is not asked for permission for camera or microphone access. Likewise, on pages using HTTPS, calls to <tt>getUserMedia()</tt> in Chrome will cause an Always Allow button to be displayed in the browser's [http://dev.chromium.org/user-experience/infobars infobar]: permission only has to be granted once.

Chrome apps also now make it possible to share a live 'video' of a browser tab via the experimental [http://developer.chrome.com/dev/extensions/tabCapture.html chrome.tabCapture] API. For a screencast, code and more information, see the HTML5 Rocks update: [http://updates.html5rocks.com/2012/12/Screensharing-with-WebRTC Screensharing with WebRTC].

The intention is eventually to enable a MediaStream for any streaming data source, not just a camera or microphone, which would enable collection of arbitrary real-time data, for example from sensors or other inputs.

Note that <tt>getUserMedia()</tt> must be used on a server, not the local file system, otherwise a <tt>PERMISSION_DENIED: 1</tt> error will be thrown.

=== Resolution Constraints ===

[http://tools.ietf.org/html/draft-alvestrand-constraints-resolution-00#page-4 Constraints] have been implemented in Chrome 24 and above. These can be used to set values for video resolution for <tt>getUserMedia()</tt> and RTCPeerConnection <tt>addStream()</tt> calls.

There's an example at [http://simpl.info/getusermedia/constraints/index.html simpl.info/getusermedia/constraints].

One gotcha: <tt>getUserMedia</tt> constraints set in one browser tab affect constraints for all tabs opened subsequently. Setting a disallowed value for constraints gives a rather cryptic error message:

<pre class="prettyprint">navigator.getUserMedia error:  NavigatorUserMediaError {code: 1, PERMISSION_DENIED: 1}</pre>
== Signaling: session control, network and media information ==

WebRTC uses RTCPeerConnection to communicate streaming data between browsers (aka peers), but also needs a mechanism to coordinate communication and to send control messages, a process known as signaling. Signaling methods and protocols are ''not'' specified by WebRTC: signaling is not part of the RTCPeerConnection API.

Instead, WebRTC app developers can choose whatever messaging protocol they prefer, such as SIP or XMPP, and any appropriate duplex (two-way) communication channel. The [http://apprtc.appspot.com apprtc.appspot.com] example uses XHR and the Channel API as the signaling mechanism. Silvia Pfeiffer and others have demonstrated [http://blog.gingertech.net/2012/06/04/video-conferencing-in-html5-webrtc-via-web-sockets/ WebRTC signaling via WebSocket].

Signaling is used to exchange three types of information.

* Session control messages: to initialize or close communication and report errors.
* Network configuration: to the outside world, what's my computer's IP address and port?
* Media capabilities: what codecs and resolutions can be handled by my browser and the browser it wants to communicate with?

The exchange of information via signaling must have completed successfully before peer-to-peer streaming can begin.

For example, imagine Alice wants to communicate with Bob. Here's a code sample from the [http://www.w3.org/TR/webrtc/#simple-example WebRTC W3C Working Draft], which shows the signaling process in action. (The code assumes the existence of some signaling mechanism, created in the <tt>createSignalingChannel()</tt> method. Also note that on Chrome, RTCPeerConnection is currently prefixed.)

<pre class="prettyprint">var signalingChannel = createSignalingChannel();
var pc;
var configuration = ...;

// run start(true) to initiate a call
function start(isCaller) {
    pc = new RTCPeerConnection(configuration);

    // send any ice candidates to the other peer
    pc.onicecandidate = function (evt) {
        signalingChannel.send(JSON.stringify({ &quot;candidate&quot;: evt.candidate }));
    };

    // once remote stream arrives, show it in the remote video element
    pc.onaddstream = function (evt) {
        remoteView.src = URL.createObjectURL(evt.stream);
    };

    // get the local stream, show it in the local video element and send it
    navigator.getUserMedia({ &quot;audio&quot;: true, &quot;video&quot;: true }, function (stream) {
        selfView.src = URL.createObjectURL(stream);
        pc.addStream(stream);

        if (isCaller)
            pc.createOffer(gotDescription);
        else
            pc.createAnswer(pc.remoteDescription, gotDescription);

        function gotDescription(desc) {
            pc.setLocalDescription(desc);
            signalingChannel.send(JSON.stringify({ &quot;sdp&quot;: desc }));
        }
    });
}

signalingChannel.onmessage = function (evt) {
    if (!pc)
        start(false);

    var signal = JSON.parse(evt.data);
    if (signal.sdp)
        pc.setRemoteDescription(new RTCSessionDescription(signal.sdp));
    else
        pc.addIceCandidate(new RTCIceCandidate(signal.candidate));
};</pre>
First up, Alice and Bob exchange network information. (The expression 'finding candidates' refers to the process of finding network interfaces and ports using the [[#ice|ICE framework]].)

# Alice creates an RTCPeerConnection object with an <tt>onicecandidate</tt> handler.
# The handler is run when network candidates become available.
# Alice sends serialized candidate data to Bob, via whatever signaling channel they are using: WebSocket or some other mechanism.
# When Bob gets a candidate message from Alice, he calls <tt>addIceCandidate</tt>, to add the candidate to the remote peer description.

WebRTC clients (known as '''peers''', aka Alice and Bob) also need to ascertain and exchange local and remote audio and video media information, such as resolution and codec capabilities. Signaling to exchange media configuration information proceeds by exchanging an ''offer'' and an ''answer'' using the Session Description Protocol (SDP):

# Alice runs the RTCPeerConnection <tt>createOffer()</tt> method. The callback argument of this is passed an RTCSessionDescription: Alice's local session description.
# In the callback, Alice sets the local description using <tt>setLocalDesecription()</tt> and then sends this session description to Bob via their signaling channel.
# Bob sets the description Alice sent him as the remote description (using <tt>setRemoteDescription()</tt>).
# Bob runs the RTCPeerConnection <tt>createAnswer()</tt> method, passing it the remote description he got from Alice, so a local session can be generated that is compatible with hers. The <tt>createAnswer()</tt> callback is passed an RTCSessionDescription: Bob sets that as the local description and sends it to Alice.
# When Alice gets Bob's session description, she sets that as the remote description with <tt>setRemoteDescription</tt>.
# Ping!

RTCSessionDescription objects are blobs that conform to the [http://en.wikipedia.org/wiki/Session_Description_Protocol Session Description Protocol], SDP. Serialized, an SDP object looks like this:

<pre class="prettyprint">v=0
o=- 3883943731 1 IN IP4 127.0.0.1
s=
t=0 0
a=group:BUNDLE audio video
m=audio 1 RTP/SAVPF 103 104 0 8 106 105 13 126

// ...

a=ssrc:2223794119 label:H4fjnMzxy3dPIgQ7HxuCTLb4wLLLeRHnFxh810</pre>
The acquisition and exchange of network and media information can be done simultaneously, but both processes must have completed before audio and video streaming between peers can begin.

The offer/answer architecture described above is called [http://tools.ietf.org/html/draft-ietf-rtcweb-jsep-00 JSEP], JavaScript Session Establishment Protocol. (There's an excellent animation explaining the process of signaling and streaming in [https://labs.ericsson.com/developer-community/blog/beyond-html5-peer-peer-conversational-video Ericsson's demo video] for its first WebRTC implementation.)

[[Image:jsep.png|JSEP architecture diagram]]

Once the signaling process has completed successfully, data can be streamed directly peer to peer, between the caller and callee—or if that fails, via an intermediary server (more about that below). Streaming is the job of RTCPeerConnection.

== RTCPeerConnection ==

RTCPeerConnection is the WebRTC component that handles stable and efficient communication of streaming data between peers.

Below is a WebRTC architecture diagram showing the role of RTCPeerConnection. As you will notice, the green parts are complex!

[http://www.webrtc.org/reference/architecture [[Image:webrtcArchitecture.png|WebRTC architecture diagram]]]

From a JavaScript perspective, the main thing to understand from this diagram is that RTCPeerConnection shields web developers from the myriad complexities that lurk beneath. The codecs and protocols used by WebRTC do a huge amount of work to make real-time communication possible, even over unreliable networks:

* packet loss concealment
* echo cancellation
* bandwidth adaptivity
* dynamic jitter buffering
* automatic gain control
* noise reduction and suppression
* image 'cleaning'.

The [[#simpleRTCPeerConnectionExample|W3C code above]] shows a simplified example of WebRTC from a signaling perspective. Below are walkthroughs of two working WebRTC applications: the first is a simple example to demonstrate RTCPeerConnection; the second is a fully operational video chat client.

=== RTCPeerConnection sans servers ===

The code below is taken from the 'single page' WebRTC demo at [https://webrtc-demos.appspot.com/html/pc1.html webrtc-demos.appspot.com], which has local ''and'' remote RTCPeerConnection (and local and remote video) on one web page. This doesn't constitute anything very useful—caller and callee are on the same page—but it does make the workings of the RTCPeerConnection API a little clearer, since the RTCPeerConnection objects on the page can exchange data and messages directly without having to use intermediary signaling mechanisms.

One gotcha: the optional second 'constraints' parameter of the <tt>RTCPeerConnection()</tt> constructor is different from the constraints type used by <tt>getUserMedia()</tt>: see [[%20http://www.w3.org/TR/webrtc/#constraints|w3.org/TR/webrtc/#constraints]] for more information.

In this example, <tt>pc1</tt> represents the local peer (caller) and <tt>pc2</tt> represents the remote peer (callee).

=== Caller ===

<ol>
<li><p>Create a new RTCPeerConnection and add the stream from <tt>getUserMedia()</tt>:</p>
<pre class="prettyprint">// servers is an optional config file (see TURN and STUN discussion below)
pc1 = new webkitRTCPeerConnection(servers);
// ...
pc1.addStream(localstream); </pre></li>
<li><p>Create an offer and set it as the local description for <tt>pc1</tt> and as the remote description for <tt>pc2</tt>. This can be done directly in the code without using signaling, because both caller and callee are on the same page:</p>
<pre class="prettyprint">pc1.createOffer(gotDescription1);
//...
function gotDescription1(desc){
  pc1.setLocalDescription(desc);
  trace(&quot;Offer from pc1 \n&quot; + desc.sdp);
  pc2.setRemoteDescription(desc);
  pc2.createAnswer(gotDescription2);
}</pre></li></ol>

=== Callee ===

<ol>
<li><p>Create <tt>pc2</tt> and, when the stream from <tt>pc1</tt>is added, display it in a video element:</p>
<pre class="prettyprint">pc2 = new webkitRTCPeerConnection(servers);
pc2.onaddstream = gotRemoteStream;
//...
function gotRemoteStream(e){
  vid2.src = URL.createObjectURL(e.stream);
}</pre></li></ol>

=== RTCPeerConnection plus servers ===

In the real world, WebRTC needs servers, however simple, so the following can happen:

* Users discover each other and exchange 'real world' details such as names.
* WebRTC client applications (peers) exchange network information.
* Peers exchange data about media such as video format and resolution.
* WebRTC client applications traverse [http://en.wikipedia.org/wiki/NAT_traversal NAT gateways] and firewalls.

In other words, WebRTC needs four types of server-side functionality:

* User discovery and communication.
* Signaling.
* NAT/firewall traversal.
* Relay servers in case peer-to-peer communication fails.

NAT traversal, peer-to-peer networking, and the requirements for building a server app for user discovery and signaling, are beyond the scope of this article. Suffice to say that the [http://en.wikipedia.org/wiki/STUN STUN] protocol and its extension [http://en.wikipedia.org/wiki/Traversal_Using_Relay_NAT TURN] are used by the [http://en.wikipedia.org/wiki/Interactive_Connectivity_Establishment ICE] framework to enable RTCPeerConnection to cope with NAT traversal and other network vagaries.

ICE is a framework for connecting peers, such as two video chat clients. Initially, ICE tries to connect peers ''directly'', with the lowest possible latency, via UDP. In this process, STUN servers have a single task: to enable a peer behind a NAT to find out its public address and port. (Google has a couple of STUN severs, one of which is used in the apprtc.appspot.com example.)

[[Image:stun.png|Finding connection candidates]]

If UDP fails, ICE tries TCP: first HTTP, then HTTPS. If direct connection fails—in particular, because of enterprise NAT traversal and firewalls—ICE uses an intermediary (relay) TURN server. In other words, ICE will first use STUN with UDP to directly connect peers and, if that fails, will fall back to a TURN relay server. The expression 'finding candidates' refers to the process of finding network interfaces and ports.

[[Image:dataPathways.png|WebRTC data pathways]]

To find out more about how set up a server to deal with signaling and user discovery, take a look at the code repository for the [http://apprtc.appspot.com apprtc.appspot.com] demo, which is at [http://code.google.com/p/webrtc-samples/source/browse/trunk/apprtc/ code.google.com/p/webrtc-samples/source/browse/trunk/apprtc/]. This uses the Google App Engine Channel API. For information about using a WebSocket server for signaling, check out Silvia Pfeiffer's [http://blog.gingertech.net/2012/06/04/video-conferencing-in-html5-webrtc-via-web-sockets/ WebSocket WebRTC app].

==== A simple video chat client ====

A good place to try out WebRTC, complete with signaling and NAT/firewall traversal using a STUN server, is the video chat demo at [http://apprtc.appspot.com apprtc.appspot.com]. This app uses [https://apprtc.appspot.com/js/adapter.js adapter.js] to cope with different RTCPeerConnection and <tt>getUserMedia()</tt> implementations.

The code is deliberately verbose in its logging: check the console to understand the order of events. Below we give a detailed walk-through of the code.

=== What's going on? ===

The demo starts by running the <tt>initalize()</tt> function:

<pre class="prettyprint">function initialize() {
    console.log(&quot;Initializing; room=99688636.&quot;);
    card = document.getElementById(&quot;card&quot;);
    localVideo = document.getElementById(&quot;localVideo&quot;);
    miniVideo = document.getElementById(&quot;miniVideo&quot;);
    remoteVideo = document.getElementById(&quot;remoteVideo&quot;);
    resetStatus();
    openChannel('AHRlWrqvgCpvbd9B-Gl5vZ2F1BlpwFv0xBUwRgLF/* ...*/');
    doGetUserMedia();
  }</pre>
Note that values used in the JavaScript, such as the <tt>room</tt> variable and the token used by <tt>openChannel()</tt>, are provided by the Google App Engine app itself: take a look at the [http://code.google.com/p/webrtc-samples/source/browse/trunk/apprtc/index.html index.html template] in the repository to see what values are added.

This code initializes variables for the HTML video elements that will display video streams from the local camera (<tt>localVideo</tt>) and from the camera on the remote client (<tt>remoteVideo</tt>). <tt>resetStatus()</tt> simply sets a status message.

The <tt>openChannel()</tt> function sets up messaging between WebRTC clients:

<pre class="prettyprint">function openChannel(channelToken) {
  console.log(&quot;Opening channel.&quot;);
  var channel = new goog.appengine.Channel(channelToken);
  var handler = {
    'onopen': onChannelOpened,
    'onmessage': onChannelMessage,
    'onerror': onChannelError,
    'onclose': onChannelClosed
  };
  socket = channel.open(handler);
}</pre>
For signaling, this demo uses the Google App Engine [http://code.google.com/appengine/docs/python/channel/overview.html Channel API], which enables messaging between JavaScript clients without polling. (WebRTC signaling is covered in more detail [[#toc-signaling|above]]).

[[Image:apprtcArchitecture.png|Architecture of the apprtc video chat application]]

Establishing a channel with the Channel API works like this:

# Client A generates a unique ID.
# Client A requests a Channel token from the App Engine app, passing its ID.
# App Engine app requests a channel and a token for the client's ID from the Channel API.
# App sends the token to Client A.
# Client A opens a socket and listens on the channel set up on the server.

[[Image:channelEstablishing.png|The Google Channel API: establishing a channel]]

Sending a message works like this:

# Client B makes a POST request to the App Engine app with an update.
# The App Engine app passes a request to the channel.
# The channel carries a message to Client A.
# Client A's onmessage callback is called.

[[Image:channelSending.png|The Google Channel API: sending a message]]

Just to reiterate: signaling messages are communicated via whatever mechanism the developer chooses: the signaling mechanism is not specified by WebRTC. The Channel API is used in this demo, but other methods (such as WebSocket) could be used instead.

After the call to <tt>openChannel()</tt>, the <tt>getUserMedia()</tt> function called by <tt>initialize()</tt> checks if the browser supports the <tt>getUserMedia</tt> API. (Find out more about getUserMedia on [http://www.html5rocks.com/en/tutorials/getusermedia/intro/ HTML5 Rocks].) If all is well, onUserMediaSuccess is called:

<pre class="prettyprint">function onUserMediaSuccess(stream) {
  console.log(&quot;User has granted access to local media.&quot;);
  // Call the polyfill wrapper to attach the media stream to this element.
  attachMediaStream(localVideo, stream);
  localVideo.style.opacity = 1;
  localStream = stream;
  // Caller creates PeerConnection.
  if (initiator) maybeStart();
}</pre>
This causes video from the local camera to be displayed in the <tt>localVideo</tt> element, by creating an [http://www.html5rocks.com/tutorials/workers/basics/#toc-inlineworkers-bloburis object (Blob) URL] for the camera's data stream and then setting that URL as the <tt>src</tt> for the element. (<tt>createObjectURL</tt> is used here as a way to get a URI for an 'in memory' binary resource, i.e. the LocalDataStream for the video.) The data stream is also set as the value of <tt>localStream</tt>, which is subsequently made available to the remote user.

At this point, <tt>initiator</tt> has been set to 1 (and it stays that way until the caller's session has terminated) so <tt>maybeStart()</tt> is called:

<pre class="prettyprint">function maybeStart() {
  if (!started &amp;&amp; localStream &amp;&amp; channelReady) {
    // ...
    createPeerConnection();
    // ...
    pc.addStream(localStream);
    started = true;
    // Caller initiates offer to peer.
    if (initiator)
      doCall();
  }
}</pre>
This function uses a handy construct when working with multiple asynchronous callbacks: <tt>maybeStart()</tt> may be called by any one of several functions, but the code in it is run only when <tt>localStream</tt> has been defined ''and'' <tt>channelReady</tt> has been set to true ''and'' communication hasn't already started. So—if a connection hasn't already been made, and a local stream is available, and a channel is ready for signaling, a connection is created and passed the local video stream. Once that happens, <tt>started</tt> is set to true, so a connection won't be started more than once.

==== RTCPeerConnection: making a call ====

<tt>createPeerConnection()</tt>, called by <tt>maybeStart()</tt>, is where the real action begins:

<pre class="prettyprint">function createPeerConnection() {
  var pc_config = {&quot;iceServers&quot;: [{&quot;url&quot;: &quot;stun:stun.l.google.com:19302&quot;}]};
  try {
    // Create an RTCPeerConnection via the polyfill (adapter.js).
    pc = new RTCPeerConnection(pc_config);
    pc.onicecandidate = onIceCandidate;
    console.log(&quot;Created RTCPeerConnnection with config:\n&quot; + &quot;  \&quot;&quot; +
      JSON.stringify(pc_config) + &quot;\&quot;.&quot;);
  } catch (e) {
    console.log(&quot;Failed to create PeerConnection, exception: &quot; + e.message);
    alert(&quot;Cannot create RTCPeerConnection object; WebRTC is not supported by this browser.&quot;);
      return;
  }

  pc.onconnecting = onSessionConnecting;
  pc.onopen = onSessionOpened;
  pc.onaddstream = onRemoteStreamAdded;
  pc.onremovestream = onRemoteStreamRemoved;
}</pre>
The underlying purpose is to set up a connection, using a STUN server, with <tt>onIceCandidate()</tt> as the callback (see [[#stun|above]] for an explanation of ICE, STUN and 'candidate'). Handlers are then set for each of the RTCPeerConnection events: when a session is connecting or open, and when a remote stream is added or removed. In fact, in this example these handlers only log status messages—except for <tt>onRemoteStreamAdded()</tt>, which sets the source for the <tt>remoteVideo</tt> element:

<pre class="prettyprint">function onRemoteStreamAdded(event) {
  // ...
  miniVideo.src = localVideo.src;
  attachMediaStream(remoteVideo, event.stream);
  remoteStream = event.stream;
  waitForRemoteVideo();
}</pre>
Once <tt>createPeerConnection()</tt> has been invoked in <tt>maybeStart()</tt>, a call is intitiated by creating and offer and sending it to the callee:

<pre class="prettyprint">function doCall() {
  console.log(&quot;Sending offer to peer.&quot;);
  pc.createOffer(setLocalAndSendMessage, null, mediaConstraints);
}</pre>
The offer creation process here is similar to the no-signaling example [[#toc-sans|above]] but, in addition, a message is sent to the remote peer, giving a serialized SessionDescription for the offer. This process is handled by <tt>setLocalAndSendMessage():</tt>

<pre class="prettyprint">function setLocalAndSendMessage(sessionDescription) {
  // Set Opus as the preferred codec in SDP if Opus is present.
  sessionDescription.sdp = preferOpus(sessionDescription.sdp);
  pc.setLocalDescription(sessionDescription);
  sendMessage(sessionDescription);
}</pre>
==== Signaling with the Channel API ====

The <tt>onIceCandidate()</tt> callback invoked when the RTCPeerConnection is successfully created in <tt>createPeerConnection()</tt> sends information about candidates as they are 'gathered':

<pre class="prettyprint">function onIceCandidate(event) {
    if (event.candidate) {
      sendMessage({type: 'candidate',
        label: event.candidate.sdpMLineIndex,
        id: event.candidate.sdpMid,
        candidate: event.candidate.candidate});
    } else {
      console.log(&quot;End of candidates.&quot;);
    }
  }</pre>
Outbound messaging, from the client to the server, is done by <tt>sendMessage()</tt> with an XHR request:

<pre class="prettyprint">function sendMessage(message) {
  var msgString = JSON.stringify(message);
  console.log('C-&gt;S: ' + msgString);
  path = '/message?r=99688636' + '&amp;u=92246248';
  var xhr = new XMLHttpRequest();
  xhr.open('POST', path, true);
  xhr.send(msgString);
}</pre>
XHR works fine for sending signaling messages from the client to the server, but some mechanism is needed for server-to-client messaging: this application uses the Google App Engine Channel API. Messages from the API (i.e. from the App Engine server) are handled by <tt>processSignalingMessage()</tt>:

<pre class="prettyprint">function processSignalingMessage(message) {
  var msg = JSON.parse(message);

  if (msg.type === 'offer') {
    // Callee creates PeerConnection
    if (!initiator &amp;&amp; !started)
      maybeStart();

    pc.setRemoteDescription(new RTCSessionDescription(msg));
    doAnswer();
  } else if (msg.type === 'answer' &amp;&amp; started) {
    pc.setRemoteDescription(new RTCSessionDescription(msg));
  } else if (msg.type === 'candidate' &amp;&amp; started) {
    var candidate = new RTCIceCandidate({sdpMLineIndex:msg.label,
                                         candidate:msg.candidate});
    pc.addIceCandidate(candidate);
  } else if (msg.type === 'bye' &amp;&amp; started) {
    onRemoteHangup();
  }
}</pre>
If the message is an answer from a peer (a response to an offer), RTCPeerConnection sets the remote SessionDescription and communication can begin. If the message is an offer (i.e. a message from the callee) RTCPeerConnection sets the remote SessionDescription, sends an answer to the callee, and starts connection by invoking the RTCPeerConnection <tt>startIce()</tt> method:

<pre class="prettyprint">function doAnswer() {
  console.log(&quot;Sending answer to peer.&quot;);
  pc.createAnswer(setLocalAndSendMessage, null, mediaConstraints);
}</pre>
And that's it! The caller and callee have discovered each other and exchanged information about their capabilities, a call session is initiated, and real-time data communication can begin.

=== Network topologies ===

WebRTC as currently implemented only supports one-to-one communication, but could be used in more complex network scenarios: for example, with multiple peers each communicating each other directly, peer-to-peer, or via a centralized server.

Many existing WebRTC apps only demonstrate communication between web browsers, but gateway servers can enable a WebRTC app running on a browser to interact with devices such as [http://en.wikipedia.org/wiki/Public_switched_telephone_network telephones], and with [http://en.wikipedia.org/wiki/Voice_over_IP VOIP] systems. In May 2012, Doubango Telecom open-sourced the [http://sipml5.org/ sipml5 SIP client], built with WebRTC and WebSocket which (among other potential uses) enables video calls between browsers and apps running on iOS or Android. At Google I/O in 2012, Tethr and Tropo demonstrated [http://tethr.tumblr.com/post/25513708436/tethr-and-tropo-in-the-google-i-o-sandbox a framework for disaster communications] 'in a briefcase', using an [http://en.wikipedia.org/wiki/OpenBTS OpenBTS cell] to enable communications between feature phones and computers via WebRTC. Telephone communication without a carrier!

[[Image:tethr.jpg|Tethr/Tropo demo at Google I/O 2012]]

== RTCDataChannel ==

As well as audio and video, WebRTC supports real-time communication for other types of data.

The RTCDataChannel API will enable peer-to-peer exchange of arbitrary data, with low latency and high throughput.

There are many potential use cases for the API, including:

* Gaming
* Remote desktop applications
* Real-time text chat
* File transfer
* Decentralized networks

The API has several features to make the most of RTCPeerConnection and enable powerful and flexible peer-to-peer communication:

* Leveraging of RTCPeerConnection session setup.
* Multiple simultaneous channels, with prioritization.
* Reliable and unreliable delivery semantics.
* Built-in security (DTLS) and congestion control.
* Ability to use with or without audio or video.

The syntax is deliberately similar to WebSocket, with <tt>send()</tt> and <tt>onmessage</tt>, as you will see in the code sample below:

<pre class="prettyprint">// RTCPeerConnection setup and offer-answer exchange omitted
var dc1 = pc1.createDataChannel(&quot;mylabel&quot;);  // create the sending RTCDataChannel (reliable mode)
var dc2 = pc2.createDataChannel(&quot;mylabel&quot;);  // create the receiving RTCDataChannel (reliable mode)

// append received RTCDataChannel messages to a textarea
var receiveTextarea = document.querySelector(&quot;textarea#receive&quot;);
dc2.onmessage = function(event) {
  receiveTextarea.value += event.data;
};

var sendInput = document.querySelector(&quot;input#send&quot;);
// send message over the RTCDataChannel
function onSend() {
  dc1.send(sendInput.value);
}</pre>
[http://www.html5rocks.com/en/tutorials/webrtc/basics/#toc-RTCDataChannel RTCDataChannel] is a WebRTC API for high performance, low latency, peer-to-peer communication of arbitrary data. The API is simple—similar to WebSocket—but communication occurs directly between browsers, so RTCDataChannel can be much faster than WebSocket even if a relay (TURN) server is required when 'hole punching' to cope with firewalls and NATs fails.

RTCDataChannel is in version 25 of Chrome, behind a flag. This version is for experimentation only, is not fully functional, and communication isn't possible with the Firefox implementation. RTCDataChannel in Chrome 26 is more stable, flagless and compatible with RTCDataChannel in Firefox.

Firefox Nightly/Aurora supports <tt>mozGetUserMedia</tt>, <tt>mozRTCPeerConnection</tt> and <tt>RTCDataChannel</tt> (but don't forget to set your about:config preferences!)

Here's a screenshot of RTCDataChannel running in Firefox:

[[Image:firefoxDataChannel.png|Firefox RTCDataChannel screenshot]]

This demo is at [http://mozilla.github.com/webrtc-landing/data_test.html http://mozilla.github.com/webrtc-landing/data_test.html]. Here's a code snippet:

<pre class="prettyprint">pc1.onconnection = function() {
  log(&quot;pc1 onConnection &quot;);
  dc1 = pc1.createDataChannel(&quot;This is pc1&quot;,{}); // reliable (TCP-like)
  dc1 = pc1.createDataChannel(&quot;This is pc1&quot;,{outOfOrderAllowed: true, maxRetransmitNum: 0}); // unreliable (UDP-like)
  log(&quot;pc1 created channel &quot; + dc1 + &quot; binarytype = &quot; + dc1.binaryType);
  channel = dc1;
  channel.binaryType = &quot;blob&quot;;
  log(&quot;pc1 new binarytype = &quot; + dc1.binaryType);

  // Since we create the RTCDataChannel, don't wait for onDataChannel!
  channel.onmessage = function(evt) {
    if (evt.data instanceof Blob) {
      fancy_log(&quot;*** pc2 sent Blob: &quot; + evt.data + &quot;, length=&quot; + evt.data.size,&quot;blue&quot;);
    } else {
      fancy_log('pc2 said: ' + evt.data, &quot;blue&quot;);
    }
  }
  channel.onopen = function() {
    log(&quot;pc1 onopen fired for &quot; + channel);
    channel.send(&quot;pc1 says Hello...&quot;);
    log(&quot;pc1 state: &quot; + channel.state);
  }
  channel.onclose = function() {
    log(&quot;pc1 onclose fired&quot;);
  };
  log(&quot;pc1 state:&quot; + channel.readyState);
      }</pre>
More information and demos for the Firefox implementation are available from the [https://hacks.mozilla.org/2012/11/progress-update-on-webrtc-for-firefox-on-desktop/comment-page-1/#comment-1851192 hacks.mozilla.org blog]. Basic WebRTC support is due for release in Firefox 18 at the beginning of 2013, and support is planned for additional features including <tt>getUserMedia</tt> and createOffer/Answer constraints, as well as TURN (to allow communication between browsers behind firewalls).

For more information about RTCDataChannel, take a look at the IETF's [http://tools.ietf.org/html/draft-jesup-rtcweb-data-protocol-00 draft protocol spec].

== Security ==

There are several ways a real-time communication application or plugin might compromise security. For example:

* Unencrypted media or data might be intercepted en route between browsers, or between a browser and a server.
* An application might record and distribute video or audio without the user knowing.
* Malware or viruses might be installed alongside an apparently innocuous plugin or application.

WebRTC has several features to avoid these problems:

* WebRTC implementations use secure protocols such as [http://en.wikipedia.org/wiki/Datagram_Transport_Layer_Security DTLS] and [http://en.wikipedia.org/wiki/Secure_Real-time_Transport_Protocol SRTP].
* Encryption is mandatory for all WebRTC components, including signaling mechanisms.
* WebRTC is not a plugin: its components run in the browser sandbox and not in a separate process, components do not require separate installation, and are updated whenever the browser is updated.
* Camera and microphone access must be granted explicitly and, when the camera or microphone are running, this is clearly shown by the user interface.

A full discussion of security for streaming media is out of scope for this article. For more information, see the [http://www.ietf.org/proceedings/82/slides/rtcweb-13.pdf WebRTC Security Architecture] proposed by the IETF.

== In conclusion ==

The APIs and standards of WebRTC can democratize and decentralize tools for content creation and communication—for telephony, gaming, video production, music making, news gathering and many other applications.

Technology doesn't get much more [http://en.wikipedia.org/wiki/Disruptive_innovation disruptive] than this.

We look forward to what JavaScript developers make of WebRTC as it becomes widely implemented. As blogger Phil Edholm [http://www.nojitter.com/post/232901042/webrtc-is-it-a-game-changer put it], 'Potentially, WebRTC and HTML5 could enable the same transformation for real-time communications that the original browser did for information.'

== Learn more ==

* WebRTC book by Alan B. Johnston and Daniel C. Burnett (available in print and for eBook formats): [http://www.webrtcbook.com webrtcbook.com]
* [https://www.youtube.com/watch?v=E8C8ouiXHHk Video of Justin Uberti's WebRTC session at Google I/O, 27 June 2012]
* [http://www.webrtc.org/ webrtc.org]: the home for all things WebRTC—demos, documentation and discussion.
* [http://www.webrtc.org/running-the-demos webrtc.org demo page]: links to demos.
* Google Developers [https://developers.google.com/talk/libjingle/important_concepts#connections Google Talk documentation], which gives more information about NAT traversal, STUN, relay servers and candidate gathering.
* [https://groups.google.com/forum/?fromgroups#!forum/discuss-webrtc discuss-webrtc]: Google Group for WebRTC discussion.
* [http://dev.w3.org/2011/webrtc/editor/webrtc.html The WebRTC W3C Editor's Draft].
* [http://dev.w3.org/2011/webrtc/editor/getusermedia.html W3C Editor's Draft: Media Capture and Streams] (aka getUserMedia).
* [http://tools.ietf.org/wg/rtcweb/charters IETF Working Group Charter].
* [http://tools.ietf.org/html/draft-jesup-rtcweb-data-protocol-01 IETF WebRTC Data Channel Protocol Draft].
* [http://tools.ietf.org/html/draft-uberti-rtcweb-jsep-02 IETF JSEP Draft].
* [http://tools.ietf.org/html/rfc5245 IETF proposed standard for ICE]

== WebRTC support summary ==

=== MediaStream and getUserMedia ===

* Chrome 18.0.1008+
* Opera, Opera Mobile 12
* Firefox 17+

=== RTCPeerConnection ===

* Chrome 20+ (now 'flagless', i.e. no need to change about://flags settings)
* Firefox Aurora/Nightly (see [https://hacks.mozilla.org/2012/11/progress-update-on-webrtc-for-firefox-on-desktop/comment-page-1/#comment-1851192 instructions and demo])(

=== RTCDataChannel ===

* Experimental version in Chrome 25, more stable (and with Firefox interoperability) in Chrome 26
* Firefox Aurora/Nightly (see [https://hacks.mozilla.org/2012/11/progress-update-on-webrtc-for-firefox-on-desktop/comment-page-1/#comment-1851192 instructions and demo])

WebRTC support is available for Internet Explorer via Chrome Frame: [http://www.youtube.com/watch?v=rICLVXcc02A demo screencast and links to documentation].

Native APIs for RTCPeerConnection are also available: [http://www.webrtc.org/reference/native-apis documentation on webrtc.org].

The experimental Ericsson [[#bowser|Bowser browser]] supports MediaStream and RTCPeerConnection. Mobile support is in planned for Chrome and Firefox.

For more detailed information about cross-platform support for APIs such as getUserMedia, see [http://caniuse.com/stream caniuse.com].

**
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Topic_clusters=Audio, Multimedia, Video, WebRTC
}}
{{Topics|Audio, Media, Video, WebAudio, WebRTC}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/webrtc/basics/
}}