{{Page_Title|Creating and modifying HTML}}
{{Flags}}
{{Byline}}
{{Summary_Section|when you've targetted an HTML element using JavaScript, how do modify it, and create new HTML nearby? This article shows you how.}}
{{Tutorial
|Content=== Introduction ==
 
In this article of the [http://www.w3.org/wiki/Web_Standards_Curriculum Web Standards Curriculum] I’ll explain the basics of using JavaScript to
manipulate the content of your pages, including showing and hiding parts of a
page, and adding new HTML and removing it. At the end of this you’ll
understand that the most fundamental thing we use JavaScript for
is to change the contents of pages, and you’ll understand the best ways
to do this.
 
== Hiding and showing ==
 
The easiest place to start is with manipulating the HTML you’ve already
got, by hiding or showing elements that are already in the page. To do this,
you can use JavaScript to change the styles on an element. CSS styles are already a
powerful way of describing how an element looks, and one part of how an
element looks is whether it’s displayed at all. The CSS <code>display</code>
property is the key to showing and hiding an element: setting it to 
<code>display:none;</code> hides an element. Imagine a paragraph like this:

<syntaxhighlight lang="html5"><p id="mypara" style="display: none">I am a paragraph</p></syntaxhighlight>
 
That paragraph would be invisible on the page. JavaScript allows you to
''dynamically'' add that <code>display: none</code> style to that element
and take it away.
 
JavaScript is designed to allow you to get a ''reference'' to an HTML
element. For example, <code>var el = document.getElementById("nav");</code> will
give you a reference to the element with <code>id="nav"</code>. Once you’ve got
a reference to an element, you can change the CSS applied to it by using the <code>style</code> attribute. For example, our above
“mypara” paragraph is currently hidden (it has <code>display: none</code> set).
To show it, set the style attribute <code>display</code> to
<code>block</code>:

<syntaxhighlight lang="javascript">var el = document.getElementById('mypara');
el.style.display = 'block';</syntaxhighlight>
 
And lo, the paragraph appears. Setting CSS on an element through the
<code>style</code> attribute does the same thing as setting it in the
<code>style</code> attribute in the HTML itself, so the above code setting 
<code>el.style.display = 'block'</code> achieves the same effect as putting 
<code>style="display: block"</code> directly in your HTML. Except that it’s dynamic. Hiding any element is just as simple:
 
<syntaxhighlight lang="javascript">var el = document.getElementById('mypara');
el.style.display = 'none';</syntaxhighlight>
 
=== Hiding and showing example ===
 
Theory is all good, but a more practical example may be useful here. Imagine
a set of tabs, where clicking on the tab itself shows it and hides all the 
others.

Here’s an example of a set of tabs:
 
<syntaxhighlight lang="html5"><ol class="tablinks">
  <li><a href="#tab1">Tab 1</a></li>
  <li><a href="#tab2">Tab 2</a></li>
  <li><a href="#tab3">Tab 3</a></li>
</ol>

<div class="tab" id="tab1">This is tab 1</div>
<div class="tab" id="tab2">This is tab 2</div>
<div class="tab" id="tab3">This is tab 3</div></syntaxhighlight>
 
In the <code>head</code> of the example file (see [http://dev.opera.com/articles/view/creating-and-modifying-html/tabs.html tabs.html] for the live example), you’ll find the following CSS and JavaScript (these would normally be put in external files and imported into the HTML, but I’m keeping everything in one file here to make things simpler to navigate). Some of the code looks intimidating; don’t worry, we’ll go through it.

<syntaxhighlight lang="html5"><style type="text/css">
ol.tablinks {
  margin: 0; padding: 0;
}
ol.tablinks li {
  float: left;
  border: 2px solid red;
  border-width: 2px 2px 0 2px;
  background: #eee;
  list-style: none;
  padding: 5px;
  margin: 0;
}
ol.tablinks li a {
  text-decoration: none;
  color: black;
}
div.tab {
  clear: left;
  border: 2px solid red;
  border-width: 1px 2px 2px 2px;
}
</style>

<script type="text/javascript">
var tabify = {
  hasClass: function(el,c) {
    return el.className.match(new RegExp('(\\s|^)'+c+'(\\s|$)'));        
  },
  addClass: function(el,c) {
    if (!tabify.hasClass(el,c)) el.className += " " + c;
  },
  removeClass: function(el,c) {
    if (tabify.hasClass(el,c)) {
      el.className=el.className.replace(new RegExp('(\\s|^)'+c+'(\\s|$)'),' ');
    }
  },
  hideAllTabs: function(ol) {
    var links = ol.getElementsByTagName("a");
    for (var i=0; i&lt;links.length; i++) {
      tabify.setTabFromLink(links[i], "none");
   }
  },
  setTabFromLink: function(link, style) {
    var dest = link.href.match(/#(.*)$/)[1];
    document.getElementById(dest).style.display = style;
    if (style == "none") {
        tabify.removeClass(link, "active");
    } else {
        tabify.addClass(link, "active");
    }
  },
  addEvent: function(obj, type, fn) {
    if ( obj.attachEvent ) {
      obj['e'+type+fn] = fn;
      obj[type+fn] = function(){obj['e'+type+fn]( window.event );};
      obj.attachEvent('on'+type, obj[type+fn] );
    } else {
      obj.addEventListener( type, fn, false );
    }
  },  
  init: function() {
    var ols = document.getElementsByTagName("ol");
    for (var i=0; i&lt;ols.length; i++) {
      var ol = ols[i];
      if (!/(^|\s)tablinks(\s|$)/.test(ol.className)) { continue; }
      tabify.addEvent(ol, "click", function(e) {
        var target = window.event ? window.event.srcElement : e.target;
        if (target.nodeName.toLowerCase() === "a") {
          tabify.hideAllTabs(e.target.parentNode.parentNode);
          tabify.setTabFromLink(e.target, "block");
          if (e) e.preventDefault();
          if (window.event) window.event.returnValue = false;
          return false;
        }
      }, true);
      tabify.hideAllTabs(ol);
      tabify.setTabFromLink(ol.getElementsByTagName("a")[0], "block");
    }
  }
};
tabify.addEvent(window, "load", tabify.init);
</script></syntaxhighlight>
 
Each tab is a link. Each link has an <code>onclick</code>
event handler on it. That event handler does
two things: it '''hides''' all the <code>div</code>s (using the
<code>display: none</code> approach from above) and then '''shows''' 
the <code>div</code> corresponding to that tab, by setting that 
<code>div</code>’s <code>style</code> to <code>display: block</code>.

You’ll have noted that the HTML here is set up to still make sense even in
the absence of scripting; while clicking a link won’t show or hide a tab, the
links jump to the appropriate tab, so the page still operates correctly and
makes semantic sense even in a browser without JavaScript. This is important:
it’s a technique that you may have heard referred to as “progressive
enhancement” (or, in the ancient tongue of three years ago “graceful
degradation”, but we don’t call it that any more). It’s important not only
for people who are using some modern browser but with JavaScript turned off, but
for a host of other user types as well. Assistive technologies such as
screen-readers for blind users rely heavily on the structure of your HTML
being semantic and meaningful, and their support for JavaScript enhancements is
not as good as those for sighted users. Mobile browsers also tend not to have
as much useful support for scripting. Search engines also read your HTML and
not your script—it could be said that Google is the world’s most
voracious blind browser user. This is the meaning of the term “progressive
enhancement”: start with a page that makes sense and displays its content
in the most simple of environments, such as a text-only web browser, and then
gradually add extra functionality to it so that at every step of the way
your site is still usable and functional.
 
All JavaScript code basically comes in two parts: the part that actually
does the work, and the part that hooks up that bit to the HTML. The code that
actually does the work in this example is pretty trivial: showing the corresponding tab to a particular link is two lines of JavaScript:
 
<syntaxhighlight lang="javascript">var dest = link.href.match(/#(.*)$/)[1];
document.getElementById(dest).style.display = "block";</syntaxhighlight>
 
The links, if you remember, look like <code>&lt;a href="#tab1"&gt;Tab 1&lt;/a&gt;</code>
and so the first line uses a regular expression (see the note below) to extract 
the part of the link that appears after the <code>#</code> symbol; in this 
example that would be the string <code>tab1</code>. That part of the link is the same as
the ID of the corresponding <code>div</code> (because, as mentioned, the page
is built to make sense semantically, so a “tab” links to its <code>div</code>).
We then fetch a reference to that <code>div</code> with 
<code>document.getElementById</code>, and set <code>style.display</code> to
<code>block</code> as previously discussed.
  
==== Regular expressions ====
 
Regular expressions are a sort of mini-programming-language designed to help
with the problem of “parsing” text—for example, answering questions like
“does this string appear inside this other string?“ and “in the string ‘abc123def’,
what are the numbers between ‘c’ and ‘d’?” They’re a very powerful tool, but
they’re also pretty complicated. There’s a description below of what the
regular expression is for; for now, though, feel free to take how they 
work on trust and come back to it later.

The “regex” (short for “regular expression”) used in this example is
<code>/#(.*)$/</code>. Each character in a regular expression is designed to
match against a sequence of characters in some target string; the idea is
to express how a target string is made up, in sections.
 
* <code>/ … /</code> — the slashes denote the start and end of a regex, just like double or single quotes do for a “string”
* <code>#</code> — the hash symbol (#) actually means “match a hash symbol”
* <code>( … )</code> — brackets mean “here is a section of the string that I’ll be interested in later”
* <code>.*</code> — this means “any characters you like”; it’s actually a dot (.), meaning “any one character”, followed by asterisk (*) meaning “repeat as many times as you want”
* <code>$</code> — the dollar means “the end of the string”
 
So our regex describes a “matching pattern” for a string comprised of “a hash,
followed by whatever characters you want”. <code>link.href</code> is the 
destination of the link we’re looking at (for example, <code>#tab1</code>, and
since this ''is'' a string described by “a hash followed by whatever
characters you want”), the “matching pattern” ''does'' apply to this 
string.
 
<code>link.href.match('''our_regexp''')</code>, therefore, will return
a true rather than false result; what it actually returns is an array of two
things, <code>["#tab1", "tab1"]</code>. The first is the text that was matched
by the whole regex, and the second is the text matched inside the brackets; this
is why the brackets are there—to mark that part of the string as “this is the
bit we care about”. That <code>tab1</code> is the string we want, so we can
grab it out of the returned array (it’s the second item, so <code>[1]</code>
will grab it — arrays start numbering at zero.)

==== Connecting the working code to the page ====
 
As mentioned above, there are two parts to the code: the part which actually
does the work, and the part which hooks up that bit to the HTML. Hooking up the
working code to the HTML is what events are for. In this particular example,
we care about two events: the <code>window</code>’s <code>load</code> event,
which is used to say “start everything off”, and the tab list’s
<code>click</code> event, which is fired when the user clicks on a tab. When the
page loads, we need to run the connection code, and the connection code should
connect the tab <code>click</code> event to the code above, which displays the
appropriate tab.
 
Running code in response to an event is done with the 
<code>addEventListener</code> function in most browsers and with the
<code>attachEvent</code> function in Internet Explorer. Here we are creating a “wrapper” function, which does the right thing depending on which is supported:
 
<syntaxhighlight lang="javascript">addEvent: function(obj, type, fn) {
  if ( obj.attachEvent ) {
    obj['e'+type+fn] = fn;
    obj[type+fn] = function(){obj['e'+type+fn]( window.event );};
    obj.attachEvent('on'+type, obj[type+fn] );
  } else {
    obj.addEventListener( type, fn, false );
  }
}</syntaxhighlight>
 
(Don’t worry too much about how this works; just take it on trust for now—you’ll understand it better as you become more experienced in JavaScript.) 
This function takes three parameters, <code>obj</code>, <code>type</code>,
and <code>fn</code>, which are “the object that fires the event”, “the
event we care about”, and “the function to run when the event fires”.
We need to run our function called <code>tabify.init</code> when the page loads;
the <code>tabify.init</code> function will then take care of hooking up each
tab’s <code>click</code> event.
 
<syntaxhighlight lang="javascript">addEvent(window, "load", tabify.init);</syntaxhighlight>
 
As you can see from the HTML structure above, a set of tabs are actually
expressed as an ordered list with <code>class="tablinks"</code>. So the
<code>tabify.init</code> function needs to do the following:
 
# Find all the <code>&lt;ol&gt;</code>s on the page with a class of <code>tablinks</code>
# Attach to each <code>&lt;ol&gt;</code>’s <code>click</code> event some code that does the following:
## Work out exactly which tab link the user clicked on
## Work out which actual tab corresponds to that tab link
## Show that one tab
## Hide any other tabs
 
The <code>init</code> function that does all this looks like so:

<syntaxhighlight lang="javascript">init: function() {
  var ols = document.getElementsByTagName("ol");
  for (var i=0; i&lt;ols.length; i++) {
    var ol = ols[i];
    if (!/(^|\s)tablinks(\s|$)/.test(ol.className)) { continue; }
    tabify.addEvent(ol, "click", function(e) {
      var target = window.event ? window.event.srcElement : e.target;
      if (target.nodeName.toLowerCase() === "a") {
        tabify.hideAllTabs(e.target.parentNode.parentNode);
        tabify.setTabFromLink(e.target, "block");
        if (e) e.preventDefault();
        if (window.event) window.event.returnValue = false;
        return false;
      }
    }, true);
    tabify.hideAllTabs(ol);
    tabify.setTabFromLink(ol.getElementsByTagName("a")[0], "block");
  }
}</syntaxhighlight>
 
Let’s walk through this function step by step, looking at what each part does in turn:

<syntaxhighlight lang="javascript">var ols = document.getElementsByTagName("ol");
  for (var i=0; i&lt;ols.length; i++) {
    var ol = ols[i];
    if (!/(^|\s)tablinks(\s|$)/.test(ol.className)) { continue; }
  }</syntaxhighlight>
 
This finds all the <code>&lt;ol&gt;</code>s on the page with a class of <code>tablinks</code>—it then pulls up a list of ''all'' <code>&lt;ol&gt;</code>s and for each one, says “if this ''doesn’t'' have a class of ‘tablinks’, then skip it”.
(Checking the class is done with a regular expression; <code>continue</code>
means “skip over this one and on to the next”.)

<syntaxhighlight lang="javascript">tabify.addEvent(ol, "click", function(e) {
  ...
});</syntaxhighlight>
 
This attaches some code to each <code>&lt;ol&gt;</code>’s <code>click</code> event.

<syntaxhighlight lang="javascript">var target = window.event ? window.event.srcElement : e.target;</syntaxhighlight>
 
This works out exactly which tab link the user clicked on…

<syntaxhighlight lang="javascript">tabify.setTabFromLink(e.target, "block");</syntaxhighlight>
 
…then this shows that single tab…

<syntaxhighlight lang="javascript">tabify.hideAllTabs(e.target.parentNode.parentNode);</syntaxhighlight>
 
…and finally, this line hides any other tabs.

The <code>setTabFromLink</code> and <code>hideAllTabs</code> functions are
also in the code; they use the techniques above to hide a tab or show it.
Take a look at them to see how they work — they’re separate functions
because it’s often useful to take a block of code that’s called from more
than one place and put it in its own function. (It makes your code easier
to understand and reuse in multiple places. People will sometimes refer to this as “breaking out” or “factorising” code into a function.)
 
There's a bit of "extra credit" work in there as well, which neatly 
demonstrates more adding and removing of attributes. The <code>setTabFromLink</code>
function not only displays the appropriate tab but also sets 
<code>class="active"</code> on the "active" tab. It does this with the help
of three utility functions, <code>hasClass</code>, <code>removeClass</code>, and
<code>addClass</code>. In the same way that we hide all the tabs and then show
the active one, we use <code>removeClass</code> to remove "active" from the
<code>className</code> of all the tablinks and then <code>addClass</code> to add
"active" to the one tablink which is actually active. Just adding a class to
a link may seem pointless — after all, classes are invisible — but
it's a hook for styling. We can (and have) make links with 
<code>class="active"</code> appear differently, by adding extra CSS:
 
<syntaxhighlight lang="css">ol.tablinks li a {
  background-color: red;
}

ol.tablinks li a.active {
  background-color: white;
}</syntaxhighlight>
 
So now, the "active" tab appears in white, while other tabs appear in red.
Using JavaScript to add and remove classes is a very common technique, and one
that you should use whenever possible; CSS is good at controlling layout and
position and appearance of your HTML elements, and so using JavaScript to
alter the classes on those elements means that they can pick up different
CSS styles. It's an ideal unification; JavaScript makes your elements dynamic
but doesn't actually change very much itself. Just add a class and let CSS
do the heavy lifting.

== Creating HTML ==
 
DOM scripting is much more powerful than simply altering the 
CSS properties of your existing HTML, though. You can also dynamically create
new HTML that was never in your page to begin with. For example, 
on the tech news site Slashdot, a link in a comment displays the destination of
the link in square brackets, so a link like 
&lt;a href="http://opera.com"&gt;A web browser&lt;/a&gt; will display as 
'''&lt;a href="http://opera.com"&gt;A web browser&lt;/a&gt; [opera.com]'''.
(They did this to stop people being [http://www.youtube.com/watch?v=oHg5SJYRHA0 rickrolled], or worse.) 
Adding this extra bit of HTML, displaying the destination domain of every link 
on the page, will be easy to do with JavaScript.
 
Creating new HTML elements is done with the <code>document.createElement</code> function. For this
example, we only need to add one thing: after each link, we’ll add a 
<code>span</code> containing text listing the domain of the link (check out [http://dev.opera.com/articles/view/creating-and-modifying-html/linkify.html linkify.html] for a live example). The HTML for the example looks like this:
 
<syntaxhighlight lang="javascript"><p id="start">This is some text that has 
<a href="http://www.w3.org/TR/html4/struct/links.html">links</a> in it
to various places, including <a href="http://www.opera.com">Opera</a>,
<a href="http://www.bbc.co.uk/">the BBC</a> and an internal link to
<a href="#start">the beginning of this section</a>. All the external links
should have <span>[domain]</span> after them.</p>
</syntaxhighlight>
 
The JavaScript looks like this:
 
<syntaxhighlight lang="javascript"><script type="text/javascript">
var linksuffix = {
  addEvent: function(obj, type, fn) {
    if ( obj.attachEvent ) {
      obj['e'+type+fn] = fn;
      obj[type+fn] = function(){obj['e'+type+fn]( window.event );};
      obj.attachEvent('on'+type, obj[type+fn] );
    } else {
      obj.addEventListener( type, fn, false );
    }
  },  
  init: function() {
    var links = document.getElementById("linksuffixtext").getElementsByTagName("a");
    for (var i=0; i&lt;links.length; i++) {
      var matches = links[i].href.match(/^http:\/\/(.*?)\//);
      if (matches) {
        var linkdomain = matches[1];
        var span = document.createElement("span");
        var spantext = document.createTextNode(" ["+linkdomain+"]");
        span.appendChild(spantext);
        links[i].parentNode.insertBefore(span, links[i].nextSibling);
      }
    }
  }
};
linksuffix.addEvent(window, "load", linksuffix.init);
</script>
</syntaxhighlight>
 
The part of the script that does the work here is as follows:
 
<syntaxhighlight lang="javascript">var links = document.getElementsByTagName("a");
for (var i=0; i&lt;links.length; i++) {
  var matches = links[i].href.match(/^http:\/\/(.*?)\//);
  if (matches) {
    var linkdomain = matches[1];
    var span = document.createElement("span");
    var spantext = document.createTextNode(" ["+linkdomain+"]");
    span.appendChild(spantext);
    links[i].parentNode.insertBefore(span, links[i].nextSibling);
  }
}</syntaxhighlight>
 
This breaks down like this:
 
<syntaxhighlight lang="javascript">var links = document.getElementsByTagName("a");
for (var i=0; i&lt;links.length; i++) {
  ...
}</syntaxhighlight>
 
First, it finds all the links (<code>getElementsByTagName("a")</code>) in the document
 
<syntaxhighlight lang="javascript">var matches = links[i].href.match(/^http:\/\/(.*?)\//);
if (matches) {
  ...
}</syntaxhighlight>
 
This line uses a regular expression on each link to find out whether the destination of the
link begins with <code>http://something/</code>. If it does…

<syntaxhighlight lang="javascript">var linkdomain = matches[1];
var span = document.createElement("span");
var spantext = document.createTextNode(" ["+linkdomain+"]");
span.appendChild(spantext);</syntaxhighlight>
 
…this next part first gets the “linkdomain”, the <code>www.opera.com</code> part of the link. It next creates a <code>&lt;span&gt;</code> element using 
<code>document.createElement</code>. Next, it creates a “textNode”. While HTML
elements themselves are created with <code>document.createElement</code>, 
all text in an HTML document is actually contained within 
“textNode”s, and you have to create those separately. You 
don’t have to worry about this (or even know about it) when writing 
actual HTML, but you do have to know about it when creating elements using 
DOM scripting. The text in the textNode is actually “ [domain]”, 
created by concatenating (adding together)
strings. Finally, this part uses the <code>&lt;span&gt;</code>’s
<code>appendChild</code> method to put the textNode inside the span.

<syntaxhighlight lang="javascript">links[i].parentNode.insertBefore(span, links[i].nextSibling);</syntaxhighlight>
 
This line adds the <code>span</code> into the document. At this point, <code>span</code> is a reference to an HTML
element that looks like this:

<syntaxhighlight lang="html5"><span> [example.com]</span></syntaxhighlight>
 
That element however isn’t part of the document. It’s not part of any document yet; it’s just floating around in limbo. Adding the element to the document can be done in one of two ways: using <code>appendChild</code> as above, or using
<code>insertBefore</code>. The <code>appendChild</code> function adds our new
element at the ''end'' of an existing element (that’s why it’s called
''append''). Since we want to add it in the middle of an existing element,
we need <code>insertBefore</code>. Remember that our current bit of HTML looks
something like this:
 
<syntaxhighlight lang="html5"><p>... text that has 
<a href="http://www.w3.org/TR/html4/struct/links.html">links</a> in it
to ...</syntaxhighlight>
 
This equates to a DOM tree looking something like Figure 1:

[[Image:create_modify_html_figure1.jpg|DOM tree before the addition of the span element after the link]] 

Figure 1: The DOM tree before the addition of the span element after the link
 
We want to insert our new span in between the <code>&lt;a&gt;</code> and the
“in it to” textNode, so that it appears after the <code>&lt;a&gt;</code>. This would leave our DOM tree looking like Figure 2:

[[Image:create_modify_html_figure2.jpg|DOM tree after the addition of the span element]]

Figure 2: The DOM tree after the addition of the span element
 
or, more simply, HTML such as
 
<syntaxhighlight lang="html5"><p>... text which has 
<a href="http://www.w3.org/TR/html4/struct/links.html">links</a>
<span> [domain]</span> in it to ...</syntaxhighlight>
 
What would be handy here is to be able to say “insert our new 
<code>span</code> ''after'' the link”. Sadly, there is no 
<code>insertAfter</code> function. Instead, we need to insert it 
''before'' the thing after the link (confusing, but think about it and
it’ll make sense). A quick shortcut to “the thing after an element labelled
<code>el</code>” is <code>el.nextSibling</code>. The <code>insertBefore</code>
function needs to be called on the element that you’re inserting into, which
is the parent <code>&lt;p&gt;</code> of the link, quickly accessible with
<code>link.parentNode</code>. So the full call, as above, is
 
<syntaxhighlight lang="javascript">links[i].parentNode.insertBefore(span, links[i].nextSibling);</syntaxhighlight>
 
That is, find the parent (<code>&lt;p&gt;</code>) of the link we’re currently
processing (<code>links[i]</code>), and insert our created <code>span</code> element
(<code>span</code>) before the thing after the link 
(<code>links[i].nextSibling</code>). Treating HTML as a DOM tree in this way
and inserting new elements into it can be confusing at first, but it soon
becomes clearer as you get more practice at it.

== Summary ==
 
HTML provides the structure of your pages, and CSS provides the description
of how it looks. What JavaScript brings is flexibility; your HTML structure
and your CSS styles become ''dynamic''. You can change how your pages
look and feel and work from moment to moment, based on what your users do. It’s
the next step up: from well-thought-out and well-structured information to 
data that changes depending on what your users need. You can show and hide elements,
change styles and appearances, and add new HTML or remove the old in whatever
way you need to.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections==== Exercise questions ===
 
* How do you set an element’s CSS display property to hide an element?
* What’s the difference between an element and a text node?
* Give two reasons why progressive enhancement is important.
* What’s the difference between <code>appendChild</code> and <code>insertBefore</code>?
* Why do we use an <code>addClass</code> function rather than just concatenating the new class name with an existing element's <code>className</code> attribute?
* In the following HTML structure, what would <code>document.getElementById("marker").nextSibling</code> be?   <syntaxhighlight lang="html5"><p>This is a <strong>block of HTML with <span id="marker">various markup<span> in it</strong>.</p></syntaxhighlight>
}}
{{Topics|JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}