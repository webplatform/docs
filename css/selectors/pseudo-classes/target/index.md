{{Page Title|:target pseudo-class}}
{{Flags|State=Not Ready}}
{{Topics|CSS}}

Some URIs refer to a location within a resource. This kind of URI ends with a "number sign" (<tt>#</tt>) followed by an anchor identifier (called the fragment identifier).

URIs with fragment identifier links to a certain element within the document, known as the target element. For instance, here is a URI pointing to an anchor named <tt>section_2</tt> in an HTML document  (e.g. <tt>&lt;div id="section_2"&gt;...&lt;/div&gt;</tt>), and we can refer to it with its matching URI <tt>http://example.com/html/top.html#section_2</tt>

A target element can be represented by the <code>:target</code> pseudo-class. If the document's URI has no fragment identifier, then the document has no target element.

== Using the selector ==
<syntaxHighlight>
  .note:target { /* ... */ }
</syntaxHighlight>

This selector represents any element that has a class Name [[css/selectors/class|class]] <tt>note</tt> that is also targeted by the current URI.

Here, the <tt>:target</tt> pseudo-class is used to make the target element red and place an image before it, if there is one:

<syntaxhighlight lang="css">
*:target { color : red }
*:target::before { content : url(target.png) }
</syntaxhighlight>