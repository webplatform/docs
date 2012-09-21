{{Flags
|High-level issues=Stub
}}
{{Summary_Section}}
{{Tutorial
|Content==The Basics of Web Workers=

====original by Eric Bidelman====
====published July 26, 2010, updated Aug. 21, 2012====

==The Problem: JavaScript Concurrency==

There are a number of bottlenecks preventing interesting applications from being ported (say, from server-heavy implementations) to client-side JavaScript. Some of these include browser compatibility, static typing, accessibility, and performance. Fortunately, the latter is quickly becoming a thing of the past as browser vendors rapidly improve the speed of their JavaScript engines.

One thing that's remained a hindrance for JavaScript is actually the language itself. JavaScript is a single-threaded environment, meaning multiple scripts cannot run at the same time. As an example, imagine a site that needs to handle UI events, query and process large amounts of API data, and manipulate the DOM. Pretty common, right? Unfortunately all of that can't be done simultaneously due to limitations in browsers' JavaScript runtimes. Script execution happens within a single thread.

Developers mimic concurrency by using techniques like <code>setTimeout()</code>, <code>setInterval()</code>, <code>XMLHttpRequest</code>, and event handlers. Yes, all of these features run asynchronously, but non-blocking doesn't necessarily mean concurrency. Asynchronous events are processed after the current executing script has yielded. The good news is that HTML5 gives us something better than these hacks!

==Introducing Web Workers: Bring Threading to JavaScript==

The [http://www.whatwg.org/specs/web-workers/current-work/ Web Workers] specification defines an API for spawning background scripts in your web application. Web Workers allow you to do things like fire up long-running scripts to handle computationally intensive tasks, but without blocking the UI or other scripts to handle user interactions. They're going to help put and end to that nasty "unresponsive script" dialog that we've all come to love:

[[Image:unresponsivescript.png|Unresponsive script dialog]]
''Common unresponsive script dialog''

Web Workers utilize thread-like message passing to achieve parallelism. They're perfect for keeping your UI refresh, performant, and responsive for users.

===Types of Web Workers===

It's worth noting that the [http://www.whatwg.org/specs/web-workers/current-work/ specification] discusses two kinds of Web Workers, [http://www.whatwg.org/specs/web-workers/current-work/#dedicated-workers-and-the-worker-interface Dedicated Workers] and [http://www.whatwg.org/specs/web-workers/current-work/#sharedworker Shared Workers]. This article will only cover Dedicated Workers, and will refer to them as "web workers" or "workers" throughout.



}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}