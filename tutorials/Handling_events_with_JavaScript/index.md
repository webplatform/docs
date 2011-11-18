== Introduction ==
 
Now you are comfortable with using CSS for styling and layout, and have taken your first stumbling steps with understanding variables, functions, methods, etc. in JavaScript, it is time to start using that knowledge to provide your site visitors with interactivity and dynamic behavior (such as dragging and dropping, animation, etc). Controlling events with JavaScript allows you to step into the role as Doctor Frankenstein and really give life to your creations!
 
But enough about the joys of JavaScript—this [http://www.w3.org/wiki/Web_Standards_Curriculum Web Standards Curriculum] article will get practical, telling you what events are and how to make use of them on your pages.
 
Bear in mind that you can [http://dev.opera.com/articles/view/handling-events-with-javascript/code-example.zip download the code example for this article] and try it out for yourself.

== What are events? ==
 
Events occur when some sort of interaction takes place in a web page. This can be the end user clicking on something, moving the mouse over a certain element or pressing down certain keys on the keyboard. An event can also be something that happens in the web browser, such as the web page completing the loading of a page, or the user scrolling or resizing the window.
 
Through the use of JavaScript, you can detect when certain events happen, and cause things to occur in response to those events.

== How events work ==
 
When events happen to an HTML element in a web page, it checks to see if any event handlers are attached to it. If the answer is yes, it calls them in respective order, while sending along references and further information for each event that occurred. The event handlers then act upon the event.
 
There are two types of event order: ''event capturing'' and ''event bubbling''.
 
Event capturing starts with the outer most element in the DOM and works inwards to the HTML element the event took place on and then out again. For example, a click in a web page would first check the <code>HTML</code> element for <code>onclick</code> event handlers, then the <code>body</code> element, and so on, until it reaches the target of the event.
 
Event bubbling works in exactly the opposite manner: it begins by checking the target of the event for any attached event handlers, then bubbles up through each respective parent element until it reaches the HTML element.

== The evolution of events ==
 
In the early days of JavaScripting, we used event handlers directly within the HTML element, like this:
 
<pre>&lt;a href="http://www.opera.com/" onclick="alert('Hello')"&gt;Say hello&lt;/a&gt;</pre>
 
The problem with this approach is that it resulted in event handlers spread throughout the code, no central control and missing out on web browsers' caching features when it comes to external JavaScript file includes.

The next step in event evolution was to apply events from within a JavaScript block, for example:
 
<pre>&lt;script type="text/javascript"&gt;
  document.getElementById("my-link").onclick = waveToAudience;
    function waveToAudience() {
      alert("Waving like I've never waved before!");
    }
&lt;/script&gt;

&lt;a id="my-link" href="http://www.opera.com/"&gt;My link&lt;/a&gt;</pre>
 
Note the clean HTML in the last example. This is generally what’s referred to as unobtrusive JavaScript. The benefit of this, besides JavaScript caching and code control, is code separation: you have all your content in one location and your interaction code in another. This also allows for a more accessible approach where the link will work perfectly fine with JavaScript disabled; it is also something that will please search engines.

=== DOM Level 2 Events ===
 
Back in November in 2000, the Document Object Model (DOM) Level 2 Events Specification was released by the W3C, offering a more detailed and granular way to control events in a web page. The new way to apply events to HTML elements looked like this:
 
<pre>document.getElementById("my-link").addEventListener("click", myFunction, false);</pre>
 
The first parameter of the <code>addEventListener method</code> is the name of the event, and you should note that it no longer uses the “on” prefix. The second parameter is a reference to the function we want to call when the event occurs. The third parameter controls the so-called <code>useCapture</code> of the event, ie if event capturing or event bubbling should be used.

The counterpart of <code>addEventListener</code> is <code>removeEventListener</code>, which removes any applied event from an HTML element.
 
=== Internet Explorer event model exception ===
 
Unfortunately, Internet Explorer has so far not implemented the DOM Level 2 event model, and instead has its own proprietary <code>attachEvent</code> method. It looks like this in action:
 
<pre>document.getElementById("my-link").attachEvent("onclick", myFunction);</pre>
 
Note that the <code>attachEvent</code> still uses the "on" prefix before the name of the actual event, and it doesn't include any support for deciding the capture phase.

The counterpart of <code>attachEvent</code> is <code>detachEvent</code>, to remove any applied event from an HTML element.
 
=== Applying events cross-browser ===
 
With the inconsistencies between web browsers in event handling implementations, there have been numerous attempts from web developers to offer a good solution for applying events sucessfully across all major browsers. These solutions have different pros and cons, and are usually referred to as <code>addEvent</code> functions.
 
Most major JavaScript libraries have these built in, and there are also a number of stand-alone solutions available online. One suggestion is to use [http://dean.edwards.name/weblog/2005/10/add-event/ addEvent by Dean Edwards]; you should also consider looking at something like [http://docs.jquery.com/Events event handling options with the jQuery JavaScript library].

== Events and accessibility ==
 
Before we delve deeper into explaining how to control and call events, I just want to emphasize accessibility. While it’s normally a broad term for most people, I use it here to convey that what you want to do through the usage of events really should work when JavaScript is disabled or for other reasons blocked in the web browser.
 
Some people do turn off JavaScript in their web browsers, but more commonly proxy servers, firewalls and overzealous antivirus programs stop JavaScript from behaving as expected. Don’t let this discourage you; my aim is to guide you through creating events that have an accessible fallback in case of JavaScript not being available.
 
In general, never apply events to HTML elements that don’t already have a built-in behavior for that certain event. You should only apply <code>onclick</code> events to elements like <code>a</code>, which already have a fallback behavior for click events (eg browsing to the location specified in the link, or submitting a form).
 
== Controlling events ==
 
Let’s start out with a simple example of an event, and how you can react to it. For the sake of simplicity, I will be using the <code>addEvent</code> solution referred to above, to avoid delving into the intricacies of cross-browser workarounds in each example.
 
Our first example is the <code>onload</code> event, which belongs to the <code>window</code> object. Generally, any events that affect the browser window (like <code>onload</code>, <code>onresize</code> and <code>onscroll</code>) are available through the <code>window</code> object.
 
The <code>onload</code> event takes place when everything in the web page has completely loaded. This includes the HTML code itself as well as external dependencies such as images, CSS files and JavaScript files. When all of them have finished loading, <code>window.onload</code> gets called, and you can trigger web page functionality to occur. The following very simple example makes an alert message appear when the page has loaded:
 
<pre>addEvent(window, "load", sayHi);
function sayHi() {
  alert("Hello there, stranger!");	
}</pre>
 
That wasn’t too bad, right? If you want to, you can use so-called anonymous functions instead, eliminating the need for a name for your function. Like this:

<pre>addEvent(window, "load", function () {
  alert("Hello there, stranger!");	
});</pre>
 
=== Applying events to certain elements ===
 
To take this further, we should start by looking into adding events to some other elements on the page. For the sake of argument, let’s suppose you want to have an event happen every time a link is clicked. Combining this with what we learned above, this would be the way to go about it:

<pre>addEvent(window, "load", function () {
  var links = document.getElementsByTagName("a");
    for (var i=0; i&lt;links.length; i++) {
      addEvent(links[i], "click", function () {
        alert("NOPE! I won't take you there!");

        // This line's support added through the addEvent function. See below.
      evt.preventDefault(); 
    });
  }
});</pre>
 
Ok, what just happened? First we used the <code>onload</code> event to check when the web page had completely loaded. Then we found all the links in the page by using the <code>getElementsByTagName</code> method of the <code>document</code> object. With an established reference to them, we looped through all links and applied an event to them to cause an action to occur once they were clicked.

But what about the cheeky “won’t take you there” part? After the <code>alert</code> has been shown, the line below reads <code>return false</code>. This means that within that context, returning false prevents the default action. We’ll get into other ways to dictate how events behave in the last section of this article.
 
== Event object references ==
 
To add more detail to your event handling, you can take different actions depending on certain properties of the event that took place. For instance, if you are dealing with an <code>onkeypress</code>, you might want the event to occur only if the user presses the enter key, but no other keys.
 
As with the event model, Internet Explorer has decided to use a global event object called <code>event</code> for handling objects, while the W3C-recommended way implemented by all other web browsers is passing event objects belonging just to that specific event. The most common problem with implementing such functionality across browsers is getting a reference to the event itself, and a reference to the element that the event is targeting. This code solves that for you:
 
<pre>addEvent(document.getElementById("check-it-out"), "click", eventCheck);
function eventCheck (evt) {
  var eventReference = (typeof evt !== "undefined")? evt : event;
  var eventTarget = (typeof eventReference.target !== "undefined")? eventReference.target : eventReference.srcElement;
}</pre>
 
The first line in the <code>eventCheck</code> function checks if there’s an event object passed along to the function. If yes, it automatically becomes the first parameter of the function, hence getting the name <code>evt</code> in this example. If it doesn’t exist, meaning that the current web browser is Internet Explorer, it refers to a global property of the <code>window</code> object named <code>event</code>.

The second line looks for a <code>target</code> property on the established event reference. If it doesn’t exist, it falls back to the <code>srcElement</code> property implemented by Internet Explorer.
 
Note: this control and behavior is also addressed with the above referenced [http://dean.edwards.name/weblog/2005/10/add-event/ addEvent] function, where the event object has been normalized to work the same in all web browsers. The above code is written out as if this is not the case, though, to give you an insight into web browser differences.
 
=== Checking an event-specific property ===
 
Let’s put this into action. The following example executes a different code block depending on what key was pressed:
 
<pre>addEvent(document.getElementById("user-name"), "keyup", whatKey);
function whatKey (evt) {
  var eventReference = (typeof evt !== "undefined")? evt : event;
  var keyCode = eventReference.keyCode;
  if (keyCode === 13) {
    // The Enter key was pressed
    // Code to validate the form and then submit it
  }
  else if (keyCode === 9) {
    // The Tab key was pressed
    // Code to, perhaps, clear the field
  }
}</pre>
 
The code inside the <code>whatKey</code> function checks a property on the event that took place, namely <code>keyCode</code>, to see which key was actually pressed on the keyboard. The number 13 means the Enter key and the number 9 means the Tab key.

== Event defaults and event bubbling ==
 
There are a number of cases where you would be interested in stopping the default behavior of an event. For instance, you might want to prevent the user from submitting a form if certain fields aren’t filled out. The same goes for event bubbling, and this part will explain how you can take control of such situations.
 
=== Preventing the default behavior of events ===
 
Just as with event model and event object differences, there are two ways to go about this to support IE, and all other browsers. Building on the previous code for getting an event object reference, the next listing includes code to stop the default link behaviour occuring when links are clicked:
 
<pre>addEvent(document.getElementById("stop-default"), "click", stopDefaultBehavior);
function stopDefaultBehavior (evt) {
  var eventReference = (typeof evt !== "undefined")? evt : event;
  if (eventReference.preventDefault) {
    eventReference.preventDefault();
  }
  else {
    eventReference.returnValue = false;
  }
}</pre>
 
This approach uses something called object detection, to confirm that a method is actually available before it is called, which helps prevent possible errors. The <code>preventDefault</code> method is available in every web browser but Internet Explorer, and it prevents the default action of an event from happening.

If that method isn’t supported, it falls back to setting the <code>returnValue</code> of the global event object to <code>false</code>, thus stopping the default behaviour in Internet Explorer.
 
=== Stopping event bubbling ===
 
Consider the following HTML hierarchy:
 
<pre>&lt;div&gt;
  &lt;ul&gt;
    &lt;li&gt;
      &lt;a href="http://www.opera.com/" id="stop-default"&gt;Opera&lt;/a&gt;
    &lt;/li&gt;
    &lt;li&gt;
      &lt;a href="http://www.opera.com/products/dragonfly/" id="stop-default"&gt;Opera Dragonfly&lt;/a&gt;
    &lt;/li&gt;
  &lt;/ul&gt;	
&lt;/div&gt;</pre>
 
Suppose you had applied an <code>onclick</code> event to all the <code>a</code> elements, <code>li</code> elements and the <code>ul</code> element. The <code>onclick</code> event would first call the event handler of the link, then the list items, and finally the event handler of the unordered list.

If the user clicks the link, most likely, you don’t want to call any possible event handler for the parent <code>li</code> element, but instead just let the user navigate to the corresponding page. However, if the user clicks the <code>li</code> item beside the link, you might want to trigger an event handler for the <code>li</code> as well as the <code>ul</code> element.
 
Note that with the DOM level 2 Event Model and <code>useCapture</code> enabled, ie using event capturing, it would start with the unordered list, then the list item and finally the link. However, since event capturing isn’t an option in Internet Explorer, this functionality is very seldom used in real practice.
 
Here’s how to write code to stop the bubbling of an event:
 
<pre>addEvent(document.getElementById("stop-default"), "click", cancelEventBubbling);
function cancelEventBubbling (evt) {
  var eventReference = (typeof evt !== "undefined")? evt : event;
  if (eventReference.stopPropagation) {
    eventReference.stopPropagation();
  }
  else {
    eventReference.cancelBubble = true;
  }
}</pre>
 
== Complete event handling example ==
 
I have put together [http://dev.opera.com/articles/view/handling-events-with-javascript/javascript-event-handling-example.html an example page] showcasing adding an event handler and preventing that event’s default action, depending on certain criteria. The event handler checks whether a form is allowed to be submitted or not depending on if the user has filled out all fields. The JavaScript code is as follows:

<pre>addEvent(window, "load", function () {
  var contactForm = document.getElementById("contact-form");
  if (contactForm) {
    addEvent(contactForm, "submit", function (evt) {
      var firstName = document.getElementById("first-name");
      var lastName = document.getElementById("last-name");
      if (firstName &amp;&amp; lastName) {
        if (firstName.value.length === 0 || lastName.value.length === 0) {
          alert("You have to fill in all fields, please.");
          evt.preventDefault();
        }
      }
    });
  }
});</pre>

== Summary ==
 
I have merely scratched the surface of event handling in this article, but I hope you have gained a good understanding of how events work. I might have been a little hard on you with web browser inconsistencies, but my belief is that it’s very important to know these issues from the start.

Once you have accepted these issues and learned to master the solutions above, there’s no end to the possibilities you can achieve with JavaScript and event handling!
 
== Exercise questions ==
 
* What is an event?
* What’s the difference between event capture and event bubbling?
* Is it possible to control the execution of an event, ie stopping the default behavior. How?
* What’s the main problem with the [http://dev.opera.com/articles/view/handling-events-with-javascript/javascript-event-handling-example.html attachEvent] and scope, which triggered a JavaScript web community contest?

Note: This material was originally published as part of the Opera Web Standards Curriculum, available as [http://dev.opera.com/articles/view/handling-events-with-javascript/ 49 - Handling events with JavaScript], written by Robert Nyman. Like the original, it is published under the [http://creativecommons.org/licenses/by-nc-sa/2.5/ Creative Commons Attribution, Non Commercial - Share Alike 2.5] license.

[[Category:Tutorials]]
[[Category:WSC]]
[[Category:Scripting]]