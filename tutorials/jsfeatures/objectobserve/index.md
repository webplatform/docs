{{Page_Title|Respond to change with Object.observe}}
{{Flags
|Checked_Out=No
}}
{{Byline
|Name=Alex Danilo
|URL=http://www.html5rocks.com/profiles/#alexdanilo
|Published=28 November 2012
}}
{{Summary_Section|'''Object.observe()''' lets you add a listener to any JavaScript object that gets called whenever that object, or its properties, change.}}
{{Tutorial
|Content===Introduction==
Lots of JavaScript frameworks using MVC or MDV need to respond to changes to the objects that model the state inside a web application. This capability is a fundamental part of a data-binding model.

There are a number of different ways to monitor JavaScript objects and DOM properties to trigger some sort of action, but most of the techniques aren’t ideal for various reasons such as performance, etc.

In order to improve the performance of web applications, a new method called [http://wiki.ecmascript.org/doku.php?id=harmony:observe Object.observe()] has been proposed to TC39 – the standards body overseeing development of ECMAScript (JavaScript).

Object.observe() lets you add a listener to any JavaScript object that gets called whenever that object, or its properties, change.

==Compatibility==
You can try it out now in [https://tools.google.com/dlpage/chromesxs Chrome Canary].

To experiment with this feature, you need to enable the Enable Experimental JavaScript flag in Chrome Canary and restart the browser. The flag can be found under 'chrome://flags’ as shown in the image below:

[[Image:objectobserve1.jpg]]

==Basic use==
Here’s a simple example of how to set up an observer on an object:

<pre>
var beingWatched = {};
// Define callback function to get notified on changes
function somethingChanged(changes) {
    // do something
}
Object.observe(beingWatched, somethingChanged);
</pre>

When the object 'beingWatched’ is modified, it will trigger the callback function 'somethingChanged’ which receives an array of changes that were applied to the object.

So the JavaScript engine is free to buffer up a number of changes and pass them all in a single call to the callback function. This helps with optimizing the callbacks so that your code can do lots of JavaScript manipulation but process only a few callbacks by batching the updates together.

The callback function will be triggered whenever a property is added, modified, deleted or reconfigured.

==Observing multiple changes==
Another really nice thing when observing arrays is that if an array has had a number of changes made to it, you can use a [https://github.com/rafaelw/ChangeSummary Change Summary] helper library to create a minimal change set, so that client side JavaScript doesn’t have to manually scan the array to check each item.

You can iterate through each change quite easily, by doing something like the following in your 'somethingChanged’ callback function:

<pre>
function whatHappened(change) {
    console.log(change.name + " was " + change.type + " and is now " + change.object[change.name]);
}
function somethingChanged(changes) {
    changes.forEach(whatHappened);
}
</pre>

The <code>type</code> property identifies what happened to the object. Some examples of properties being set and the associated type can be seen in the code below:

<pre>
beingWatched.a = "foo"; // new
beingWatched.a = "bar"; // updated
beingWatched.a = "bar"; // no change
beingWatched.b = "amazing"; // new
</pre>

The great thing about this technique is that all the monitoring smarts are inside the JavaScript engine which allows the browser to optimize it well and free your JavaScript up to implement functionality taking advantage of this feature.

==Calling the debugger==
Another really great feature for development is the ability to use Object.observe() to trigger the debugger whenever an object changes. To do that you’d use code something like the example below:

<pre>
Object.observe(beingWatched, function(){ debugger; });
</pre>

==More information==
[https://www.youtube.com/watch?feature=player_embedded&v=VO--VXFJnmE Here’s a great video introduction] about Object.observe() that explains it in detail.

There’s also a [http://weblog.bocoup.com/JavaScript-object-observe/ nice descriptive write-up here] and a [http://simpl.info/observe/ working example here].

==Conclusion==
The TC39 standards body is seeking feedback on this feature, so go ahead and try it and let us know what you think.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
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