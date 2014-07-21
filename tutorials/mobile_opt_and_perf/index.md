{{Page_Title|HTML5 Techniques for Optimizing Mobile Performance}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Flags
}}
{{Byline
|Name=Wesley Hales
|URL=http://www.html5rocks.com/profiles/#wesleyhales
|Published=Sept. 19, 2011
}}
{{Summary_Section|Learn the fundamentals of an HTML5 mobile framework. From network detection to sliding, flipping, and more.}}
{{Tutorial
|Content=<h2 id="toc-introduction">Introduction</h2>

Spinning refreshes, choppy page transitions, and periodic delays in tap events are just a few of the headaches in today’s mobile web environments. Developers are trying to get as close to native as they possibly can, but are often derailed by hacks, resets, and rigid frameworks.

In this article, we will discuss the bare minimum of what it takes to create a mobile HTML5 web app. The main point is to unmask the hidden complexities which today’s mobile frameworks try to hide. You will see a minimalistic approach (using core HTML5 APIs) and basic fundamentals that will empower you to write your own framework or contribute to the one you currently use.

<h2 id="toc-hw-acceleration">Hardware acceleration</h2>

Normally, GPUs handle detailed 3D modeling or CAD diagrams, but in this case, we want our primitive drawings (divs, backgrounds, text with drop shadows, images, etc...) to appear smooth and animate smoothly via the GPU.
The unfortunate thing is that most front-end developers are dishing this animation process off to a third-party party framework without being concerned about the semantics, but should these core CSS3 features masked? Let me give you a few reasons why caring about this stuff is important:

# Memory allocation and computational burden — If you go around compositing every element in the DOM just for the sake of hardware acceleration, the next person who works on your code may chase you down and beat you severely.
# Power Consumption — Obviously, when hardware kicks in, so does the battery. When developing for mobile, developers are forced to take the wide array of device constraints into consideration while writing mobile web apps. This will be even more prevalent as browser makers start to enable access to more and more device hardware.
# Conflicts — I encountered glitchy behavior when applying hardware acceleration to parts of the page that were already accelerated. So knowing if you have overlapping acceleration is *very* important.

To make user interaction smooth and as close to native as possible, we must make the browser work for us. Ideally, we want the mobile device CPU to set up the initial animation, then have the GPU responsible for only compositing different layers during the animation process. This is what translate3d, scale3d and translateZ do — they give the animated elements their own layer, thus allowing the device to render everything together smoothly. To find out more about accelerated compositing and how WebKit works, Ariya Hidayat has [http://ariya.blogspot.com/2011/07/fluid-animation-with-accelerated.html a lot of good info] on [http://ariya.blogspot.com/ his blog].

<h2 id="toc-transitions">Page transitions</h2>

Let’s take a look at three of the most common user-interaction approaches when developing a mobile web app: slide, flip, and rotation effects.

You can view this code in action here [http://slidfast.appspot.com/slide-flip-rotate.html http://slidfast.appspot.com/slide-flip-rotate.html] (Note: This demo is built for a mobile device, so fire up an emulator, use your phone or tablet, or reduce the size of your browser window to ~1024px or less).

First, we’ll dissect the slide, flip, and rotation transitions and how they’re accelerated. Notice how each animation only takes three or four lines of CSS and JavaScript.

<h3 id="toc-sliding">Sliding</h3>

The most common of the three transition approaches, sliding page transitions mimics the native feel of mobile applications. The slide transition is invoked to bring a new content area into the view port.

For the slide effect, first we declare our markup:

<pre>
&lt;div id=&quot;home-page&quot; class=&quot;page&quot;&gt;
  &lt;h1&gt;Home Page&lt;/h1&gt;
&lt;/div&gt;

&lt;div id=&quot;products-page&quot; class=&quot;page stage-right&quot;&gt;
  &lt;h1&gt;Products Page&lt;/h1&gt;
&lt;/div&gt;

&lt;div id=&quot;about-page&quot; class=&quot;page stage-left&quot;&gt;
  &lt;h1&gt;About Page&lt;/h1&gt;
&lt;/div&gt;
</pre>

Notice how we have this concept of staging pages left or right. It could essentially be any direction, but this is most common.

We now have animation plus hardware acceleration with just a few lines of CSS. The actual animation happens when we swap classes on the page div elements.


<pre>
.page {
  position: absolute;
  width: 100%;
  height: 100%;
  /*activate the GPU for compositing each page */
  -webkit-transform: translate3d(0, 0, 0);
}
</pre>

<code>translate3d(0,0,0)</code> is known as the "silver bullet" approach.

When the user clicks a navigation element, we execute the following JavaScript to swap the classes. No third-party frameworks are being used, this is straight up JavaScript! ;)

<pre>
function getElement(id) {
  return document.getElementById(id);
}

function slideTo(id) {
  //1.) the page we are bringing into focus dictates how
  // the current page will exit. So let's see what classes
  // our incoming page is using. We know it will have stage[right&#124;left&#124;etc...]
  var classes = getElement(id).className.split(' ');

  //2.) decide if the incoming page is assigned to right or left
  // (-1 if no match)
  var stageType = classes.indexOf('stage-left');

  //3.) on initial page load focusPage is null, so we need
  // to set the default page which we're currently seeing.
  if (FOCUS_PAGE == null) {
    // use home page
    FOCUS_PAGE = getElement('home-page');
  }

  //4.) decide how this focused page should exit.
  if (stageType > 0) {
    FOCUS_PAGE.className = 'page transition stage-right';
  } else {
    FOCUS_PAGE.className = 'page transition stage-left';
  }

  //5. refresh/set the global variable
  FOCUS_PAGE = getElement(id);

  //6. Bring in the new page.
  FOCUS_PAGE.className = 'page transition stage-center';
}
</pre>

<code>stage-left</code> or <code>stage-right</code> becomes <code>stage-center</code> and forces the page to slide into the center view port. We are completely depending on CSS3 to do the heavy lifting.

<pre>
.stage-left {
  left: -480px;
}

.stage-right {
  left: 480px;
}

.stage-center {
  top: 0;
  left: 0;
}
</pre>

Next, let’s take a look at the CSS which handles mobile device detection and orientation.
We could address every device and every resolution (see [http://www.w3.org/TR/css3-mediaqueries/#resolution media query resolution]). I used just a few simple examples in this demo to cover most portrait and landscape views on mobile devices. This is also useful for applying hardware acceleration per device. For example, since the desktop version of WebKit accelerates all transformed elements (regardless if it’s 2-D or 3-D), it makes sense to create a media query and exclude acceleration at that level.
Note that hardware acceleration tricks do not provide any speed improvement under Android Froyo 2.2+. All composition is done within the software.

<pre>
/* iOS/android phone landscape screen width*/
@media screen and (max-device-width: 480px) and (orientation:landscape) {
  .stage-left {
    left: -480px;
  }

  .stage-right {
    left: 480px;
  }

  .page {
    width: 480px;
  }
}
</pre>

<h3 id="toc-flipping">Flipping</h3>

On mobile devices, flipping is known as actually swiping the page away. Here we use some simple JavaScript to handle this event on iOS and Android (WebKit-based) devices.

View it in action [http://slidfast.appspot.com/slide-flip-rotate.html http://slidfast.appspot.com/slide-flip-rotate.html].

When dealing with touch events and transitions, the first thing you’ll want is to get a handle on the current position of the element. See this doc for more information on WebKitCSSMatrix.

<pre>
function pageMove(event) {
  // get position after transform
  var curTransform = new WebKitCSSMatrix(window.getComputedStyle(page).webkitTransform);
  var pagePosition = curTransform.m41;
}
</pre>

Since we are using a CSS3 ease-out transition for the page flip, the usual <code>element.offsetLeft</code> will not work.

Next we want to figure out which direction the user is flipping and set a threshold for an event (page navigation) to take place.

<pre>
if (pagePosition &gt;= 0) {
 //moving current page to the right
 //so means we&#x27;re flipping backwards
   if ((pagePosition &gt; pageFlipThreshold) &#124;&#124; (swipeTime &lt; swipeThreshold)) {
     //user wants to go backward
     slideDirection = &#x27;right&#x27;;
   } else {
     slideDirection = null;
   }
} else {
  //current page is sliding to the left
  if ((swipeTime &lt; swipeThreshold) &#124;&#124; (pagePosition &lt; pageFlipThreshold)) {
    //user wants to go forward
    slideDirection = &#x27;left&#x27;;
  } else {
    slideDirection = null;
  }
}
</pre>

You’ll also notice that we are measuring the <code>swipeTime</code> in milliseconds as well. This allows the navigation event to fire if the user quickly swipes the screen to turn a page.

To position the page and make the animations look native while a finger is touching the screen, we use CSS3 transitions after each event firing.

<pre>
function positionPage(end) {
  page.style.webkitTransform = &#x27;translate3d(&#x27;+ currentPos + &#x27;px, 0, 0)&#x27;;
  if (end) {
    page.style.WebkitTransition = &#x27;all .4s ease-out&#x27;;
    //page.style.WebkitTransition = &#x27;all .4s cubic-bezier(0,.58,.58,1)&#x27;
  } else {
    page.style.WebkitTransition = &#x27;all .2s ease-out&#x27;;
  }
  page.style.WebkitUserSelect = &#x27;none&#x27;;
}
</pre>

I tried to play around with cubic-bezier to give the best native feel to the transitions, but ease-out did the trick.

Finally, to make the navigation happen, we must call our previously defined <code>slideTo()</code> methods that we used in the last demo.

<pre>
track.ontouchend = function(event) {
  pageMove(event);
  if (slideDirection == &#x27;left&#x27;) {
    slideTo(&#x27;products-page&#x27;);
  } else if (slideDirection == &#x27;right&#x27;) {
    slideTo(&#x27;home-page&#x27;);
  }
}
</pre>

<h3 id="toc-rotating">Rotating</h3>

Next, let’s take a look at the rotate animation being used in this demo. At any time, you can rotate the page you’re currently viewing 180 degrees to reveal the reverse side by tapping on the “Contact” menu option. Again, this only takes a few lines of CSS and some JavaScript to assign a transition class <code>onclick</code>.
NOTE: The rotate transition isn't rendered correctly on most versions of Android because it lacks 3D CSS transform capabilities. Unfortunately, instead of ignoring the flip, Android makes the page "cartwheel" away by rotating instead of flipping. We recommend using this transition sparingly until support improves.

The markup (basic concept of front and back):

<pre>
&lt;div id=&quot;front&quot; class=&quot;normal&quot;&gt;
...
&lt;/div&gt;
&lt;div id=&quot;back&quot; class=&quot;flipped&quot;&gt;
    &lt;div id=&quot;contact-page&quot; class=&quot;page&quot;&gt;
        &lt;h1&gt;Contact Page&lt;/h1&gt;
    &lt;/div&gt;
&lt;/div&gt;
</pre>

The JavaScript:

<pre>
function flip(id) {
  // get a handle on the flippable region
  var front = getElement(&#x27;front&#x27;);
  var back = getElement(&#x27;back&#x27;);

  // again, just a simple way to see what the state is
  var classes = front.className.split(&#x27; &#x27;);
  var flipped = classes.indexOf(&#x27;flipped&#x27;);

  if (flipped &gt;= 0) {
    // already flipped, so return to original
    front.className = &#x27;normal&#x27;;
    back.className = &#x27;flipped&#x27;;
    FLIPPED = false;
  } else {
    // do the flip
    front.className = &#x27;flipped&#x27;;
    back.className = &#x27;normal&#x27;;
    FLIPPED = true;
  }
}
</pre>

The CSS:

<pre>
/*----------------------------flip transition */
#back,
#front {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden;
  -webkit-transition-duration: .5s;
  -webkit-transform-style: preserve-3d;
}

.normal {
  -webkit-transform: rotateY(0deg);
}

.flipped {
  -webkit-user-select: element;
  -webkit-transform: rotateY(180deg);
}
</pre>

<h2 id="toc-debugging-hw-acceleration">Debugging hardware acceleration</h2>

Now that we have our basic transitions covered, let’s take a look at the mechanics of how they work and are composited.

To make this magical debugging session happen, let’s fire up a couple of browsers and your IDE of choice.
First start Safari from the command line to make use of some debugging environment variables. I’m on Mac, so the commands might differ based on your OS.
Open the Terminal and type the following:

* $&gt; export CA_COLOR_OPAQUE=1
* $&gt; export CA_LOG_MEMORY_USAGE=1
* $&gt; /Applications/Safari.app/Contents/MacOS/Safari

This starts Safari with a couple of debugging helpers. CA_COLOR_OPAQUE shows us which elements are actually composited or accelerated. CA_LOG_MEMORY_USAGE shows us how much memory we are using when sending our drawing operations to the [http://ariya.blogspot.com/2011/06/progressive-rendering-via-tiled-backing.html backing store]. This tells you exactly how much strain you are putting on the mobile device, and possibly give hints to how your GPU usage might be draining the target device’s battery.

Now let’s fire up Chrome so we can see some good frames per second (FPS) information:

# Open the Google Chrome web browser.
# In the URL bar, type <code>about:flags</code>.
# Scroll down a few items and click on “Enable” for FPS Counter.

Note: Do not enable the GPU compositing on all pages option. The FPS counter only appear in the left-hand corner if the browser detects compositing in your markup—and that is what we want in this case.

If you view [http://slidfast.appspot.com/slide-flip-rotate.html this page] in your souped up version of Chrome, you will see the red FPS counter in the top left hand corner.

[[File:chrome-fps.png|200x31px|Chrome FPS]]

This is how we know hardware acceleration is turned on. It also gives us an idea on how the animation runs and if you have any leaks (continuous running animations that should be stopped).

Another way to actually visualize the hardware acceleration is if you open the same page in Safari (with the environment variables I mentioned above). Every accelerated DOM element have a red tint to it. This shows us exactly what is being composited by layer.
Notice the white navigation is not red because it is not accelerated.

[[File:composited-contact.png|300px|Composited Contact Page]]

A similar setting for Chrome is also available in the <code>about:flags</code> “Composited render layer borders”.

Another great way to see the composited layers is to view the [http://www.webkit.org/blog-files/leaves/ WebKit falling leaves demo] while this mod is applied.

[[File:composited-leaves.jpeg|300px|Composited Leaves Demo]]

And finally, to truly understand the graphics hardware performance of our application, let’s take a look at how memory is being consumed.
Here we see that we are pushing 1.38MB of drawing instructions to the CoreAnimation buffers on Mac OS. The Core Animation memory buffers are shared between OpenGL ES and the GPU to create the final pixels you see on the screen.

[[File:coreanimation-1.png|500px|Coreanimation 1]]

When we simply resize or maximize the browser window, we see the memory expand as well.

[[File:coreanimation-2.png|500px|Coreanimation 2]]

This gives you an idea of how memory is being consumed on your mobile device only if you resize the browser to the correct dimensions. If you were debugging or testing for iPhone environments resize to 480px by 320px.
We now understand exactly how hardware acceleration works and what it takes to debug. It’s one thing to read about it, but to actually see the GPU memory buffers working visually really brings things into perspective.

<h2 id="toc-fetching-caching">Behind the Scenes: Fetching and Caching</h2>

Now it’s time to take our page and resource caching to the next level. Much like the approach that JQuery Mobile and similar frameworks use, we are going to pre-fetch and cache our pages with concurrent AJAX calls.

Let’s address a few core mobile web problems and the reasons why we need to do this:

* Fetching: Pre-fetching our pages allows users to take the app offline and also enables no waiting between navigation actions. Of course, we don’t want to choke the device’s bandwidth when the device comes online, so we need to use this feature sparingly.
* Caching: Next, we want a concurrent or asynchronous approach when fetching and caching these pages. We also need to use localStorage (since it’s well supported amongst devices) which unfortunately isn’t asynchronous.
* AJAX and parsing the response: Using innerHTML() to insert the AJAX response into the DOM is dangerous (and [http://martinkou.blogspot.com/2011/05/alternative-workaround-for-mobile.html unreliable]?). We instead use a [http://community.jboss.org/people/wesleyhales/blog/2011/08/28/fixing-ajax-on-mobile-devices reliable mechanism] for AJAX response insertion and handling concurrent calls. We also leverage some new features of HTML5 for parsing the <code>xhr.responseText</code>.

Building on the code from the [http://slidfast.appspot.com/slide-flip-rotate.html Slide, Flip, and Rotate demo], we start out by adding some secondary pages and linking to them. We’ll then parse the links and create transitions on the fly.

[[File:iphone-home.jpeg|372x335px|iPhone Home]]

[http://slidfast.appspot.com/fetch-cache.html View the Fetch and Cache demo here.]

As you can see, we are leveraging semantic markup here. Just a link to another page. The child page follows the same node/class structure as its parent. We could take this a step further and use the data-* attribute for “page” nodes, etc...
And here is the detail page (child) located in a separate html file (/demo2/home-detail.html) which will be loaded, cached and set up for transition on app load.

<pre>
&lt;div id=&quot;home-page&quot; class=&quot;page&quot;&gt;
  &lt;h1&gt;Home Page&lt;/h1&gt;
  &lt;a href=&quot;demo2/home-detail.html&quot; class=&quot;fetch&quot;&gt;Find out more about the home page!&lt;/a&gt;
&lt;/div&gt;
</pre>

Now lets take a look at the JavaScript. For simplicity sake, I am leaving any helpers or optimizations out of the code. All we are doing here is looping through a specified array of DOM nodes to dig out links to fetch and cache.
Note—For this demo, this method <code>fetchAndCache()</code> is being called on page load. We rework it in the next section when we detect the network connection and determine when it should be called.

<pre>
var fetchAndCache = function() {
  // iterate through all nodes in this DOM to find all mobile pages we care about
  var pages = document.getElementsByClassName(&#x27;page&#x27;);

  for (var i = 0; i &lt; pages.length; i++) {
    // find all links
    var pageLinks = pages[i].getElementsByTagName(&#x27;a&#x27;);

    for (var j = 0; j &lt; pageLinks.length; j++) {
      var link = pageLinks[j];

      if (link.hasAttribute(&#x27;href&#x27;) &amp;&amp;
      //&#x27;#&#x27; in the href tells us that this page is already loaded in the DOM - and
      // that it links to a mobile transition/page
         !(/[\#]/g).test(link.href) &amp;&amp;
        //check for an explicit class name setting to fetch this link
        (link.className.indexOf(&#x27;fetch&#x27;) &gt;= 0))  {
         //fetch each url concurrently
         var ai = new ajax(link,function(text,url){
              //insert the new mobile page into the DOM
             insertPages(text,url);
         });
         ai.doGet();
      }
    }
  }
};
</pre>

We ensure proper asynchronous post-processing through the use of the “AJAX” object. There is a more advanced explanation of using localStorage within an AJAX call in [[tutorials/mobile_offline|Working Off the Grid with HTML5 Offline]]. In this example, you see the basic usage of caching on each request and providing the cached objects when the server returns anything but a successful (200) response.

<pre>
function processRequest () {
  if (req.readyState == 4) {
    if (req.status == 200) {
      if (supports_local_storage()) {
        localStorage[url] = req.responseText;
      }
      if (callback) callback(req.responseText,url);
    } else {
      // There is an error of some kind, use our cached copy (if available).
      if (!!localStorage[url]) {
        // We have some data cached, return that to the callback.
        callback(localStorage[url],url);
        return;
      }
    }
  }
}
</pre>

Unfortunately, since localStorage uses UTF-16 for character encoding, each single byte is stored as 2 bytes bringing our storage limit from 5MB to [https://twitter.com/#!/wesleyhales/status/104992809534238721 2.6MB total]. The whole reason for fetching and caching these pages/markup outside of the application cache scope is revealed in the next section.

With the recent advances in the [http://dev.w3.org/html5/spec-author-view/the-iframe-element.html iframe element] with HTML5, we now have a simple and effective way to parse the <code>responseText</code> we get back from our AJAX call. There are plenty of 3000-line JavaScript parsers and regular expressions which removes script tags and so on. But why not let the browser do what it does best? In this example, we are going to write the <code>responseText</code> into a temporary hidden iframe. We are using the HTML5 “sandbox” attribute which disables scripts and offers many security features...

From the spec:
The sandbox attribute, when specified, enables a set of extra restrictions on any content hosted by the iframe. Its value must be an unordered set of unique space-separated tokens that are ASCII case-insensitive. The allowed values are allow-forms, allow-same-origin, allow-scripts, and allow-top-navigation. When the attribute is set, the content is treated as being from a unique origin, forms and scripts are disabled, links are prevented from targeting other browsing contexts, and plugins are disabled.
To limit the damage that can be caused by hostile HTML content, it should be served using the [http://dev.w3.org/html5/spec-author-view/iana.html#text-html-sandboxed text/html-sandboxed] MIME type.

<pre>
var insertPages = function(text, originalLink) {
  var frame = getFrame();
  //write the ajax response text to the frame and let
  //the browser do the work
  frame.write(text);

  //now we have a DOM to work with
  var incomingPages = frame.getElementsByClassName(&#x27;page&#x27;);

  var pageCount = incomingPages.length;
  for (var i = 0; i &lt; pageCount; i++) {
    //the new page will always be at index 0 because
    //the last one just got popped off the stack with appendChild (below)
    var newPage = incomingPages[0];

    //stage the new pages to the left by default
    newPage.className = &#x27;page stage-left&#x27;;

    //find out where to insert
    var location = newPage.parentNode.id == &#x27;back&#x27; ? &#x27;back&#x27; : &#x27;front&#x27;;

    try {
      // mobile safari will not allow nodes to be transferred from one DOM to another so
      // we must use adoptNode()
      document.getElementById(location).appendChild(document.adoptNode(newPage));
    } catch(e) {
      // todo graceful degradation?
    }
  }
};
</pre>

Safari correctly refuses to implicitly move a node from one document to another. An error is raised if the new child node was created in a different document. So here we use <code>adoptNode</code> and all is well.

So why iframe? Why not just use innerHTML? Even though innerHTML is now part of the HTML5 spec, it is a dangerous practice to insert the response from a server (evil or good) into an unchecked area. During the writing of this article, I couldn’t find *anyone* using anything but innerHTML. I know JQuery uses it at it’s core with an append fallback on exception only. And JQuery Mobile uses it as well. However I haven’t done any heavy testing in regards to innerHTML "[http://martinkou.blogspot.com/2011/05/alternative-workaround-for-mobile.html stops working randomly]", but it would be very interesting to see all the platforms this affects. It would also be interesting to see which approach is more performant... I’ve heard claims from both sides on this as well.

<h2 id="toc-network-detection">Network type detection, handling, and profiling</h2>

Now that we have the ability to buffer (or predictive cache) our web app, we must provide the proper connection detection features that makes our app smarter. This is where mobile app development gets extremely sensitive to online/offline modes and connection speed.
Enter [http://dev.w3.org/2009/dap/netinfo/ The Network Information API]. Every time I show this feature in a presentation, someone in the audience raises their hand and asks “What would I use that for?”. So here is a possible way to setup an extremely smart mobile web app.

Boring common sense scenario first...
While interacting with the Web from a mobile device on a high-speed train, the network may very well go away at various moments and different geographies might support different transmission speeds (e.g., HSPA or 3G might be available in some urban areas, but remote areas might support much slower 2G technologies). The following code addresses most of the connection scenarios.

The following code provides:

* Offline access through <code>applicationCache</code>.
* Detects if bookmarked and offline.
* Detects when switching from offline to online and vice versa.
* Detects slow connections and fetches content based on network type.

Again, all of these features require very little code. First we detect our events and loading scenarios:

<pre>
window.addEventListener(&#x27;load&#x27;, function(e) {
 if (navigator.onLine) {
  // new page load
  processOnline();
 } else {
   // the app is probably already cached and (maybe) bookmarked...
   processOffline();
 }
}, false);

window.addEventListener(&quot;offline&quot;, function(e) {
  // we just lost our connection and entered offline mode, disable eternal link
  processOffline(e.type);
}, false);

window.addEventListener(&quot;online&quot;, function(e) {
  // just came back online, enable links
  processOnline(e.type);
}, false);
</pre>

In the EventListeners above, we must tell our code if it is being called from an event or an actual page request or refresh. The main reason is because the body <code>onload</code> event won’t be fired when switching between the online and offline modes.

Next, we have a simple check for an <code>ononline</code> or <code>onload</code> event. This code resets disabled links when switching from offline to online, but if this app were more sophisticated, you might insert logic that would resume fetching content or handle the UX for intermittent connections.

<pre>
function processOnline(eventType) {

  setupApp();
  checkAppCache();

  // reset our once disabled offline links
  if (eventType) {
    for (var i = 0; i &lt; disabledLinks.length; i++) {
      disabledLinks[i].onclick = null;
    }
  }
}
</pre>

The same goes for <code>processOffline()</code>. Here you would manipulate your app for offline mode and try to recover any transactions that were going on behind the scenes. This code below digs out all of our external links and disables them—trapping users in our offline app FOREVER muhahaha!

<pre>
function processOffline() {
  setupApp();

  // disable external links until we come back - setting the bounds of app
  disabledLinks = getUnconvertedLinks(document);

  // helper for onlcick below
  var onclickHelper = function(e) {
    return function(f) {
      alert(&#x27;This app is currently offline and cannot access the hotness&#x27;);return false;
    }
  };

  for (var i = 0; i &lt; disabledLinks.length; i++) {
    if (disabledLinks[i].onclick == null) {
      //alert user we&#x27;re not online
      disabledLinks[i].onclick = onclickHelper(disabledLinks[i].href);

    }
  }
}
</pre>

OK, so on to the good stuff. Now that our app knows what connected state it’s in, we can also check the type of connection when it’s online and adjust accordingly. I have listed typical North American providers download and latencies in the comments for each connection.

<pre>
function setupApp(){
  // create a custom object if navigator.connection isn&#x27;t available
  var connection = navigator.connection &#124;&#124; {&#x27;type&#x27;:&#x27;0&#x27;};
  if (connection.type == 2 &#124;&#124; connection.type == 1) {
      //wifi/ethernet
      //Coffee Wifi latency: ~75ms-200ms
      //Home Wifi latency: ~25-35ms
      //Coffee Wifi DL speed: ~550kbps-650kbps
      //Home Wifi DL speed: ~1000kbps-2000kbps
      fetchAndCache(true);
  } else if (connection.type == 3) {
  //edge
      //ATT Edge latency: ~400-600ms
      //ATT Edge DL speed: ~2-10kbps
      fetchAndCache(false);
  } else if (connection.type == 2) {
      //3g
      //ATT 3G latency: ~400ms
      //Verizon 3G latency: ~150-250ms
      //ATT 3G DL speed: ~60-100kbps
      //Verizon 3G DL speed: ~20-70kbps
      fetchAndCache(false);
  } else {
  //unknown
      fetchAndCache(true);
  }
}
</pre>

There are numerous adjustments we could make to our fetchAndCache process, but all I did here was tell it to fetch the resources asynchronous (true) or synchronous (false) for a given connection.

Edge (Synchronous) Request Timeline

[[File:edge-sync.png|700px|Edge Sync]]

WIFI (Asynchronous) Request Timeline

[[File:wifi-async.png|700px|WIFI Async]]

This allows for at least some method of user experience adjustment based on slow or fast connections.
This is by no means is an end-all-be-all solution. Another todo would be to throw up a loading modal when a link is clicked (on slow connections) while the app still may be fetching that link’s page in the background.
The big point here is to cut down on latencies while leveraging the full capabilities of the user’s connection with the latest and greatest HTML5 has to offer.
[http://slidfast.appspot.com/network-detection.html View the network detection demo here].

<h2 id="toc-conclusion">Conclusion</h2>
The journey down the road of mobile HTML5 apps is just beginning. Now you see the very simple and basic underpinnings of a mobile “framework” built solely around HTML5 and it’s supporting technologies. I think it’s important for developers to work with and address these features at their core and not masked by a wrapper.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=20
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Performance
}}
{{Topics|Mobile, Performance}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/mobile/optimization-and-performance/
}}