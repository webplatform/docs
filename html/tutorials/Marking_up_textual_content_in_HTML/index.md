---
title: Marking up textual content in HTML
tags:
  - Tutorials
  - WSC
  - HTML
uri: 'html/tutorials/Marking up textual content in HTML'
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'Lesser - known semantic elements'

---
## Introduction

In this article we will take you through the basics of using HTML to markup the content within the body of your document.

We will look at general structural elements such as headings and paragraphs and embedding quotes and code. After that we will look at inline content, such as short quotes and emphasis, and finish with a quick examination of old-fashioned presentational content.

**Note**: You can [view all the examples in this article running live](http://devfiles.myopera.com/articles/379/HTMLtext_examples.html).

## Space—the final frontier

An important point to cover before I start discussing text, though, is that of space, specifically the space between words. When writing HTML, the source document will contain what is termed “white space” — the characters in the file that serve to separate text. An actual space character, as you would get when you hit the Spacebar on the keyboard is the most common, but there are others such as the Tab character and the marker between two separate lines in a document (called a carriage return or new line).

In HTML, multiple occurrences of these characters are (almost) always treated as a single space character. For example:

    <h3>In   the
                    beginning</h3>

would be interpreted by a web browser to be equivalent to:

    <h3>In the beginning</h3>

The only place where this is not the case is in the `<pre>` element, which is discussed in detail later in this article.

This can be a source of confusion for first-time authors of an HTML document, who may try to pad out text with extra spaces to achieve a desired indentation, to get more spacing after the period between sentences or to introduce more vertical space between paragraphs. Influencing the visual layout of your documents is not something to be done in the HTML source, and is instead achieved via CSS, discussed later in the series.

## Block level elements

In this section I’ll go through the syntax and usage of the common block level elements used to format text.

### Page section headings

Each part of your web content, whether you are talking about a web site, a single content block or an article, should be introduced by an appropriate heading.

HTML defines six levels of heading, `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, and `<h6>` (from the highest importance to the lowest). Generally speaking, the `<h1>` would be the main heading of the entire page and introduce everything. `<h2>` is then used to break the page up into sections, `<h3>` the sub-sections, and so on.

It is important to use the heading levels to describe the document in terms of section, sub-section, sub-sub-section as this makes the [document more understandable to screen readers](http://www.accessibilitytips.com/2008/03/10/avoid-skipping-header-levels/) and to automated processes (like Google’s indexing bots).

A good example of a header structure, using this article as a template, would look like this:

    <h1>Marking up textual content in HTML</h1>
    <h2>Introduction</h2>
    <h2>Space — the final frontier</h2>
    <h2>Block level elements</h2>
    <h3>Page section headings</h3>
    <h3>Generic paragraphs</h3>
    <h3>Quoting other sources</h3>
    <h3>Preformatted text</h3>
    <h2>Inline elements</h2>

    […and so on…]

### Generic paragraphs

The paragraph is the building block of most documents. In HTML a paragraph is represented by the `<p>` element, which takes no special attributes. For example:

    <p>This is a very short paragraph. It only has two sentences.</p>

A paragraph can contain just one sentence, but taking the literary meaning, further, you can't really call two words a paragraph. There is however no more suitable semantic element for marking up just two words of prose, so stick to the humble `<p>` element even in these cases, unless it is in fact a list item, heading, link or similar, in which case there will be a more suitable element available.

### Quoting other sources

Very often articles, blog posts, and reference documents will quote another document in whole or in part. In HTML, this is marked up using the `<blockquote>` element for lengthy quotations, such as entire sentences, paragraphs, lists, etc.

A `<blockquote>` element cannot contain text, but must instead have another block level element inside it. You should use the same block level element as was used in the original source you are quoting. If you are quoting a paragraph of text, use a paragraph; when quoting a list of items, use the elements for lists; and so on.

If the quote comes from another web page, you can indicate this using the `cite` attribute, like so:

    <p>HTML 4.01 is the only version of HTML that you should use
    when creating a new web page, as, according to the
    specification:</p>
    <blockquote cite="http://www.w3.org/TR/html401/">
    <p>This document obsoletes previous versions of HTML 4.0,
    although W3C will continue to make those specifications and
    their DTDs available at the W3C Web site.</p>
    </blockquote>

The `cite` attribute doesn't really do anything on its own, although it is useful to keep a record of where the quotes are taken from. You could just JavaScript to extract this information from the `cite` attribute and do something meaningful with it, like open a new tab with that page loaded in it, for example.

### Preformatted text

Any case in which the formatting and white space (see earlier) needs to be preserved should be marked up using the `<pre>` element. In this example, you can see a snippet of code written in the Perl programming language:

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

In most web browsers, text marked as preformatted will be displayed to the user as it appears in the source, sometimes using a fixed-width (monospaced) font, giving the text a feeling of having come from a typewriter. This is an artifact of programmers using fixed width fonts for early uses of preformatted text.

Note: The use of the `<code>` element above will be explained in the [Lesser - known semantic elements](/w/index.php?title=Lesser_-_known_semantic_elements&action=edit&redlink=1) article later on in the course.

## Inline elements

In this section I’ll go through the syntax and usage of the common inline elements used to format text.

### Short quotations

Short quotes used within a normal sentence or paragraph are contained within the `<q>` element. Like the `<blockquote>` element, this can contain a `cite` attribute, which indicates the page on the internet where the quote can be found.

A short quote should normally be rendered with quotation marks around it. According to [the HTML specification](http://www.w3.org/TR/html401/struct/text.html#h-9.2.2.1), these should be inserted by the user-agent so that they can be correctly nested and made aware of the language being used in the document.

An example of `<q>` in action:

    <p>This did not end well for me. Oh well,
                  <q lang="fr">c'est la vie</q> as the French say.</p>

### Emphasis

HTML contains four elements for indicating emphasis of some kind, such as important text like warnings, or subtle differences in meaning. For visual browsers this normally means applying a different colour, font or making the text bolder or italicised. For users of screen readers this can result in a different voice or other auditory effect.

#### \<em\>

For emphasis that subtly changes the meaning of a sentence, you use the `<em>` element, like so:

    <p><em>Please</em> remember to unplug the kettle at night.</p>

#### \<i\>

The `<i>` element used to mean italic in HTML4, and this was considered a bit naughty, as it was more of a presentational element than a semantic one (it just described what the element looked like, rather than what its meaning was - see below for more on these kinds of elements). HTML5 however redefines the meaning of `<i>`, saying that it "represents a span of text in an alternate voice or mood, or otherwise offset from the normal prose, such as a taxonomic designation, a technical term, an idiomatic phrase from another language, a thought, a ship name, or some other prose whose typical typographic presentation is italicised."

This does sound rather confusing, so here are some examples of where `<i>` would be appropriate:

    <p>As we sailed into port, we spied the <i>Black Pearl</i> moored at the dock.</p>

    <p>Book: <i>Living with a Diminutive Stature</i>, Bruce Lawson, Peachpit Press,
    published <time pubdate="2011-08-01">1st August 2011</time>,
    ISBN 999-0-388-99999-6</p>

    <p>She really does add that little bit of <i lang="fr">je ne sais quoi</i>.</p>

#### \<strong\>

The `<strong>` element indicates strong importance for its contents: that they are more important than surrounding content. For example:

\<p\>There are a total of twenty different species living inside this enclosure. \<strong\>Warning: Do not feed them: they will eat your shoes\</strong\>.\</p\>

#### \<b\>

The `<b>` element again used to be frowned upon because it described the look of the content, not its meaning. HTML5 has therefore redefined this element too: it is now meant to markup content that is stylistically offset from the rest of the text, but no more important in terms of its meaning. So for example, consider the most significant words in a product review or document abstract. An example follows:

    <p>In this article, Chris Mills will show you how to combine <b>HTML5</b>, <b>CSS3</b>, <b>coloured card</b>
    and <b>string</b> to create an attractive mobile for your child's bedroom.</p>

#### Combining emphasis elements

You can combine and nest these different types of emphasis. For example, if an entire sentence was to be emphasised, but there was also a point within that sentence that was more important, you could use the `<strong>` and `<em>`elements together to indicate stronger emphasis than normal, like so:

    <p><em>Please note: the kettle <strong>must</strong> be unplugged every evening, otherwise it will explode -
    <strong>killing us all</strong></em>.</p>

### Small print

Another element that was presentational and therefore naughty in HTML4, but that has been redefined in HTML5 is `<small>`. It used to be a presentational element for making text appear smaller, but in HTML5 it is now used to mark up small print, such as legal restrictions, disclaimers, copyright notices, attribution statements, or licensing information. For example:

    <p><small>This content is released under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/">
    Creative Commons Attribution Share-alike license</a>.</small></p>

### Telling the time

New to HTML5, the `<time>` element gives you a way to unambiguously markup any times and dates you include in your text, allowing you to display them however you want to your readers, whilst including a consistent ISO-formatted date that machines can read. Here's an example:

    <p>I was born on the <time datetime="1978-06-27">27<sup>th</sup> June 1978</time>.</p>

Because you can put whatever you want inbetween the opening and closing tags, you could write this any number of ways, while still keeping the date precise and machine readable:

    <p><time datetime="1978-06-27">June 27 1978 - my birthday</time>.</p>

You can also add a time on to the date, appended to the end of the ISO-formatted string after a capital T, in 24 hour clock format:

    <p><time datetime="1978-06-27T21:00">9pm on my birthday</time>.</p>

You can just specify the time if you want

    <p><time datetime="21:00">9pm</time>.</p>

Although note that you can't currently specify a non-specific date, such as "August 2011" or "2011" - this is a bit limiting for say, museum web sites.

You can also add a number of seconds (after another colon), milliseconds (after a period) and a time zone offset (after a dash) after the time value. Check out the following:

    <p><time datetime="1978-06-27T21:00:00.006-08:00">9pm and 6 milliseconds
    on my birthday, in Pacific standard time</time>.</p>

Finally, you can also add a pubdate attribute to a `<time>` element, to specify that this datetime is the date and time that the particular piece of content was published:

    <p>Published on <time datetime="2011-07-20" pubdate>July 27<sup>th</sup> 2011</time>.</p>

## Presentational elements — never use these

The HTML 4 specification includes several elements that are widely described as “presentational” because they only specify what the content within them should look like, and not what it means. Most of these have been removed in the HTML5 specification.

We will describe them briefly here, but note that this is mostly of historic interest — these elements should never be used in any modern web page, although they are still used in HTML e-mails, which follow a non-standard set of rules. The effect of all of these elements should be achieved in another way, such as using CSS.

### \<font face="…" size="…"\>

The text within should be rendered by the browser using a font different from the default — instead, fonts should be set using CSS.

### \<strike\>

The text within has been struck-through with a line — if this is merely a presentational effect, this should be achieved with CSS. Alternatively, if the text is actually being marked as having been deleted or unwanted it should be marked up with the `<del>` element, described in [Lesser - known semantic elements](/w/index.php?title=Lesser_-_known_semantic_elements&action=edit&redlink=1).

### \<u\>

The text within has been underlined — this is almost always a visual effect, and so should be achieved with CSS.

### \<tt\>

The text within is presented in a “teletype” or monospaced font — this should be achieved with CSS or a more appropriate semantic element such as `<pre>` (a block level element), shown above, or `<code>`, an inline element.

### \<big\>

This makes the size of the text inside bigger — this should be achieved with CSS.

## Summary

In this article, we have talked about some of the most common elements used when marking up textual content. In the next article, [HTML lists](/guides/html_lists), you will progress to another type of content: lists of items.

Note: This material was originally published as part of the Opera Web Standards Curriculum, available as [15: Marking up textual content in HTML](http://dev.opera.com/articles/view/15-marking-up-textual-content-in-html/), written by Mark Norman Francis. Like the original, it is published under the [Creative Commons Attribution, Non Commercial - Share Alike 2.5](http://creativecommons.org/licenses/by-nc-sa/2.5/) license.