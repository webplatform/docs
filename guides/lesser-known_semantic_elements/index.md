---
title: Lesser known semantic elements
readiness: 'Ready to Use'
summary: "This article discusses some of the lesser known and more\ninfrequently used semantic elements available in HTML.\n"
tags:
  - Tutorials
  - HTML
uri: 'guides/lesser-known semantic elements'

---
## Summary

This article discusses some of the lesser known and more infrequently used semantic elements available in HTML.

## Introduction

In this article we look at some of the and less well-known and used semantic elements in HTML. We'll look at marking up programming code, interaction with computers, citations and abbreviations, showing changes made to documents, and more.

## Highlighting contact information

The `<address>` element is probably the most poorly named and misunderstood element in HTML. At first glance, with a name like "address", it would appear that it is used to encapsulate addresses, email, postal, or otherwise. This is only partially the case.

The actual meaning of `<address>` is to supply contact information *for the author or authors* of the page, or for the major section of the page, that it appears within. This can take the form of a name, an email address, a postal address, or a link to another page with more contact information. For example:

``` html
<address>
  Mark Norman Francis,
  <span class="tel">1-800-555-4865</span>
</address>
```

 In the following example, the address is contained within the footer paragraph and simply links to another page on the site. The extended contact information on the page that this link targets could then have more detailed contact information, to save repeating it endlessly across the entire site.

``` html
<footer>
<p>© Copyright 2011</p>
<address>
<a href="/contact/">Mark Norman Francis</a>
</address>
</footer>
```

 Of course, if the site had more than one author, the same pattern could be used, just linking to different contact pages for the different authors.

It is **incorrect** to use the `<address>` element to indicate any other type of addresses, such as this:

``` html
<p> Our company address: </p>
<address>
  Opera Software ASA,
  Waldemar Thranes gate 98,
  NO-0175 OSLO,
  NORWAY
</address>
```

 (Unless, of course, Opera was taking collective responsibility for the content as the "author" of the article.)

For any general address, you can use something called a "microformat" to indicate that a paragraph contains an address.

## Programming languages and code

The `<code>` element is used to indicate computer code or programming languages, such as PHP, JavaScript, CSS, or XML. For short samples within a sentence, you would simply wrap the element around the code snippet, like so:

``` html
<p>It is bad form to use event handlers like
<code>onclick</code> directly in the HTML.</p>
```

 For larger samples of code which span multiple lines, you can use a preformatted block `<pre>...</pre>` as shown in the [HTML Text](/guides/html_text) article.

Although there is no defined method for indicating which programming language or code is shown within the `<code>` element, you can use the `class` attribute. A common practice (mentioned in the HTML 5 specification) is to use the prefix `<language->` and then append the language name. So the above example would become:

``` html
<p>It is bad form to use event handlers like
<code class="language-javascript">onclick</code>
directly in the HTML.</p>
```

 Some programming languages have names that cannot be easily represented in classes, such as C\# (C-Sharp). The correct way of writing this would be "`<class='language-c\#'>`", where the "\\" indicates "treat the next character literally". This, of course, could be confusing and could easily be mis-typed. We recommend using a class consisting of only letters and hyphens, and spelling it out completely. So in this case, use "`<class='language-csharp'>`" instead.

## Displaying computer interaction

The two elements `<samp>` and `<kbd>` can be used to indicate the input and output of interaction with a computer program. For example:

``` html
<p>One common method of determining if a computer is connected
to the internet is to use the computer program <code>ping</code>
to see if a computer likely to be running is reachable.</p>

<pre><samp class="prompt">kittaghy%</samp> <kbd>ping -o google.com</kbd>
  <samp>PING google.com (64.233.187.99): 56 data bytes
  64 bytes from 64.233.187.99: icmp_seq=0 ttl=242 time=108.995 ms

  --- google.com ping statistics ---
  1 packets transmitted, 1 packets received, 0% packet loss
  round-trip min/avg/max/stddev = 108.995/108.995/108.995/0.000 ms
</samp></pre>
```

 The `<samp>` element indicates sample output from a computer program. As shown in the example, different types of output can be indicated using the `class` attribute. There are no widely adopted conventions for which kind of classes to use, however.

The `<kbd>` element indicates input from the user interacting with the computer. Although this is traditionally keyboard input (hence the "kbd" contraction) it should also be used to indicate other types of input, such as spoken voice.

## Variables

The `<var>` element is used to indicate variables in textual content. This can include variables in algebraic mathematical expressions or within programming code. For example:

``` html
<p>The value of <var>x</var> in
 3<var>x</var>+2=14 is 4.</p>

<pre><code class="language-perl">
my <var>$welcome</var> = "Hello world!";
</code></pre>
```

