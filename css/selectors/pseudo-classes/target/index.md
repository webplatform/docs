Some URIs refer to a location within a resource. This kind of URI ends with a "number sign" (#) followed by an anchor identifier (called the fragment identifier).

URIs with fragment identifiers link to a certain element within the document, known as the target element. For instance, here is a URI pointing to an anchor named section_2 in an HTML document:

<pre>http://example.com/html/top.html#section_2</pre>

A target element can be represented by the <code>:target</code> pseudo-class. If the document's URI has no fragment identifier, then the document has no target element.

==Example:==
<syntaxhighlight lang="css">p.note:target</syntaxhighlight>

This selector represents a [[html/elements/p|p]] element of [[css/selectors/class|class]] note that is the target element of the referring URI.

==CSS example:==
Here, the :target pseudo-class is used to make the target element red and place an image before it, if there is one:

<syntaxhighlight lang="css">
*:target { color : red }
*:target::before { content : url(target.png) }
</syntaxhighlight>

[[Category:CSS]]