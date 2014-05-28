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

See the irony? The web's most basic content, HTML, requires the greatest amount of effort to work with. Fortunately, [http://w3c.github.io/webcomponents/explainer/ Web Components] are here to get us back on track.

==Getting started==

[http://w3c.github.io/webcomponents/spec/imports/ HTML Imports], part of the [http://w3c.github.io/webcomponents/explainer/ Web Components] cast, is a way to include HTML documents in other HTML documents. You're not limited to markup either. An import can also include CSS, JavaScript, or anything else an .html file can contain. In other words, this makes imports a '''fantastic tool for loading related HTML/CSS/JS.'''

===The basics===

Include an import on your page by declaring a <link rel="import">:

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

'''Fact!''' The browser's network stack automatically de-dupes all requests from the same URL. This means that imports that reference the same URL are only retrieved once. No matter how many times an import at the same location is loaded, it only executes once.

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

'''Tip!''' Also '''Enable experimental Web Platform features''' to get the other bleeding edge web component goodies.


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