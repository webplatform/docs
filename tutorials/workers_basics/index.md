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

==Getting Started==

Web Workers run in an isolated thread. As a result, the code that they execute needs to be contained in a separate file. But before we do that, the first thing to do is create a new <code>Worker</code> object in your main page. The constructor takes the name of the worker script:

<pre>
 var worker = new Worker('task.js');
</pre>

If the specified file exists, the browser will spawn a new worker thread, which is downloaded asynchronously. The worker will not begin until the file has completely downloaded and executed. If the path to your worker returns an 404, the worker will fail silently.

After creating the worker, start it by calling the <code>postMessage()</code> method:

<pre>
 worker.postMessage(); // Start the worker.
</pre>

==Getting Started==

Web Workers run in an isolated thread. As a result, the code that they execute needs to be contained in a separate file. But before we do that, the first thing to do is create a new <code>Worker</code> object in your main page. The constructor takes the name of the worker script:

<pre>
 var worker = new Worker('task.js');
</pre>

If the specified file exists, the browser will spawn a new worker thread, which is downloaded asynchronously. The worker will not begin until the file has completely downloaded and executed. If the path to your worker returns an 404, the worker will fail silently.

After creating the worker, start it by calling the <code>postMessage()</code> method:

<pre>
 worker.postMessage(); // Start the worker.
</pre>

===Communicating with a Worker via Message Passing===

Communication between a worker and its parent page is done using an event model and the <code>postMessage()</code> method. Depending on your browser/version, <code>postMessage()</code> can accept either a string or JSON object as its single argument. 

Below is a example of using a string to pass "Hello World" to a worker in doWork.js. The worker simply returns the message that is passed to it. 

Main script:

<pre>
 var worker = new Worker('doWork.js');
 
 worker.addEventListener('message', function(e) {
   console.log('Worker said: ', e.data);
 }, false);
 
 worker.postMessage('Hello World'); // Send data to our worker.
</pre>

doWork.js (the worker):

<pre>
 self.addEventListener('message', function(e) {
   self.postMessage(e.data);
 }, false);
</pre>

When <code>postMessage()</code> is called from the main page, our worker handles that message by defining an <code>onmessage</code> handler for the <code>message</code> event. The message payload (in this case "Hello World") is accessible in <code>Event.data</code>. Although this particular example isn't very exciting, it demonstrates that <code>postMessage()</code> is also your means for passing data back to the main thread. Convenient!

Messages passed between the main page and workers are copied, not shared. For example, in the next example the <code>msg</code> property of the JSON message is accessible in both locations. It appears that the object is being passed directly to the worker even though it's running in a separate, dedicated space. In actuality, what is happening is that the object is being serialized as it's handed to the worker and subsequently de-serialized on the other end. The page and worker do not share the same instance, so the end result is that a duplicate is created on each pass. Most browsers implement this feature by automatically JSON encoding/decoding the value on either end.

The following is a more complex example that passes messages using JSON objects.


==Getting Started==

Web Workers run in an isolated thread. As a result, the code that they execute needs to be contained in a separate file. But before we do that, the first thing to do is create a new <code>Worker</code> object in your main page. The constructor takes the name of the worker script:

<pre>
 var worker = new Worker('task.js');
</pre>

If the specified file exists, the browser will spawn a new worker thread, which is downloaded asynchronously. The worker will not begin until the file has completely downloaded and executed. If the path to your worker returns an 404, the worker will fail silently.

After creating the worker, start it by calling the <code>postMessage()</code> method:

<pre>
 worker.postMessage(); // Start the worker.
</pre>

===Communicating with a Worker via Message Passing===

Communication between a worker and its parent page is done using an event model and the <code>postMessage()</code> method. Depending on your browser/version, <code>postMessage()</code> can accept either a string or JSON object as its single argument. 

Below is a example of using a string to pass "Hello World" to a worker in doWork.js. The worker simply returns the message that is passed to it. 

Main script:

<pre>
 var worker = new Worker('doWork.js');
 
 worker.addEventListener('message', function(e) {
   console.log('Worker said: ', e.data);
 }, false);
 
 worker.postMessage('Hello World'); // Send data to our worker.
</pre>

doWork.js (the worker):

<pre>
 self.addEventListener('message', function(e) {
   self.postMessage(e.data);
 }, false);
</pre>

When <code>postMessage()</code> is called from the main page, our worker handles that message by defining an <code>onmessage</code> handler for the <code>message</code> event. The message payload (in this case "Hello World") is accessible in <code>Event.data</code>. Although this particular example isn't very exciting, it demonstrates that <code>postMessage()</code> is also your means for passing data back to the main thread. Convenient!

Messages passed between the main page and workers are copied, not shared. For example, in the next example the <code>msg</code> property of the JSON message is accessible in both locations. It appears that the object is being passed directly to the worker even though it's running in a separate, dedicated space. In actuality, what is happening is that the object is being serialized as it's handed to the worker and subsequently de-serialized on the other end. The page and worker do not share the same instance, so the end result is that a duplicate is created on each pass. Most browsers implement this feature by automatically JSON encoding/decoding the value on either end.

The following is a more complex example that passes messages using JSON objects.

Main script:

<pre>
 &lt;button onclick="sayHI()"&gt;Say HI&lt;/button&gt;
 &lt;button onclick="unknownCmd()"&gt;Send unknown command&lt;/button&gt;
 &lt;button onclick="stop()"&gt;Stop worker&lt;/button&gt;
 &lt;output id="result"&gt;&lt;/output&gt;
 
 &lt;script&gt;
   function sayHI() {
     worker.postMessage({'cmd': 'start', 'msg': 'Hi'});
   }
 
   function stop() {
     // Calling worker.terminate() from this script would also stop the worker.
     worker.postMessage({'cmd': 'stop', 'msg': 'Bye'});
   }
 
   function unknownCmd() {
     worker.postMessage({'cmd': 'foobard', 'msg': '???'});
   }
 
   var worker = new Worker('doWork2.js');
 
   worker.addEventListener('message', function(e) {
     document.getElementById('result').textContent = e.data;
   }, false);
 &lt;/script&gt;
</pre>

doWork2.js:

<pre>
 self.addEventListener('message', function(e) {
   var data = e.data;
   switch (data.cmd) {
     case 'start':
       self.postMessage('WORKER STARTED: ' + data.msg);
       break;
     case 'stop':
       self.postMessage('WORKER STOPPED: ' + data.msg + '. (buttons will no longer work)');
       self.close(); // Terminates the worker.
       break;
     default:
       self.postMessage('Unknown command: ' + data.msg);
   };
 }, false);
</pre>

'''Note''': There are two ways to stop a worker, by calling <code>worker.terminate()</code> from the main page or by calling <code>self.close()</code> inside of the worker itself.

'''Example''': Run this worker 
[http://www.html5rocks.com/en/tutorials/workers/basics/ here]!

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