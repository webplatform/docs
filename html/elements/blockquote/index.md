---
title: blockquote
tags:
  - Markup
  - Elements
  - HTML
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Add Category, Parent, Children and Compatibility information.'
summary: 'The blockquote element indicates an extended quotation.'
uri: html/elements/blockquote

---
# blockquote

## Summary

The blockquote element indicates an extended quotation.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLQuoteElement](/dom/HTMLQuoteElement)

### Introduction

The **blockquote** element represents content that is quoted from another source, optionally with a citation which must be within a [**footer**](/html/elements/footer) or [**cite**](/html/elements/cite) element, and optionally with in-line changes such as annotations and abbreviations.

Content inside a **blockquote** other than citations and in-line changes must be quoted from another source, whose address, if it has one, may be cited in the [**cite** attribute](/html/attributes/cite).

<dl>
<dd>
Note: In cases where a page contains contributions from multiple people, such as comments on a blog post, 'another source' can include text from the same page, written by another person.

</dd>
</dl>
If the cite attribute is present, it must be a valid URL potentially surrounded by spaces. To obtain the corresponding citation link, the value of the attribute must be resolved relative to the element. User agents may allow users to follow such citation links, but they are primarily intended for private use (e.g. by server-side scripts collecting statistics about a site's use of quotations), not for readers.

The cite IDL attribute must reflect the element's cite content attribute.

## HTML Attributes

-   `cite` = valid URL potentially surrounded by spaces
    Specifies the address in the quotation source. [[Example B]](#Example_B)

## Examples

``` {.html}
<!-- This example uses the blockquote element to set off a quotation that renders as indented text: -->
<p>He said,
<blockquote cite="http://www.example.com">"Hi there!"</blockquote>
```

The **blockquote** element represents content that is quoted from another source, optionally with a citation which must be within a **footer** or **cite** element, and optionally with in-line changes such as annotations and abbreviations. For example, in English, abbreviations are traditionally identified using square brackets. Consider a page with the sentence "Fred ate the cracker. He then said he liked apples and fish."; it could be quoted as follows:

``` {.html}
<blockquote>
 <p>[Fred] then said he liked [...] fish.</p>
</blockquote>
```

Quotation marks may be used to delineate between quoted text and annotations within a **blockquote**.

``` {.html}
<!-- For example, an in-line note provided by the author: -->
<figure>
 <blockquote>
 "That monster custom, who all sense doth eat
 Of habit's devil," <abbr title="et cetera">&c.</abbr> not in Folio
 "What a falling off was there !
 From me, whose love was of that dignity
 That it went hand in hand even with the vow
 I made to her in marriage, and to decline
 Upon a wretch."
 </blockquote>
 <footer>
 — <cite class="title">Shakespeare manual</cite> by <cite class="author">Frederick Gard Fleay</cite>,
 p19 (in Google Books)
 </footer>
 </figure>
<!-- Note: In the example above, the citation is contained within the footer of a figure element, this groups and associates the information about the quote with the quote. The figcaption element was not used in this case as a container for the citation, as it is not a caption. -->
```

Attribution for the quotation may be be placed inside the **blockquote** element, but must be within a **cite** element for in-text attributions or within a **footer** element.

``` {.html}
<!-- For example, here the attribution is given in a footer after the quoted text, to clearly relate the quote to its attribution: -->
<blockquote>
 <p>I contend that we are both atheists. I just believe in one fewer
 god than you do. When you understand why you dismiss all the other
 possible gods, you will understand why I dismiss yours.</p>
 <footer>— <cite>Stephen Roberts</cite></footer>
 </blockquote>
```

``` {.html}
<!-- Here the attribution is given in a cite element on the last line of the quoted text. Note that a link to the author is also included. -->
<blockquote>
 The people recognize themselves in their commodities; they find their
 soul in their automobile, hi-fi set, split-level home, kitchen equipment.
 — <cite><a href="http://en.wikipedia.org/wiki/Herbert_Marcuse">Herbert Marcuse</a></cite>
 </blockquote>
```

``` {.html}
<!-- Here the attribution is given in a footer after the quoted text, and metadata about the reference has been added using the Microdata syntax (note it could have equally been marked up using RDFA Lite). -->
<blockquote>
  <p>... she said she would not sign any deposition containing the word "amorous" instead of "advances". For her the difference was of crucial significance, and one of the reasons she had separated from her husband was that he had never been amorous but had consistently made advances.</p>
  <footer itemscope itemtype="http://schema.org/Book">
    <span itemprop="author">Heinrich Böll</span>,
    <span itemprop="name">The Lost Honor of Katharina Blum</span>,
    <span itemprop="datePublished">January 1, 1974</span>
  </footer>
</blockquote>
<!-- Note: There is no formal method for indicating the markup in a blockquote is from a quoted source. It is suggested that if the footer or cite elements are included and these elements are also being used within a blockquote to identify citations, the elements from the quoted source could be annotated with metadata to identify their origin, for example by using the class attribute (a defined extensibility mechanism). -->
```

``` {.html}
<!-- In this example the source of a quote includes a cite element, which is annotated using the class attribute: -->
<blockquote>
  <p>My favorite book is <cite class="from-source">At Swim-Two-Birds</cite></p>
  <footer>- <cite>Mike[tm]Smith</cite></footer>
</blockquote>
```

The other examples below show other ways of showing attribution.

``` {.html}
<!-- Here a blockquote element is used in conjunction with a figure element and its figcaption: -->
<figure>
 <blockquote>
  <p>The truth may be puzzling. It may take some work to grapple with. It may be counterintuitive. It may contradict deeply held prejudices. It may not be consonant with what we desperately want to be true. But our preferences do not determine what's true. We have a method, and that method helps us to reach not absolute truth, only asymptotic approaches to the truth — never there, just closer and closer, always finding vast new oceans of undiscovered possibilities. Cleverly designed experiments are the key.</p>
 </blockquote>
 <figcaption><cite>Carl Sagan</cite>, in "<cite>Wonder and Skepticism</cite>", from the <cite>Skeptical Enquirer</cite> Volume 19, Issue 1 (January-February 1995)</figcaption>
</figure>
```

``` {.html}
<!-- This next example shows the use of cite alongside blockquote: -->
<p>His next piece was the aptly named <cite>Sonnet 130</cite>:</p>
<blockquote cite="http://quotes.example.org/s/sonnet130.html">
  <p>My mistress' eyes are nothing like the sun,<br>
  Coral is far more red, than her lips red,<br>
  ...
```

``` {.html}
<!-- This example shows how a forum post could use blockquote to show what post a user is replying to. The article element is used for each post, to mark up the threading. -->
<article>
 <h1><a href="http://bacon.example.com/?blog=109431">Bacon on a crowbar</a></h1>
 <article>
  <header><strong>t3yw</strong> 12 points 1 hour ago</header>
  <p>I bet a narwhal would love that.</p>
  <footer><a href="?pid=29578">permalink</a></footer>
  <article>
   <header><strong>greg</strong> 8 points 1 hour ago</header>
   <blockquote><p>I bet a narwhal would love that.</p></blockquote>
   <p>Dude narwhals don't eat bacon.</p>
   <footer><a href="?pid=29579">permalink</a></footer>
   <article>
    <header><strong>t3yw</strong> 15 points 1 hour ago</header>
    <blockquote>
     <blockquote><p>I bet a narwhal would love that.</p></blockquote>
     <p>Dude narwhals don't eat bacon.</p>
    </blockquote>
    <p>Next thing you'll be saying they don't get capes and wizard
    hats either!</p>
    <footer><a href="?pid=29580">permalink</a></footer>
    <article>
     <article>
      <header><strong>boing</strong> -5 points 1 hour ago</header>
      <p>narwhals are worse than ceiling cat</p>
      <footer><a href="?pid=29581">permalink</a></footer>
     </article>
    </article>
   </article>
  </article>
  <article>
   <header><strong>fred</strong> 1 points 23 minutes ago</header>
   <blockquote><p>I bet a narwhal would love that.</p></blockquote>
   <p>I bet they'd love to peel a banana too.</p>
   <footer><a href="?pid=29582">permalink</a></footer>
  </article>
 </article>
</article>
```

``` {.html}
<!-- This example shows the use of a blockquote for short snippets, demonstrating that one does not have to use p elements inside blockquote elements: -->
<p>He began his list of "lessons" with the following:</p>
<blockquote>One should never assume that his side of
the issue will be recognized, let alone that it will
be conceded to have merits.</blockquote>
<p>He continued with a number of similar points, ending with:</p>
<blockquote>Finally, one should be prepared for the threat
of breakdown in negotiations at any given moment and not
be cowed by the possibility.</blockquote>
<p>We shall now discuss these points...
```

## Notes

### Remarks

-   Examples of how to represent a conversation are shown in a later section; it is not appropriate to use the **cite** and **blockquote** elements for this purpose.

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/grouping-content.html#the-blockquote-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/grouping-content.html#the-blockquote-element)
:   W3C Recommendation
[HTML 4.01](http://www.w3.org/TR/html401/struct/text.html#edef-BLOCKQUOTE)
:   W3C Recommendation

## See also

### Related pages (internal)

-   `q`
-   `cite`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/HTML/Element/blockquote)

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

