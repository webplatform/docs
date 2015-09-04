---
title: data-*
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Review import; Compatibility table; link examples to our code.webplatform.org playground; fix see also'
uri: 'html/attributes/data-*'

---
# dataset and data-\*

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Applies to
:    ?

##### 3.2.3.9 Embedding custom non-visible data with the \<a href="\#attr-data-\*"\>data-\*\</a\> attributes

A <dfn id="custom-data-attribute">custom data attribute</dfn> is an attribute in no namespace whose name starts with the string "<dfn id="attr-data-.2A" title="attr-data-*">`data-`</dfn>", has at least one character after the hyphen, is \<a href="infrastructure.html\#xml-compatible"\>XML-compatible\</a\>, and contains no \<a href="infrastructure.html\#uppercase-ascii-letters"\>uppercase ASCII letters\</a\>.

All attribute names on \<a href="infrastructure.html\#html-elements"\>HTML elements\</a\> in \<a href="infrastructure.html\#html-documents"\>HTML documents\</a\> get ASCII-lowercased automatically, so the restriction on ASCII uppercase letters doesn't affect such documents.

\<a href="\#custom-data-attribute" title="custom data attribute"\>Custom data attributes\</a\> are intended to store custom data private to the page or application, for which there are no more appropriate attributes or elements.

These attributes are not intended for use by software that is independent of the site that uses the attributes.

For instance, a site about music could annotate list items representing tracks in an album with custom data attributes containing the length of each track. This information could then be used by the site itself to allow the user to sort the list by track length, or to filter the list for tracks of certain lengths.

    <ol>
     <li data-length="2m11s">Beyond The Sea</li>
     ...
    </ol>

It would be inappropriate, however, for the user to use generic software not associated with that music site to search for tracks of a certain length by looking at this data.

This is because these attributes are intended for use by the site's own scripts, and are not a generic extension mechanism for publicly-usable metadata.

Every \<a href="infrastructure.html\#html-elements" title="HTML elements"\>HTML element\</a\> may have any number of \<a href="\#custom-data-attribute" title="custom data attribute"\>custom data attributes\</a\> specified, with any value.

* * * * *

<var title>element</var> . `<a href="#dom-dataset">dataset</a>`
:   Returns a `<a href="infrastructure.html#domstringmap-0">DOMStringMap</a>` object for the element's `<a href="#attr-data-*">data-*</a>` attributes.

    Hyphenated names become camel-cased. For example, `data-foo-bar=""` becomes `element.dataset.fooBar`.



The <dfn id="dom-dataset" title="dom-dataset">`dataset`</dfn> IDL attribute provides convenient accessors for all the `<a href="#attr-data-*">data-*</a>` attributes on an element. On getting, the `<a href="#dom-dataset">dataset</a>` IDL attribute must return a `<a href="infrastructure.html#domstringmap-0">DOMStringMap</a>` object, associated with the following algorithms, which expose these attributes on their element:

The algorithm for getting the list of name-value pairs
:   1.  Let <var title>list</var> be an empty list of name-value pairs.
    2.  For each content attribute on the element whose first five characters are the string "`data-`" and whose remaining characters (if any) do not include any \<a href="infrastructure.html\#uppercase-ascii-letters"\>uppercase ASCII letters\</a\>, in the order that those attributes are listed in the element's <span>attributes list</span>, add a name-value pair to <var title>list</var> whose name is the attribute's name with the first five characters removed and whose value is the attribute's value.
    3.  For each name <var title>list</var>, for each "-" (U+002D) character in the name that is followed by a \<a href="infrastructure.html\#lowercase-ascii-letters" title="lowercase ASCII letters"\>lowercase ASCII letter\</a\>, remove the "-" (U+002D) character and replace the character that followed it by the same character \<a href="infrastructure.html\#converted-to-ascii-uppercase"\>converted to ASCII uppercase\</a\>.
    4.  Return <var title>list</var>.

