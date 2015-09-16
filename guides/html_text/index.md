---
title: HTML text
readiness: 'Ready to Use'
summary: 'This article talks about some of the most common elements used when marking up text content in HTML.'
tags:
  - Guides
  - HTML
uri: 'guides/html text'

---
## Summary

This article talks about some of the most common elements used when marking up text content in HTML.

## Introduction

In this article we will take you through the basics of using HTML to mark up the content within the body of your document.

We will first look at general structural elements such as headings and paragraphs, and how to embed long quotes and code. After that we will look at inline content, such as short quotes and emphasis, and finish with a quick examination of old-fashioned presentational markup.

## Space — the final frontier

Before we discuss text, we should discuss the space between the text. HTML documents contain non-printing characters known as *white space* that separate text. The regular space character (the space bar on a keyboard) is the most common, but there are others such as the tab character and the carriage return (or new line) character.

In HTML, multiple contiguous occurrences of these characters are almost always treated as a single space character. Consider this source code:

``` html
<h3>In   the
                beginning</h3>
```

 It would be interpreted by a web browser to be equivalent to:

``` html
<h3>In the beginning</h3>
```

 The only time this is not the case is when the `<pre>` element is used, which we will discuss later in this article.

White space compression can be a source of confusion for novice HTML authors, who may try to pad out text with extra spaces to achieve a desired indentation, to get more spacing after the period between sentences, or to introduce more vertical space between paragraphs. Remember, HTML is a content language, not a style language; visual layout should not be attempted in the HTML source, and should instead be achieved via CSS.

## Block elements

*Block elements* are those that create a line break before and after the element. In this section we will look at the syntax and usage of some common block elements.

### Page section headings

Each part of your web content should be introduced by an appropriate heading.

HTML defines six heading levels: `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, and `<h6>` (from the highest importance to the lowest). Generally speaking, the `<h1>` would be the main heading of the page. You would then use `<h2>` to break the page up into sections, `<h3>` to define the sub-sections, and so on.

It is important to use the heading levels to describe the document hierarchically, and to not skip or incorrectly nest different levels, as this makes the document more understandable to screen readers and to automated processes like indexing bots. See [this article](http://www.accessibilitytips.com/2008/03/10/avoid-skipping-header-levels/) for more information.

A good example of a header structure, using this article as a template, might look like this:

``` html
<h1>Marking up textual content in HTML</h1>
<h2>Introduction</h2>
<h2>Space — the final frontier</h2>
<h2>Block elements</h2>
<h3>Page section headings</h3>
<h3>Generic paragraphs</h3>
<h3>Quoting other sources</h3>
<h3>Preformatted text</h3>
<h2>Inline elements</h2>

