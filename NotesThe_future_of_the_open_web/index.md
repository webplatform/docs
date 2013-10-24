= The future of the Open Web =

== Summary ==
Notes taken to give an overview of what is coming on the Open Web and the Web Platform as a whole.

'''Subjects'''
* Key historic events
* Closing the gap with native
* Better layout systems
* Essential to learn to be future proof
* The web as a database
* Cool new things that you should know about

== Threads ==

=== Key historic events ===
* Microsoft and HP, two big desktop companies, created Web based Operating systems (WebOS, Windows 8)
* Mozilla creating a fork of Android and making it completely web based too
* Microsoft contributing to open source in Blink (Chrome rendering engine) with Pointer Events
* SVG web applications is getting more and more possible, look at this [1]
* Accessibility and SVG (see [http://describler.com/ Describler])
* Microsoft enforcing the DNT header
* W3C, Adobe, Mozilla, Google, Facebook, Microsoft, Opera decided to team up together to solve the documentation for web developers problem

=== Closing the gap with native ===
The web is not what it was a few years ago. We see many makers using web technologies to connect to physical devices. 

Access to this data might arise never seen before issues: 
* Am I recorded without my consent
* I just want to watch this video, why do I need a plugin?
* My phone has access to my location, is it sent without my knowledge to anybody?

But we still want to gain access to the device to make cool thins:
* Notification dialogs
* Use the camera to make photo booth
* Create ways to interact with friends who are currently close by
* Adjust site depending on the device orientation

Where do we draw a line?

=== Better layout systems ===

See Eric Meyer's presentation on Strong Layout systems (#TODO) and notes [http://responsive.ly/2013/04/session-notes-for-eric-meyers-strong-layout-systems/ Session notes from Eric Meyer's Strong Layout systems].

Float was a temporary hack to allow images to be beside text. It grew to what we know.

What is coming in that realm:
* Flexible box, where we can play with ordering, orientation, how it spans, how it calculates its own size
* Pixels is not a good unit of measurement: REMs and EMs
* Grid definition ([http://dev.w3.org/csswg/css-grid/ W3C/CSSWG])
* Web components <gangnam-style /> ([https://www.youtube.com/watch?v=fqULJBBEVQE WebComponents at Google IO])
* Live data binding ([http://wiki.ecmascript.org/doku.php?id=harmony:observe Object.observe]) (see also [http://derbyjs.com/ Derby], [http://knockoutjs.com/documentation/value-binding.html Knockout], [http://docs.angularjs.org/guide/dev_guide.templates.databinding AngularJS], [http://jquerymy.com/ jQuery.my], [http://rivetsjs.com/ rivetsjs])

=== The web as a database ===
The web is more than just web pages in a browser. You can programatically ask for things and it can follow relationships.
* Hypermedia (using HTTP verbs, follow links, get a resource from it)
* Meta data in the markup


=== Essential to learn to be future proof ===
Learn to use the real APIs. Not just the tools such as jQuery, or Cordova, or Sencha.  It binds you to the vendor.



=== Cool new things that you should know about ===
There are many very powerful things coming our way nowadays.

* Let's add value to the data RDFa and use the web as a database (SPARQL, YQL)
* LocalStorage, 
* AppCache,
* Touch Events,
* Event Source ([http://www.w3.org/TR/eventsource/ W3C document]), see also [https://developer.mozilla.org/en-US/docs/Web/API/EventSource MDN],
* Web workers
* Better developer tools (not only Firebug)