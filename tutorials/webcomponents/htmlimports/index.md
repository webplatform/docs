{{Page_Title|HTML Imports: #include for the web}}
{{Flags
|Checked_Out=No
}}
{{Byline
|Name=Eric Bidelman
|URL=http://www.html5rocks.com/profiles/#ericbidelman
|Published=11 November 2013
}}
{{Summary_Section|'''HTML Imports''', part of Web Components, is a way to include HTML documents in other HTML documents. An import can include CSS, JavaScript, or anything else an .html file can contain.}}
{{Tutorial
|Content===Why imports?==

Think about how you load different types of resources on the web. For JS, we have <code><script src></code>. For CSS, your go-to is probably <code><link rel="stylesheet"></code>. For images it's <code><img></code>. Video has <code><video></code>. Audio, <code><audio></code>... Get to the point! The majority of the web's content has a simple and declarative way to load itself. Not so for HTML. Here's your options:

#'''<iframe>''' - tried and true but heavy weight. An iframe's content lives entirely in a separate context than your page. While that's mostly a great feature, it creates additional challenges (shrink wrapping the size of the frame to its content is tough, insanely frustrating to script into/out of, nearly impossible to style).
#'''AJAX''' - [http://ericbidelman.tumblr.com/post/31140607367/mashups-using-cors-and-responsetype-document I love xhr.responseType="document"], but you're saying I need JS to load HTML? That doesn't seem right.
#'''CrazyHacks™''' - embedded in strings, hidden as comments (e.g., <code><script type="text/html"></code>). Yuck!

See the irony? '''The web's most basic content, HTML, requires the greatest amount of effort to work with.''' Fortunately, [http://w3c.github.io/webcomponents/explainer/ Web Components] are here to get us back on track.

==Getting started==

[http://w3c.github.io/webcomponents/spec/imports/ HTML Imports], part of the [http://w3c.github.io/webcomponents/explainer/ Web Components] cast, is a way to include HTML documents in other HTML documents. You're not limited to markup either. An import can also include CSS, JavaScript, or anything else an .html file can contain. In other words, this makes imports a '''fantastic tool for loading related HTML/CSS/JS.'''

===The basics===

Include an import on your page by declaring a <code><link rel="import"></code>:

<pre>
<head>
  <link rel="import" href="/path/to/imports/stuff.html">
</head>
</pre>

The URL of an import is called an ''import location''. To load content from another domain, the import location needs to be [http://enable-cors.org/ CORS-enabled] (Cross Origin Resource Sharing):

<pre>
<!-- Resources on other origins must be CORS-enabled. -->
<link rel="import" href="http://example.com/elements.html">
</pre>

'''Fact!''' ''The browser's network stack automatically de-dupes all requests from the same URL. This means that imports that reference the same URL are only retrieved once. No matter how many times an import at the same location is loaded, it only executes once.''

===Feature detection and support===

To detect support, check if <code>.import</code> exists on the <code><link></code> element:

<pre>
function supportsImports() {
  return 'import' in document.createElement('link');
}

if (supportsImports()) {
  // Good to go!
} else {
  // Use other libraries/require systems to load files.
}
</pre>

Browser support is still in the early days. Chrome 31 was the first browser to see an implementation. Since then, Chrome 36 was update with the latest spec. You can enable the flag by turning on '''Enable experimental Web Platform features''' in <code>about:flags</code> in Chrome Canary. For other browsers, [http://www.polymer-project.org/platform/html-imports.html Polymer's polyfill] works great until things are widely supported.

'''Tip!''' ''Also '''Enable experimental Web Platform features''' to get the other bleeding edge web component goodies.''

===Bundling resources===

Imports provide convention for bundling HTML/CSS/JS (even other HTML Imports) into a single deliverable. It's an intrinsic feature, but a powerful one. If you're creating a theme, library, or just want to segment your app into logical chunks, giving users a single URL is compelling. Heck, you could even deliver an entire app via an import. Think about that for a second.

''Using only one URL, you can package together a single relocatable bundle of web goodness for others to consume.''

A real-world example is [http://getbootstrap.com/ Bootstrap]. Bootstrap is comprised of individual files (bootstrap.css, bootstrap.js, fonts), requires JQuery for its plugins, and provides markup examples. Developers like à la carte flexibility. It allows them buy in to the parts of the framework they want to use. That said, I'd wager your typical JoeDeveloper™ goes the easy route and downloads all of Bootstrap.

Imports make a ton of sense for something like Bootstrap. I present to you, the future of loading Bootstrap:

<pre>
<head>
  <link rel="import" href="bootstrap.html">
</head>
</pre>

Users simply load an HTML Import link. They don't need to fuss with the scatter-shot of files. Instead, the entirety of Bootstrap is managed and wrapped up in an import, bootstrap.html:

<pre>
<link rel="stylesheet" href="bootstrap.css">
<link rel="stylesheet" href="fonts.css">
<script src="jquery.js"></script>
<script src="bootstrap.js"></script>
<script src="bootstrap-tooltip.js"></script>
<script src="bootstrap-dropdown.js"></script>
...

<!-- scaffolding markup -->
<template>
  ...
</template>
</pre>

Let this sit. It's exciting stuff.

===Load/error events===

The <code><link></code> element fires a load event when an import is loaded successfully and onerror when the attempt fails (e.g., if the resource 404s).

Imports try to load immediately. An easy way avoid headaches is to use the <code>onload/onerror</code> attributes:

<pre>
<script async>
  function handleLoad(e) {
    console.log('Loaded import: ' + e.target.href);
  }
  function handleError(e) {
    console.log('Error loading import: ' + e.target.href);
  }
</script>

<link rel="import" href="file.html"
      onload="handleLoad(event)" onerror="handleError(event)">
</pre>

'''Tip!''' ''Notice the event handlers are defined before the import is loaded on the page. The browser tries to load the import as soon as it encounters the tag. If the functions don't exist yet, you'll get console errors for undefined function names.''

Or, if you're creating the import dynamically:

<pre>
var link = document.createElement('link');
link.rel = 'import';
link.href = 'file.html'
link.onload = function(e) {...};
link.onerror = function(e) {...};
document.head.appendChild(link);
</pre>

==Using the content==

Including an import on a page doesn't mean "plop the content of that file here". It means "parser, go off an fetch this document so I can use it". To actually use the content, you have to take action and write script.

A critical aha! moment is realizing that an import is just a document. In fact, the content of an import is called an ''import document''. You're able to '''manipulate the guts of an import using standard DOM APIs!'''

===link.import===

To access the content of an import, use the link element's <code>.import</code> property:

<pre>
var content = document.querySelector('link[rel="import"]').import;
</pre>

<code>link.import</code> is null under the following conditions:

*The browser doesn't support HTML Imports.
*The <code><link></code> doesn't have <code>rel="import"</code>.
*The <code><link></code> has not been added to the DOM.
*The <code><link></code> has been removed from the DOM.
*The resource is not CORS-enabled.

====Full example====
Let's say <code>warnings.html</code> contains:

<pre>
<div class="warning">
  <style scoped>
    h3 {
      color: red;
    }
  </style>
  <h3>Warning!</h3>
  <p>This page is under construction</p>
</div>

<div class="outdated">
  <h3>Heads up!</h3>
  <p>This content may be out of date</p>
</div>
</pre>

Importers can grab a specific portion of this document and clone it into their page:

<pre>
<head>
  <link rel="import" href="warnings.html">
</head>
<body>
  ...
  <script>
    var link = document.querySelector('link[rel="import"]');
    var content = link.import;

    // Grab DOM from warning.html's document.
    var el = content.querySelector('.warning');

    document.body.appendChild(el.cloneNode(true));
  </script>
</body>
</pre>

===Scripting in imports===

Imports are not in the main document. They're satellite to it. However, your import can still act on the main page even though the main document reigns supreme. An import can access its own DOM and/or the DOM of the page that's importing it:

'''Example''' - import.html that adds one of its stylesheets to the main page

<pre>
<link rel="stylesheet" href="http://www.example.com/styles.css">
<link rel="stylesheet" href="http://www.example.com/styles2.css">

<style>
  /* Note: <style> in an import apply to the main
     document by default. That is, style tags don't need to be
     explicitly added to the main document. */
  #somecontainer {
    color: blue;
  }
</style>
...

<script>
  // importDoc references this import's document
  var importDoc = document.currentScript.ownerDocument;

  // mainDoc references the main document (the page that's importing us)
  var mainDoc = document;

  // Grab the first stylesheet from this import, clone it,
  // and append it to the importing document.
  var styles = importDoc.querySelector('link[rel="stylesheet"]');
  mainDoc.head.appendChild(styles.cloneNode(true));
</script>
</pre>

Notice what's going on here. The script inside the import references the imported document (<code>document.currentScript.ownerDocument</code>), and appends part of that document to the importing page (<code>mainDoc.head.appendChild(...)</code>). Pretty gnarly if you ask me.

''A script in an import can either execute code directly, or define functions to be used by the importing page. This is similar to the way [http://docs.python.org/2/tutorial/modules.html#more-on-modules modules] are defined in Python.''

Rules of JavaScript in an import:

*Script in the import is executed in the context of the window that contains the importing document. So <code>window.document</code> refers to the main page document. This has two useful corollaries:
**functions defined in an import end up on <code>window</code>.
**you don't have to do anything crazy like append the import's <code><script></code> blocks to the main page. Again, script gets executed.
*Imports do not block parsing of the main page. However, scripts inside them are processed in order. This means you get defer-like behavior while maintaining proper script order. More on this below.

==Delivering Web Components==

The design of HTML Imports lends itself nicely to loading reusable content on the web. In particular, it's an ideal way to distribute Web Components. Everything from basic [http://www.html5rocks.com/webcomponents/template/ HTML <code><template></code>s] to full-blown [http://www.html5rocks.com/tutorials/webcomponents/customelements/#registering Custom Elements] with Shadow DOM ([http://www.html5rocks.com/tutorials/webcomponents/shadowdom/ 1], [http://www.html5rocks.com/tutorials/webcomponents/shadowdom-201/ 2], [http://www.html5rocks.com/tutorials/webcomponents/shadowdom-301/ 3]). When these technologies are used in tandem, imports become a [http://en.cppreference.com/w/cpp/preprocessor/include #include] for Web Components.

===Including templates===

The [http://www.html5rocks.com/tutorials/webcomponents/template/ HTML Template] element is a natural fit for HTML Imports. <code><template></code> is great for scaffolding out sections of markup for the importing app to use as it desires. Wrapping content in a <code><template></code> also gives you the added benefit of making the content inert until used. That is, scripts don't run until the template is added to the DOM. Boom!

'''import.html'''

<pre>
<template>
  <h1>Hello World!</h1>
  <!-- Img is not requested until the <template> goes live. -->
  <img src="world.png">
  <script>alert("Executed when the template is activated.");</script>
</template>
</pre>

'''index.html'''

<pre>
<head>
  <link rel="import" href="import.html">
</head>
<body>
  <div id="container"></div>
  <script>
    var link = document.querySelector('link[rel="import"]');

    // Clone the <template> in the import.
    var template = link.import.querySelector('template');
    var clone = document.importNode(template.content, true);

    document.querySelector('#container').appendChild(clone);
  </script>
</body>
</pre>

===Registering custom elements===

[http://www.html5rocks.com/en/tutorials/webcomponents/imports/tutorials/webcomponents/customelements/ Custom Elements] is another Web Component technology that plays absurdly well with HTML Imports. [http://www.html5rocks.com/en/tutorials/webcomponents/imports/#includejs Imports can execute script], so why not define and register your custom elements so users don't have to? Call it..."auto-registration".

'''elements.html'''

<pre>
<script>
  // Define and register <say-hi>.
  var proto = Object.create(HTMLElement.prototype);

  proto.createdCallback = function() {
    this.innerHTML = 'Hello, <b>' +
                     (this.getAttribute('name') || '?') + '</b>';
  };

  document.registerElement('say-hi', {prototype: proto});

  // Define and register <shadow-element> that uses Shadow DOM.
  var proto2 = Object.create(HTMLElement.prototype);

  proto2.createdCallback = function() {
    var root = this.createShadowRoot();
    root.innerHTML = "<style>::content > *{color: red}</style>" +
                     "I'm a " + this.localName +
                     " using Shadow DOM!<content></content>";
  };
  document.registerElement('shadow-element', {prototype: proto2});
</script>
</pre>

This import defines (and registers) two elements, <code><say-hi></code> and <code><shadow-element></code>. The importer can simply declare them on their page. No wiring needed.

'''index.html'''

<pre>
<head>
  <link rel="import" href="elements.html">
</head>
<body>
  <say-hi name="Eric"></say-hi>
  <shadow-element>
    <div>( I'm in the light dom )</div>
  </shadow-element>
</body>
</pre>

In my opinion, this workflow alone makes HTML Imports an ideal way to share Web Components.

===Managing dependencies and sub-imports===

''Yo dawg. I hear you like imports, so I included an import in your import.''

===Sub-imports===

It can be useful for one import to include another. For example, if you want to reuse or extend another component, use an import to load the other element(s).

Below is a real example from [http://polymer-project.org/ Polymer]. It's a new tab component (<code><polymer-ui-tabs></code>) that reuses a layout and selector component. The dependencies are managed using HTML Imports.

'''polymer-ui-tabs.html'''

<pre>
<link rel="import" href="polymer-selector.html">
<link rel="import" href="polymer-flex-layout.html">

<polymer-element name="polymer-ui-tabs" extends="polymer-selector" ...>
  <template>
    <link rel="stylesheet" href="polymer-ui-tabs.css">
    <polymer-flex-layout></polymer-flex-layout>
    <shadow></shadow>
  </template>
</polymer-element>
</pre>

([https://github.com/Polymer/polymer-ui-elements/blob/master/polymer-ui-tabs/polymer-ui-tabs.html Full source here.])

App developers can import this new element using:

<pre>
<link rel="import" href="polymer-ui-tabs.html">
<polymer-ui-tabs></polymer-ui-tabs>
</pre>

When a new, more awesome <code><polymer-selector2></code> comes along in the future, you can swap out <code><polymer-selector></code> and start using it straight away. You won't break your users thanks to imports and web components.

===Dependency management===

We all know that loading JQuery more than once per page causes errors. Isn't this going to be a ''huge'' problem for Web Components when multiple components use the same library? Not if we use HTML Imports! They can be used to manage dependencies.

By wrapping libraries in an HTML Import, you automatically de-dupe resources. The document is only parsed once. Scripts are only executed once. As an example, say you define an import, jquery.html, that loads a copy of JQuery.

'''jquery.html'''

<pre>
<script src="http://cdn.com/jquery.js"></script>
</pre>

This import can be reused in subsequent imports like so:

'''import2.html'''

<pre>
<link rel="import" href="jquery.html">
<div>Hello, I'm import 2</div>
</pre>

'''ajax-element.html'''

<pre>
<link rel="import" href="jquery.html">
<link rel="import" href="import2.html">

<script>
  var proto = Object.create(HTMLElement.prototype);

  proto.makeRequest = function(url, done) {
    return $.ajax(url).done(function() {
      done();
    });
  };

  document.registerElement('ajax-element', {prototype: proto});
</script>
</pre>

Even the main page itself can include jquery.html if it needs the library:

<pre>
<head>
  <link rel="import" href="jquery.html">
  <link rel="import" href="ajax-element.html">
</head>
<body>

...

<script>
  $(document).ready(function() {
    var el = document.createElement('ajax-element');
    el.makeRequest('http://example.com');
  });
</script>
</body>
</pre>

Despite jquery.html being included in many different import trees, its document is only fetched and processed once by the browser. Examining the network panel proves this:

[[Image:htmlimports1.png]]
''jquery.html is requested once''

==Performance considerations==

HTML Imports are totally awesome but as with any new web technology, you should use them wisely. Web development best practices still hold true. Below are some things to keep in mind.

===Concatenate imports===

Reducing network requests is always important. If you have many top-level import links, consider combining them into a single resource and importing that file!

[https://github.com/Polymer/vulcanize Vulcanize] is an npm build tool from the [http://www.polymer-project.org/ Polymer] team that recursively flattens a set of HTML Imports into a single file. Think of it as a concatenation build step for Web Components.

===Imports leverage browser caching===

Many people forget that the browser's networking stack has been finely tuned over the years. Imports (and sub-imports) take advantage of this logic too. The <code>http://cdn.com/bootstrap.html</code> import might have sub-resources, but they'll be cached.

===Content is useful only when you add it===

Think of content as inert until you call upon its services. Take a normal, dynamically created stylesheet:

<pre>
var link = document.createElement('link');
link.rel = 'stylesheet';
link.href = 'styles.css';
</pre>

The browser won't request styles.css until link is added to the DOM:

<pre>
document.head.appendChild(link); // browser requests styles.css
</pre>

Another example is dynamically created markup:

<pre>
var h2 = document.createElement('h2');
h2.textContent = 'Booyah!';
</pre>

The h2 is relatively meaningless until you add it to the DOM.

The same concept holds true for the import document. Unless you append it's content to the DOM, it's a no-op. In fact, the only thing that "executes" in the import document directly is <code><script></code>. See [[#Scripting in imports|Scripting in imports]] above.

===Optimizing for async loading===

'''Imports don't block parsing of the main page.''' Scripts inside imports are processed in order but don't block the importing page. This means you get defer-like behavior while maintaining proper script order. One benefit of putting your imports in the <code><head></code> is that it lets the parser start working on the content as soon as possible. With that said, it's critical to remember <code><script></code> in the main document still continues to block the page:

<pre>
<head>
  <link rel="import" href="/path/to/import_that_takes_5secs.html">
  <script>console.log('I block page rendering');</script>
</head>
</pre>

Depending on your app structure and use case, there are several ways to optimize async behavior. The techniques below mitigate blocking the main page rendering.

====Scenario #1 (preferred): you ''don't'' have script in <code><head></code> or inlined in <code><body></code>====

My recommendation for placing <code><script></code> is to avoid immediately following your imports. Move scripts as late in the game as possible... but you're already doing that best practice, AREN'T YOU!? ;)

Here's an example:

<pre>
<head>
  <link rel="import" href="/path/to/import.html">
  <link rel="import" href="/path/to/import2.html">
  <!-- avoid including script -->
</head>
<body>
  <!-- avoid including script -->

  <div id="container"></div>

  <!-- avoid including script -->
  ...

  <script>
    // Other scripts n' stuff.

    // Bring in the import content.
    var link = document.querySelector('link[rel="import"]');
    var post = link.import.querySelector('#blog-post');

    var container = document.querySelector('#container');
    container.appendChild(post.cloneNode(true));
  </script>
</body>
</pre>

Everything is at the bottom.

====Scenario 1.5: the import adds itself====

Another option is to have the import [[#Scripting in imports|add its own content]]. If the import author establishes a contract for the app developer to follow, the import can add itself to an area of the main page:

'''import.html'''

<pre>
<div id="blog-post">...</div>
<script>
  var me = document.currentScript.ownerDocument;
  var post = me.querySelector('#blog-post');

  var container = document.querySelector('#container');
  container.appendChild(post.cloneNode(true));
</script>
</pre>

'''index.html'''

<pre>
<head>
  <link rel="import" href="/path/to/import.html">
</head>
<body>
  <!-- no need for script. the import takes care of things -->
</body>
</pre>

====Scenario #2: you ''do'' have script in <code><head></code> or inlined in <code><body></code>====

If you have an import that takes a long time to load, the first <code><script></code> that follows it on the page will block the page from rendering. Google Analytics for example, recommends putting the tracking code in the <code><head></code>. If you can't avoid putting <code><script></code> in the <code><head></code>, dynamically adding the import will prevent blocking the page:

<pre>
<head>
  <script>
    function addImportLink(url) {
      var link = document.createElement('link');
      link.rel = 'import';
      link.href = url;
      link.onload = function(e) {
        var post = this.import.querySelector('#blog-post');

        var container = document.querySelector('#container');
        container.appendChild(post.cloneNode(true));
      };
      document.head.appendChild(link);
    }

    addImportLink('/path/to/import.html'); // Import is added early :)
  </script>
  <script>
    // other scripts
  </script>
</head>
<body>
   <div id="container"></div>
   ...
</body>
</pre>

Alternatively, add the import near the end of the <code><body></code>:

<pre>
<head>
  <script>
    // other scripts
  </script>
</head>
<body>
  <div id="container"></div>
  ...

  <script>
    function addImportLink(url) { ... }

    addImportLink('/path/to/import.html'); // Import is added very late :(
  </script>
</body>
</pre>

'''Note:''' This very last approach is least preferable. The parser doesn't start to work on the import content until late in the page.

==Things to remember==

*An import's mimetype is <code>text/html</code>.
*Resources from other origins need to be CORS-enabled.
*Imports from the same URL are retrieved and parsed once. That means script in an import is only executed the first time the import is seen.
*Scripts in an import are processed in order, but do not block the main document parsing.
*An import link doesn't mean "#include the content here". It means "parser, go off an fetch this document so I can use it later". While scripts execute at import time, stylesheets, markup, and other resources need to be added to the main page explicitly. Note: <code><style></code> don't need to be added explicitly. This is a major difference between HTML Imports and <code><iframe></code>, which says "load and render this content here".

==Conclusion==

HTML Imports allow bundling HTML/CSS/JS as a single resource. While useful by themselves, this idea becomes extremely powerful in the world of Web Components. Developers can create reusable components for others to consume and bring in to their own app, all delivered through <code><link rel="import"></code>.

HTML Imports are a simple concept, but enable a number of interesting use cases for the platform.

===Use cases===

*'''Distribute''' related [[#Bundling resources|HTML/CSS/JS as a single bundle]]. Theoretically, you could import an entire web app into another.
*'''Code organization''' - segment concepts logically into different files, encouraging modularity & reusability.
*'''Deliver''' one or more [http://www.html5rocks.com/tutorials/webcomponents/customelements/ Custom Element] definitions. An import can be used to register and include them in an app. This practices good software patterns, keeping the element's interface/definition separate from how its used.
*[[#Managing dependencies and sub-imports|'''Manage dependencies''']] - resources are automatically de-duped.
*'''Chunk scripts''' - before imports, a large-sized JS library would have its file wholly parsed in order to start running, which was slow. With imports, the library can start working as soon as chunk A is parsed. Less latency!

<code><link rel="import" href="chunks.html"></code>:

<pre>
<script>/* script chunk A goes here */</script>
<script>/* script chunk B goes here */</script>
<script>/* script chunk C goes here */</script>
...
</pre>

*'''Parallelizes''' HTML parsing - first time the browser has been able to run two (or more) HTML parsers in parallel.
*'''Enables switching between debug and non-debug modes''' in an app, just by changing the import target itself. Your app doesn't need to know if the import target is a bundled/compiled resource or an import tree.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/webcomponents/imports/
}}