The algorithm for setting names to certain values
:   1.  Let <var title>name</var> be the name passed to the algorithm.
    2.  Let <var title>value</var> be the value passed to the algorithm.
    3.  If <var title>name</var> contains a "-" (U+002D) character followed by a \<a href="infrastructure.html\#lowercase-ascii-letters" title="lowercase ASCII letters"\>lowercase ASCII letter\</a\>, throw a `<a href="infrastructure.html#syntaxerror">SyntaxError</a>` exception and abort these steps.
    4.  For each \<a href="infrastructure.html\#uppercase-ascii-letters" title="uppercase ASCII letters"\>uppercase ASCII letter\</a\> in <var title>name</var>, insert a "-" (U+002D) character before the character and replace the character with the same character \<a href="infrastructure.html\#converted-to-ascii-lowercase"\>converted to ASCII lowercase\</a\>.
    5.  Insert the string `data-` at the front of <var title>name</var>.
    6.  Set the value of the attribute with the name <var title>name</var>, to the value <var title>value</var>, replacing any previous value if the attribute already existed. If `setAttribute()` would have thrown an exception when setting an attribute with the name <var title>name</var>, then this must throw the same exception.

The algorithm for deleting names
:   1.  Let <var title>name</var> be the name passed to the algorithm.
    2.  For each \<a href="infrastructure.html\#uppercase-ascii-letters" title="uppercase ASCII letters"\>uppercase ASCII letter\</a\> in <var title>name</var>, insert a "-" (U+002D) character before the character and replace the character with the same character \<a href="infrastructure.html\#converted-to-ascii-lowercase"\>converted to ASCII lowercase\</a\>.
    3.  Insert the string `data-` at the front of <var title>name</var>.
    4.  Remove the attribute with the name <var title>name</var>, if such an attribute exists. Do nothing otherwise.

The same object must be returned each time.

If a Web page wanted an element to represent a space ship, e.g. as part of a game, it would have to use the `<a href="#classes">class</a>` attribute along with `<a href="#attr-data-*">data-*</a>` attributes:

    <div class="spaceship" data-ship-id="92432"
         data-weapons="laser 2" data-shields="50%"
         data-x="30" data-y="10" data-z="90">
     <button class="fire"
             onclick="spaceships[this.parentNode.dataset.shipId].fire()">
      Fire
     </button>
    </div>

Notice how the hyphenated attribute name becomes camel-cased in the API.

Authors should carefully design such extensions so that when the attributes are ignored and any associated CSS dropped, the page is still usable.

User agents must not derive any implementation behavior from these attributes or values. Specifications intended for user agents must not define these attributes to have any meaningful values.

JavaScript libraries may use the \<a href="\#custom-data-attribute" title="custom data attribute"\>custom data attributes\</a\>, as they are considered to be part of the page on which they are used. Authors of libraries that are reused by many authors are encouraged to include their name in the attribute names, to reduce the risk of clashes. Where it makes sense, library authors are also encouraged to make the exact name used in the attribute names customizable, so that libraries whose authors unknowingly picked the same name can be used on the same page, and so that multiple versions of a particular library can be used on the same page even when those versions are not mutually compatible.

For example, a library called "DoQuery" could use attribute names like `data-doquery-range`, and a library called "jJo" could use attributes names like `data-jjo-range`. The jJo library could also provide an API to set which prefix to use (e.g. `J.setDataPrefix('j2')`, making the attributes have names like `data-j2-range`).

**Needs Examples**: This section should include examples.

## See also

### External resources

-   Imported from: \<a href="[http://www.w3.org/html/wg/drafts/html/master/dom.html\#embedding-custom-non-visible-data-with-the-data-\*-attributes](http://www.w3.org/html/wg/drafts/html/master/dom.html#embedding-custom-non-visible-data-with-the-data-*-attributes)"\>[http://www.w3.org/html/wg/drafts/html/master/dom.html\#embedding-custom-non-visible-data-with-the-data-\*-attributes](http://www.w3.org/html/wg/drafts/html/master/dom.html#embedding-custom-non-visible-data-with-the-data-*-attributes)\</a.

