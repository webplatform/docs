---
title: Events in JavaScript
readiness: 'Ready to Use'
summary: 'This articles shows how to handle events in JavaScript, such as a user clicking a button, and perform actions in response.'
tags:
  - Tutorials
  - JavaScript
uri: 'tutorials/events in javascript'

---
## <span>Summary</span>

This articles shows how to handle events in JavaScript, such as a user clicking a button, and perform actions in response.

## <span>Introduction</span>

Now you are comfortable with using CSS for styling and layout, and have taken your first stumbling steps with understanding variables, functions, methods, etc. in JavaScript, it is time to start using that knowledge to provide your site visitors with interactivity and dynamic behavior (such as dragging and dropping, animation, etc). Controlling events with JavaScript allows you to step into the role as Doctor Frankenstein and really give life to your creations!

But enough about the joys of JavaScript—this [Web Standards Curriculum](http://www.w3.org/wiki/Web_Standards_Curriculum) article will get practical, telling you what events are and how to make use of them on your pages.

Bear in mind that you can [download the code example for this article](http://dev.opera.com/articles/view/handling-events-with-javascript/code-example.zip) and try it out for yourself.

## <span>What are events?</span>

Events occur when some sort of interaction takes place in a web page. This can be the end user clicking on something, moving the mouse over a certain element or pressing down certain keys on the keyboard. An event can also be something that happens in the web browser, such as the web page completing the loading of a page, or the user scrolling or resizing the window.

Through the use of JavaScript, you can detect when certain events happen, and cause things to occur in response to those events.

## <span>How events work</span>

When events happen to an HTML element in a web page, it checks to see if any event handlers are attached to it. If the answer is yes, it calls them in respective order, while sending along references and further information for each event that occurred. The event handlers then act upon the event.

There are two types of event order: *event capturing* and *event bubbling*.

Event capturing starts with the outer most element in the DOM and works inwards to the HTML element the event took place on and then out again. For example, a click in a web page would first check the `HTML` element for `onclick` event handlers, then the `body` element, and so on, until it reaches the target of the event.

Event bubbling works in exactly the opposite manner: it begins by checking the target of the event for any attached event handlers, then bubbles up through each respective parent element until it reaches the HTML element.

## <span>The evolution of events</span>

In the early days of JavaScripting, we used event handlers directly within the HTML element, like this:

``` html
<a href="http://www.opera.com/" onclick="alert('Hello')">Say hello</a>
```

 The problem with this approach is that it resulted in event handlers spread throughout the code, no central control and missing out on web browsers' caching features when it comes to external JavaScript file includes.

The next step in event evolution was to apply events from within a JavaScript block, for example:

``` html
<script type="text/javascript">
  document.getElementById("my-link").onclick = waveToAudience;
    function waveToAudience() {
      alert("Waving like I've never waved before!");
    }
</script>

<a id="my-link" href="http://www.opera.com/">My link</a>
```

 Note the clean HTML in the last example. This is generally what’s referred to as unobtrusive JavaScript. The benefit of this, besides JavaScript caching and code control, is code separation: you have all your content in one location and your interaction code in another. This also allows for a more accessible approach where the link will work perfectly fine with JavaScript disabled; it is also something that will please search engines.

### <span>DOM Level 2 Events</span>

Back in November in 2000, the Document Object Model (DOM) Level 2 Events Specification was released by the W3C, offering a more detailed and granular way to control events in a web page. The new way to apply events to HTML elements looked like this:

``` js
document.getElementById("my-link").addEventListener("click", myFunction, false);
```

 The first parameter of the `addEventListener method` is the name of the event, and you should note that it no longer uses the “on” prefix. The second parameter is a reference to the function we want to call when the event occurs. The third parameter controls the so-called `useCapture` of the event, ie if event capturing or event bubbling should be used.

The counterpart of `addEventListener` is `removeEventListener`, which removes any applied event from an HTML element.

### <span>Internet Explorer event model exception</span>

Unfortunately, Internet Explorer has so far not implemented the DOM Level 2 event model, and instead has its own proprietary `attachEvent` method. It looks like this in action:

``` js
document.getElementById("my-link").attachEvent("onclick", myFunction);
```

 Note that the `attachEvent` still uses the "on" prefix before the name of the actual event, and it doesn't include any support for deciding the capture phase.

The counterpart of `attachEvent` is `detachEvent`, to remove any applied event from an HTML element.

### <span>Applying events cross-browser</span>

With the inconsistencies between web browsers in event handling implementations, there have been numerous attempts from web developers to offer a good solution for applying events sucessfully across all major browsers. These solutions have different pros and cons, and are usually referred to as `addEvent` functions.

Most major JavaScript libraries have these built in, and there are also a number of stand-alone solutions available online. One suggestion is to use [addEvent by Dean Edwards](http://dean.edwards.name/weblog/2005/10/add-event/); you should also consider looking at something like [event handling options with the jQuery JavaScript library](http://docs.jquery.com/Events).

## <span>Events and accessibility</span>

Before we delve deeper into explaining how to control and call events, I just want to emphasize accessibility. While it’s normally a broad term for most people, I use it here to convey that what you want to do through the usage of events really should work when JavaScript is disabled or for other reasons blocked in the web browser.

Some people do turn off JavaScript in their web browsers, but more commonly proxy servers, firewalls and overzealous antivirus programs stop JavaScript from behaving as expected. Don’t let this discourage you; my aim is to guide you through creating events that have an accessible fallback in case of JavaScript not being available.

In general, never apply events to HTML elements that don’t already have a built-in behavior for that certain event. You should only apply `onclick` events to elements like `a`, which already have a fallback behavior for click events (eg browsing to the location specified in the link, or submitting a form).

## <span>Controlling events</span>

Let’s start out with a simple example of an event, and how you can react to it. For the sake of simplicity, I will be using the `addEvent` solution referred to above, to avoid delving into the intricacies of cross-browser workarounds in each example.

Our first example is the `onload` event, which belongs to the `window` object. Generally, any events that affect the browser window (like `onload`, `onresize` and `onscroll`) are available through the `window` object.

The `onload` event takes place when everything in the web page has completely loaded. This includes the HTML code itself as well as external dependencies such as images, CSS files and JavaScript files. When all of them have finished loading, `window.onload` gets called, and you can trigger web page functionality to occur. The following very simple example makes an alert message appear when the page has loaded:

``` js
addEvent(window, "load", sayHi);
function sayHi() {
  alert("Hello there, stranger!");
}
```

 That wasn’t too bad, right? If you want to, you can use so-called anonymous functions instead, eliminating the need for a name for your function. Like this:

``` js
addEvent(window, "load", function () {
  alert("Hello there, stranger!");
});
```

### <span>Applying events to certain elements</span>

To take this further, we should start by looking into adding events to some other elements on the page. For the sake of argument, let’s suppose you want to have an event happen every time a link is clicked. Combining this with what we learned above, this would be the way to go about it:

``` js
addEvent(window, "load", function () {
  var links = document.getElementsByTagName("a");
    for (var i=0; i<links.length; i++) {
      addEvent(links[i], "click", function () {
        alert("NOPE! I won't take you there!");

        // This line's support added through the addEvent function. See below.
      evt.preventDefault();
    });
  }
});
```

 Ok, what just happened? First we used the `onload` event to check when the web page had completely loaded. Then we found all the links in the page by using the `getElementsByTagName` method of the `document` object. With an established reference to them, we looped through all links and applied an event to them to cause an action to occur once they were clicked.

But what about the cheeky “won’t take you there” part? After the `alert` has been shown, the line below reads `return false`. This means that within that context, returning false prevents the default action. We’ll get into other ways to dictate how events behave in the last section of this article.

## <span>Event object references</span>

To add more detail to your event handling, you can take different actions depending on certain properties of the event that took place. For instance, if you are dealing with an `onkeypress`, you might want the event to occur only if the user presses the enter key, but no other keys.

As with the event model, Internet Explorer has decided to use a global event object called `event` for handling objects, while the W3C-recommended way implemented by all other web browsers is passing event objects belonging just to that specific event. The most common problem with implementing such functionality across browsers is getting a reference to the event itself, and a reference to the element that the event is targeting. This code solves that for you:

``` js
addEvent(document.getElementById("check-it-out"), "click", eventCheck);
function eventCheck (evt) {
  var eventReference = (typeof evt !== "undefined")? evt : event;
  var eventTarget = (typeof eventReference.target !== "undefined")? eventReference.target : eventReference.srcElement;
}
```

 The first line in the `eventCheck` function checks if there’s an event object passed along to the function. If yes, it automatically becomes the first parameter of the function, hence getting the name `evt` in this example. If it doesn’t exist, meaning that the current web browser is Internet Explorer, it refers to a global property of the `window` object named `event`.

The second line looks for a `target` property on the established event reference. If it doesn’t exist, it falls back to the `srcElement` property implemented by Internet Explorer.

Note: this control and behavior is also addressed with the above referenced [addEvent](http://dean.edwards.name/weblog/2005/10/add-event/) function, where the event object has been normalized to work the same in all web browsers. The above code is written out as if this is not the case, though, to give you an insight into web browser differences.

### <span>Checking an event-specific property</span>

Let’s put this into action. The following example executes a different code block depending on what key was pressed:

``` js
addEvent(document.getElementById("user-name"), "keyup", whatKey);
function whatKey (evt) {
  var eventReference = (typeof evt !== "undefined")? evt : event;
  var keyCode = eventReference.keyCode;
  if (keyCode === 13) {
    // The Enter key was pressed
    // Code to validate the form and then submit it
  }
  else if (keyCode === 9) {
    // The Tab key was pressed
    // Code to, perhaps, clear the field
  }
}
```

 The code inside the `whatKey` function checks a property on the event that took place, namely `keyCode`, to see which key was actually pressed on the keyboard. The number 13 means the Enter key and the number 9 means the Tab key.

## <span>Event defaults and event bubbling</span>

There are a number of cases where you would be interested in stopping the default behavior of an event. For instance, you might want to prevent the user from submitting a form if certain fields aren’t filled out. The same goes for event bubbling, and this part will explain how you can take control of such situations.

### <span>Preventing the default behavior of events</span>

Just as with event model and event object differences, there are two ways to go about this to support IE, and all other browsers. Building on the previous code for getting an event object reference, the next listing includes code to stop the default link behaviour occuring when links are clicked:

``` js
addEvent(document.getElementById("stop-default"), "click", stopDefaultBehavior);
function stopDefaultBehavior (evt) {
  var eventReference = (typeof evt !== "undefined")? evt : event;
  if (eventReference.preventDefault) {
    eventReference.preventDefault();
  }
  else {
    eventReference.returnValue = false;
  }
}
```

 This approach uses something called object detection, to confirm that a method is actually available before it is called, which helps prevent possible errors. The `preventDefault` method is available in every web browser but Internet Explorer, and it prevents the default action of an event from happening.

If that method isn’t supported, it falls back to setting the `returnValue` of the global event object to `false`, thus stopping the default behaviour in Internet Explorer.

### <span>Stopping event bubbling</span>

Consider the following HTML hierarchy:

``` html
<div>
  <ul>
    <li>
      <a href="http://www.opera.com/" id="stop-default">Opera</a>
    </li>
    <li>
      <a href="http://www.opera.com/products/dragonfly/" id="stop-default">Opera Dragonfly</a>
    </li>
  </ul>
</div>
```

 Suppose you had applied an `onclick` event to all the `a` elements, `li` elements and the `ul` element. The `onclick` event would first call the event handler of the link, then the list items, and finally the event handler of the unordered list.

If the user clicks the link, most likely, you don’t want to call any possible event handler for the parent `li` element, but instead just let the user navigate to the corresponding page. However, if the user clicks the `li` item beside the link, you might want to trigger an event handler for the `li` as well as the `ul` element.

Note that with the DOM level 2 Event Model and `useCapture` enabled, ie using event capturing, it would start with the unordered list, then the list item and finally the link. However, since event capturing isn’t an option in Internet Explorer, this functionality is very seldom used in real practice.

Here’s how to write code to stop the bubbling of an event:

``` js
addEvent(document.getElementById("stop-default"), "click", cancelEventBubbling);
function cancelEventBubbling (evt) {
  var eventReference = (typeof evt !== "undefined")? evt : event;
  if (eventReference.stopPropagation) {
    eventReference.stopPropagation();
  }
  else {
    eventReference.cancelBubble = true;
  }
}
```

## <span>Complete event handling example</span>

I have put together [an example page](http://dev.opera.com/articles/view/handling-events-with-javascript/javascript-event-handling-example.html) showcasing adding an event handler and preventing that event’s default action, depending on certain criteria. The event handler checks whether a form is allowed to be submitted or not depending on if the user has filled out all fields. The JavaScript code is as follows:

``` js
addEvent(window, "load", function () {
  var contactForm = document.getElementById("contact-form");
  if (contactForm) {
    addEvent(contactForm, "submit", function (evt) {
      var firstName = document.getElementById("first-name");
      var lastName = document.getElementById("last-name");
      if (firstName && lastName) {
        if (firstName.value.length === 0 || lastName.value.length === 0) {
          alert("You have to fill in all fields, please.");
          evt.preventDefault();
        }
      }
    });
  }
});
```

## <span>Summary</span>

I have merely scratched the surface of event handling in this article, but I hope you have gained a good understanding of how events work. I might have been a little hard on you with web browser inconsistencies, but my belief is that it’s very important to know these issues from the start.

Once you have accepted these issues and learned to master the solutions above, there’s no end to the possibilities you can achieve with JavaScript and event handling!

## <span>See also</span>

### <span>Exercise questions</span>

-   What is an event?
-   What’s the difference between event capture and event bubbling?
-   Is it possible to control the execution of an event, ie stopping the default behavior. How?
-   What’s the main problem with the [attachEvent](http://dev.opera.com/articles/view/handling-events-with-javascript/javascript-event-handling-example.html) and scope, which triggered a JavaScript web community contest?