## Citations

The `<cite>` element is used to indicate where the nearby content comes from. When quoting a person, a book or other publication, or generally referring people to another source, that source should be wrapped in a `<cite>` element. For example:

``` html
<p>The saying <q>Everything should be made as simple as possible,
but not simpler</q> is often attributed to <cite>Albert
Einstein</cite>, but it is actually a paraphrasing of a quote which
is much less easy to understand.</p>
```

## Abbreviations

The `<abbr>` element is used to indicate where abbreviations occur, and to provide a method for expanding them without unnecessarily interrupting the flow of the document.

The text that is the abbreviation gets wrapped in the `<abbr>` element, and the full expansion is placed in the `title` attribute, like this:

``` html
<p>Styling is added to
<abbr title="Hypertext Markup Language">HTML</abbr> documents
using <abbr title="Cascading Style Sheets">CSS</abbr>.</p>
```

 Note that in the HTML4 specification there is also an element called `<acronym>`, which had a similar function to `<abbr>`, but for acronyms. This was dropped in HTML5 because the functional difference between an acronym and an abbreviation isn't distinct enough to require different elements.

One problem with this is Internet Explorer support: Internet Explorer (before version 7, and 7 doesn't provide the dotted underline underneath abbreviations that other browsers do) doesn't recognise the `<abbr>` element, but does recognise `<acronym>`. But this is easy enough to get around. To ensure that `<abbr>` will be stylable in Internet Explorer, just create the element with JavaScript. Put this code in your document `<head>`:

``` html
<script type="text/javascript">document.createElement('abbr');</script>
```

 To find out more about why this works, see the [HTML Structural Elements](/guides/html_structural_elements) article. Of course, you could just stick to using `<acronym>` for now, until you decide to make a complete move toward HTML5.

## Defining instances

There is some confusion over the proper use of `<dfn>`, which is described in the HTML specification as "the defining instance of the enclosed term". This is remarkably close to the idea of the `<dt>` element (definition term) used in definition lists.

The difference is that the term used in `<dfn>` does not have to be a part of a list of terms and descriptions and can instead be used as part of the normal flow of text, even in conversational style prose. So, let's look at an example of using `<dfn>`:

``` html
<p><dfn>HTML</dfn>: HTML stands for "HyperText Markup Language". This is
the language used to describe the contents of web documents.</p>
```

 The term HTML appears in the text, and is followed immediately by a definition of what it is; therefore, this is an ideal place for the `<dfn>` element to be used. You should really only use it once on a page, where a term is first defined, but terms should only really be defined once on a page anyway, so this is not too troubling.

This is all well and good, but an isolated example is not very practical — the use of `<dfn>` is recommended when an abbreviation is used more than once on a page. For example, in any article about HTML, the abbreviation "HTML" could appear dozens of times. To use the code "`<abbr title="HyperText Markup Language">HTML</abbr>`" each and every time it is seen would be a waste of bandwidth, visually distracting, and for screen reader users probably quite tiresome as HTML is expanded over and over, even though they would already have been told what it stands for. Instead, the code could be inserted only at the point where it is first defined for the readers:

``` html
<p><dfn><abbr>HTML</abbr></dfn> ("HyperText Markup Language") is
a language to describe the contents of web documents.</p>
```

 Then later, whenever "HTML" is used, it can be marked up simply as "`<abbr>HTML</abbr>`". A user agent could then make available to the user some method of retrieving the defining instance of that abbreviation. Unfortunately, no user agent currently does this, including screen readers. It would be better, then, to use the `title` attribute as well to provide this information:

``` html
<p><dfn><abbr title="HyperText Markup Language">HTML</abbr></dfn> ("HyperText Markup Language") is a language
to describe the contents of web documents.</p>
```

 Unfortunately, we have now doubled up on the expanded term for "HTML", which can be a problem for screen reader users. However, leaving out the visible expansion makes the document less useful for sighted users, which will be the greater proportion of users in almost every case.

We suggest that this is an acceptable trade-off when there are only one or two items requiring a definition. In pages that require a larger number of definitions, it might be better to create a glossary section or page where the more rigourous definition list markup can be used. If you are very concerned about this, the code could instead appear as:

``` html
<p><abbr title="HyperText Markup Language">HTML</abbr>
(<dfn>HyperText Markup Language</dfn>) is a language to
describe the contents of web documents.</p>
```

 However, the user agent would still need some method of connecting the definition with all the instances of the defined term. No browser currently does anything useful with `<dfn>`, although it is still a useful hook for CSS to style. The solution suggested above is currently the best we've got.

This is an unfortunate instance where the specification has been created without clear guidelines on how an element is supposed to be used, and probably was not based upon any real-world usage of that element; otherwise, there would be a method of combining the term with its full description or definition. The HTML5 specification goes into [[more detail](http://www.whatwg.org/specs/web-apps/current-work/multipage/text-level-semantics.html#the-dfn-element)] about how dfn is used, but this is still in draft and not suitable for use on the web yet.

## Superscript and subscript

To mark up a part of some text as being super- or subscripted (slightly raised or lowered compared to the rest of the text) you use the `<sup>` and `<sub>` elements.

Some languages require these elements for correct rendering of abbreviations, and it can be used when a small amount of mathematical content is being marked up, without resorting to using MathML (a specific, rather heavyweight mathematical markup language, created for the sole purpose of marking up complex mathematical formulas).

An example of both types:

``` html
<p>The chemical formula for water is H<sub>2</sub>O, and it
is also known as hydrogen hydroxide.</p>
<p>The famous formula for mass-energy equivalence as derived
by Albert Einstein is E=mc<sup>2</sup> — energy
is equal to the mass multiplied by the speed of light
squared.</p>
```

## Line breaks

Because of the way HTML defines white space, it is not possible to control where lines of text break (such as marking up a postal address as a paragraph, but wanting the visual appearance to have each part of the address appear on a separate line) by simply pressing the Return key whilst writing the text.

A line break can be introduced into the document using the `<br>` element. However, this should only be used to force line breaks where they are required, and never to apply more vertical spacing between paragraphs or such in a document; that is of course more properly done with CSS.

Sometimes it might be easier to use the preformatted text block rather than inserting `<br>` elements. Or, if one particular part of some text is desired to be on a line by itself, but this is just a styling issue, it can be surrounded by a `<span>` element and set to display as a block level element.

For example, you could write the Opera contact address seen earlier in this article like this instead:

``` html
<p>Our company address: </p>
<address>
Opera Software ASA,<br>Waldemar Thranes gate 98,<br>
NO-0175 OSLO,<br>NORWAY
</address>
```

 Of course, if you are writing XHTML style syntax rather than HTML, the element should be self-closing: `<br />`.

## Horizontal rules

A horizontal rule is created in HTML with the `<hr>` element. It inserts into the document a line, which is described to represent a boundary between different sections of a document.

Whilst some argue that this is inherently non-semantic and purely a visual, presentational effect, there is actually some precedent in literature for such an element to exist. Within a chapter (which could be described as a section within a book), a horizontal rule may appear between scenes that occur in different times and/or places. Also, poetry can use decorative breaks to separate different stanzas of the poem.

Neither use would justify the existence of a new header element, which is the accepted way of marking the boundaries between document sections.

The `<hr>` element has no uncommon attributes and should be styled using CSS if the default appearance is unsatisfactory.

Also, like the line break, if you are writing XHTML style syntax and not HTML, use the self-closing form: `<hr />`.

## Changes to documents (inserting, deleting and outdated content)

If a document has been changed since the first time it was available, you can mark these changes so that return visitors or automated processes can tell what has changed, and when.

New text (insertions) should be surrounded by the `<ins>` element. Text that has been removed (deletions) should be surrounded by the `<del>` element. If a deletion and insertion have been made at the same point in the document, good form suggests having the deleted text first, followed by the insertion.

Both elements can take two attributes that give more meaning to the edits.

If the reason for the change is stated in the page or elsewhere on the web, you should link to that document or fragment in the `cite` attribute. This effectively says "This change happened for this reason."

You can also indicate the time at which the change was made by using a `datetime` attribute. The value should be an ISO-standard timestamp, which is generally of the form "YYYY-MM-DD HH:MM:SS ±HH:MM". See [this Wikipedia article](http://en.wikipedia.org/wiki/ISO_8601) for more information.

An example using both attributes:

``` html
<p>We should only solve problems that actually arise. As
<cite><del datetime="2008-03-25 18:26:55 Z"
cite="/changes.html#revision-4">Donald Knuth</del><ins
datetime="2008-03-25 18:26:55 Z"
cite="/changes.html#revision-4">C. A. R. Hoare</ins></cite>
said: <q>premature optimization is the root of all
evil</q>.</p>
```

 We can also use the `<s>` element to markup content that is outdated, perhaps if you want to mark it for future updating or deletion. For example:

``` html
<p><s>The president of the USA is currently Barack Obama</s>.</p>
```

## Conclusion

Although the elements in this article are less well known than some of their fellows, they are no less useful. You should of course use whichever elements are appropriate to the content they mark up, regardless of popularity. Usage promotes familiarity, and familiarity promotes usage!