[...and so on...]
```

### Generic paragraphs

The *paragraph* is the primary building block of most documents. In HTML a paragraph is represented by the `<p>` element. For example:

``` html
<p>This is a very short paragraph. It only has two sentences.</p>
```

 A paragraph can contain any amount of text, from a single character to thousands of words, but is typically used in the standard literary sense to contain one to a few sentences. However, there's no need to overuse `<p>`; if the content is actually a list, heading, link, or other specific type of content, there are many suitable elements available.

### Quoting other sources

Articles, blog posts, and reference documents often quote sections of text from another document, called a *block quote*. In HTML, this kind of quotation is marked up using the `<blockquote>` element.

While, technically, a `<blockquote>` element can directly contain text that is not enclosed in other elements, it is bad practice, and will probably cause your code to not validate. Instead, you should nest other elements inside `<blockquote>`. When quoting from another source, you should use the same type of elements: when quoting a paragraph of text, use a paragraph tag; when quoting a list of items, use the list tags; and so on.

If you want, you can indicate the source of the quote using the `cite` attribute, like this:

``` html
<p>HTML 4.01 is the only version of HTML that you should use
when creating a new web page, according to the
specification:</p>
<blockquote cite="http://www.w3.org/TR/html401/">
<p>This document obsoletes previous versions of HTML 4.0,
although W3C will continue to make those specifications and
their DTDs available at the W3C website.</p>
</blockquote>
```

 Depending on default and user-defined styles, the above content might render like this in the browser:

HTML 4.01 is the only version of HTML that you should use when creating a new web page, according to the specification:

> This document obsoletes previous versions of HTML 4.0, although W3C will continue to make those specifications and their DTDs available at the W3C website.

Note that the `cite` attribute doesn't really do anything on its own, although it is useful to keep a record of the quote's source in the same page location as the quote itself.

### Preformatted text

Any case in which the formatting and white space should be preserved, such as code examples, should be marked up using the *preformatted* element `<pre>`. In this example, you see a snippet of code written in the Perl programming language:

``` html
<pre><code class="language-perl">
# read in the named file in its entirety
sub slurp {
  my $filename = shift;
  my $file     = new FileHandle $filename;

  if ( defined $file ) {
    local $/;
    return <$file>;
  }
  return undef;
};
</code></pre>
```

 In the browser, that snippet is rendered exactly as written, including white space:

    <code class="language-perl">
    # read in the named file in its entirety
    sub slurp {
      my $filename = shift;
      my $file     = new FileHandle $filename;

      if ( defined $file ) {
        local $/;
        return <$file>;
      }
      return undef;
    };
    </code>

In most web browsers, text marked as preformatted will be displayed to the user as it appears in the source, usually using a fixed width (monospace) font, giving the text a feeling of having come from a typewriter or printer. This is an artifact of older computers, which had only fixed width fonts, but is quite handy today for code examples and other content that is best displayed without browser modification.

Note: The use of the `<code>` element is covered in the [Lesser-known semantic elements](/tutorials/lesser-known_semantic_elements) article.

## Inline elements

*Inline elements* are those that do not create a line break before or after the element. In this section we will look at the syntax and usage of some common inline elements.

### Short quotations

Short quotes used within a normal sentence or paragraph are contained within the *quote* element `<q>`. Like `<blockquote>`, this element can contain a `cite` attribute that indicates the source of the quote.

A short quote should normally be rendered with quotation marks around it. According to the [HTML specification](http://www.w3.org/TR/html401/struct/text.html#h-9.2.2.1), these should be inserted by the user agent so that they can be correctly nested and so that quote characters appropriate to the document's language can be used.

Here's an example of `<q>` in action, with a `lang` attribute:

``` html
<p>This did not end well for me. Oh well,
<q lang="fr">c'est la vie</q>, as the French say.</p>
```

 In the browser, that paragraph will render like this (note the European quote characters):

This did not end well for me. Oh well, “c'est la vie”, as the French say.

### Emphasis

HTML contains four elements for indicating emphasis, a way to differentiate specific text from its surrounding content. For browsers this normally means making the text bold or italicised. For screen readers it can result in a different voice or other auditory effect.

#### \<em\>

For emphasis that subtly changes the meaning of a sentence, you use the *emphasis* element `<em>`, like this:

``` html
<p><em>Please</em> remember to unplug the kettle at night.</p>
```

 Most browsers render `<em>` as italic text:

*Please* remember to unplug the kettle at night.

#### \<i\>

The `<i>` element used to mean *italic* in HTML4, but this was considered bad practice, as it was more of a presentational element than a semantic one. That is, it just described what the element looked like, rather than what its meaning was. (See below for more on these kinds of elements.) HTML5, however, redefines the meaning of `<i>`, saying that it "represents a span of text in an alternate voice or mood, or otherwise offset from the normal prose, such as a taxonomic designation, a technical term, an idiomatic phrase from another language, a thought, a ship name, or some other prose whose typical typographic presentation is italicised."

That does sound rather confusing, so here are some examples of where `<i>` would be appropriate:

``` html
<p>As we sailed into port, we spied the <i>Black Pearl</i> moored at the dock.</p>
<p>She really does add that little bit of <i lang="fr">je ne sais quoi</i>.</p>
```

 In the browser, that renders exactly as you expect:

As we sailed into port, we spied the *Black Pearl* moored at the dock.

She really does add that little bit of *je ne sais quoi*.

#### \<strong\>

The *strong* element `<strong>` indicates particular importance for its content, declaring that it is more important than its surrounding content. For example:

``` html
<p>There are twenty different species living inside this enclosure.
<strong>Warning! Do not feed them: they will eat your shoes.</strong></p>
```

 Most browsers render `<strong>` as bold text:

There are twenty different species living inside this enclosure. **Warning! Do not feed them: they will eat your shoes.**

#### \<b\>

Like `<i>`, the *bold* element `<b>` used to be frowned upon because it described the look of the content, not its meaning. HTML5 has therefore redefined this element as well; it now "identifies content that is stylistically offset from the rest of the text, but no more important in terms of its meaning." Consider the most significant words in a product review or document abstract, as in this example:

``` html
<p>In this article, Chris Mills will show you how to combine <b>HTML5</b>, <b>CSS3</b>, <b>coloured card</b>,
and <b>string</b> to create an attractive mobile for your child's bedroom.</p>
```

 Also like `<i>`, this renders as expected:

In this article, Chris Mills will show you how to combine **HTML5**, **CSS3**, **coloured card**, and **string** to create an attractive mobile for your child's bedroom.

#### Combining emphasis elements

You can combine and nest these different types of emphasis. For example, if an entire sentence was to be emphasised, but there was also a point within the sentence that was more important, you could use the `<strong>` and `<em>` elements together to indicate stronger emphasis than normal:

``` html
<p><em>Please note: The kettle <strong>must</strong> be unplugged every evening, otherwise it will explode --
<strong>killing us all!</strong></em></p>
```

 The browser will render that paragraph like this:

*Please note: The kettle **must** be unplugged every evening, otherwise it will explode -- **killing us all!***

### Small print

The *small* element `<small>` is another element that was originally presentational and therefore considered bad practice in HTML4, but has been redefined in HTML5. It used to be an element for making ordinary text appear in a smaller font, but in HTML5 it is now properly used to mark up small print, such as legal restrictions, disclaimers, copyright notices, attribution statements, or licensing information. For example:

``` html
<p><small>This content is released under a
Creative Commons Attribution Share-alike license.</small></p>
```

 In the browser, that will render as:

<small>This content is released under a Creative Commons Attribution Share-alike license.</small>

### Telling the time

New to HTML5, the *time* element `<time>` gives you a way to unambiguously mark up times and dates you include in your text, allowing you to display them however you want, whilst including a consistent ISO-formatted date that machines can read. Here's an example:

``` html
<p>I was born on the <time datetime="1978-06-27">27<sup>th</sup> June 1978</time>.</p>
```

 Because you can put whatever you want in between the opening and closing tags, you could write this any number of ways, while still keeping the date precise and machine readable:

``` html
<p><time datetime="1978-06-27">June 27 1978 - my birthday</time>.</p>
```

 You can also add a time to the date, appended to the end of the ISO-formatted string after a capital T, in 24 hour clock format:

``` html
<p><time datetime="1978-06-27T21:00">9pm on my birthday</time>.</p>
```

 Or you can just specify the time if you want:

``` html
<p><time datetime="21:00">9pm</time>.</p>
```

 Note, however, that you cannot currently specify a non-specific date, such as "August 2011" or "2011".

You can also add a number of seconds (after another colon), milliseconds (after a period), and a time zone offset (after a dash) following the time value. For example:

``` html
<p><time datetime="1978-06-27T21:00:00.006-08:00">9pm and 6 milliseconds
on my birthday, in Pacific standard time</time>.</p>
```

 Finally, you can also add a *publication date* attribute `pubdate` to a `<time>` element, to specify that the datetime value represents when the content was published:

``` html
<p>Published on <time datetime="2011-07-20" pubdate>July 27<sup>th</sup> 2011</time>.</p>
```

## Presentational elements — never use these

In addition to `<i>`, `<b>`, and `<small>`, the HTML4 specification includes several other elements that are strictly presentational because they only specify what the content within them should look like, and not what it means. The use of these elements is discouraged, and most have been removed from the HTML5 specification.

We will describe them briefly here, but note that this is mostly for historic interest — these elements should never be used in a modern web page. To achieve these text effects, you should use CSS.

### \<font face="..." size="..."\>

The *font* element indicates that the text should be rendered using a font different from the default. Use CSS instead.

### \<strike\>

The *strike* element indicates that the text should be struck-through with a line. Use CSS instead.

### \<u\>

The *u* element indicates that the text should be underlined (underscored). Not only should this be done with CSS instead, but it should rarely be done at all, because most readers will interpret the underscore as a hyperlink. Of course, because it isn't a hyperlink, clicking it will do nothing — except frustrate your readers.

### \<tt\>

The *tt* element indicates that the text should be presented in a "teletype" or monospace font. An alternative to using CSS to achieve this effect would be to use the semantic elements `<pre>` for block content or `<code>` for inline content.

### \<big\>

The *big* element indicates that the text should be rendered in a larger font.

## Conclusion

In this article we have looked at the basics of HTML text markup, including headings, paragraphs, quotes, code, and various emphasis elements. When you are comfortable with these concepts, please move on to the other tutorials in this series, which cover HTML lists, images, links, tables, and more.
