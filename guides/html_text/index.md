{{Page_Title|HTML text}}
{{Flags}}
{{Byline}}
{{Summary_Section|This article talks about some of the most common elements used when marking up textual content using HTML.}}
{{Guide
|Content=== Introduction ==
 
In this article we will take you through the basics of using HTML to
markup the content within the body of your document.
 
We will look at general structural elements such as headings and
paragraphs and embedding quotes and code. After that we will look
at inline content, such as short quotes and emphasis, and finish with
a quick examination of old-fashioned presentational content.

'''Note''': You can [http://devfiles.myopera.com/articles/379/HTMLtext_examples.html view all the examples in this article running live].

== Space—the final frontier ==
 
An important point to cover before I start discussing text, though,
is that of space, specifically the space between words. When writing
HTML, the source document will contain what is termed “white space”
— the characters in the file that serve to separate text. An
actual space character, as you would get when you hit the Spacebar 
on the keyboard is the most common, but there are others such as the
Tab character and the marker between two separate lines in a document
(called a carriage return or new line).
 
In HTML, multiple occurrences of these characters are (almost) always
treated as a single space character. For example:
 
<pre>&lt;h3&gt;In   the
                beginning&lt;/h3&gt;</pre>

would be interpreted by a web browser to be equivalent to:
 
<pre>&lt;h3&gt;In the beginning&lt;/h3&gt;</pre>
 
The only place where this is not the case is in the <code>&lt;pre&gt;</code> element, 
which is discussed in detail later in this article.
 
This can be a source of confusion for first-time authors of an HTML
document, who may try to pad out text with extra spaces to achieve a
desired indentation, to get more spacing after the period between
sentences or to introduce more vertical space between paragraphs.
Influencing the visual layout of your documents is not something to
be done in the HTML source, and is instead achieved via CSS, discussed later in the series.

== Block level elements ==
 
In this section I’ll go through the syntax and usage of the common block level elements used to format text.
 
=== Page section headings ===
 
Each part of your web content, whether you are talking about a web site, a single content block or an article, should be introduced by an appropriate heading.
 
HTML defines six levels of heading, <code>&lt;h1&gt;</code>, <code>&lt;h2&gt;</code>, <code>&lt;h3&gt;</code>, <code>&lt;h4&gt;</code>, <code>&lt;h5&gt;</code>, and
<code>&lt;h6&gt;</code> (from the highest importance to the lowest). Generally speaking,
the <code>&lt;h1&gt;</code> would be the main heading of the entire page and introduce
everything. <code>&lt;h2&gt;</code> is then used to break the page up into sections,
<code>&lt;h3&gt;</code> the sub-sections, and so on.
 
It is important to use the heading levels to describe the document in
terms of section, sub-section, sub-sub-section as this makes the
[http://www.accessibilitytips.com/2008/03/10/avoid-skipping-header-levels/ document more understandable to screen readers] and to automated
processes (like Google’s indexing bots).
 
A good example of a header structure, using this article as a
template, would look like this:
 
<pre>&lt;h1&gt;Marking up textual content in HTML&lt;/h1&gt;
&lt;h2&gt;Introduction&lt;/h2&gt;
&lt;h2&gt;Space — the final frontier&lt;/h2&gt;
&lt;h2&gt;Block level elements&lt;/h2&gt;
&lt;h3&gt;Page section headings&lt;/h3&gt;
&lt;h3&gt;Generic paragraphs&lt;/h3&gt;
&lt;h3&gt;Quoting other sources&lt;/h3&gt;
&lt;h3&gt;Preformatted text&lt;/h3&gt;
&lt;h2&gt;Inline elements&lt;/h2&gt;

[…and so on…]</pre>

=== Generic paragraphs ===
 
The paragraph is the building block of most documents. In HTML a
paragraph is represented by the <code>&lt;p&gt;</code> element, which takes no special
attributes. For example:
 
<pre>&lt;p&gt;This is a very short paragraph. It only has two sentences.&lt;/p&gt;</pre>

A paragraph can contain just one sentence, but taking the literary meaning, further, you can't really call two words a paragraph. There is however no more suitable semantic element for marking up just two words of prose, so stick to the humble <code>&lt;p&gt;</code> element even in these cases, unless it is in fact a list item, heading, link or similar, in which case there will be a more suitable element available.

=== Quoting other sources ===
 
Very often articles, blog posts, and reference documents will quote another document in whole or in part. In HTML, this is marked up 
using the <code>&lt;blockquote&gt;</code> element for lengthy quotations, such as entire
sentences, paragraphs, lists, etc.
 
A <code>&lt;blockquote&gt;</code> element cannot contain text, but must instead have
another block level element inside it. You should use the same
block level element as was used in the original source you are quoting. If you 
are quoting a paragraph of text, use a paragraph; when quoting a
list of items, use the elements for lists; and so on.

If the quote comes from another web page, you can indicate this using
the <code>cite</code> attribute, like so:
 
<pre>&lt;p&gt;HTML 4.01 is the only version of HTML that you should use
when creating a new web page, as, according to the 
specification:&lt;/p&gt;
&lt;blockquote cite="http://www.w3.org/TR/html401/"&gt;
&lt;p&gt;This document obsoletes previous versions of HTML 4.0,
although W3C will continue to make those specifications and
their DTDs available at the W3C Web site.&lt;/p&gt;
&lt;/blockquote&gt;</pre>

The <code>cite</code> attribute doesn't really do anything on its own, although it is useful to keep a record of where the quotes are taken from. You could just JavaScript to extract this information from the <code>cite</code> attribute and do something meaningful with it, like open a new tab with that page loaded in it, for example.

=== Preformatted text ===
 
Any case in which the formatting and white space (see earlier) needs to be preserved should be marked up using the <code>&lt;pre&gt;</code> element. In this example, you can see a snippet of code written in the Perl programming language:
 
<pre>&lt;pre&gt;&lt;code class="language-perl"&gt;
# read in the named file in its entirety
sub slurp {
  my $filename = shift;
  my $file     = new FileHandle $filename;
                
  if ( defined $file ) {
    local $/;
    return &lt;$file&gt;;
  }
  return undef;
};
&lt;/code&gt;&lt;/pre&gt;</pre>
 
In most web browsers, text marked as preformatted will be displayed
to the user as it appears in the source, sometimes using a fixed-width
(monospaced) font, giving the text a feeling of having come from a
typewriter. This is an artifact of programmers using fixed width fonts for early uses of preformatted text.

Note: The use of the <code>&lt;code&gt;</code> element above will be explained in the [[Lesser - known semantic elements]] article later on in the course.

== Inline elements ==
 
In this section I’ll go through the syntax and usage of the common inline elements used to format text.
 
=== Short quotations ===
 
Short quotes used within a normal sentence or paragraph 
are contained within the <code>&lt;q&gt;</code> element. Like the <code>&lt;blockquote&gt;</code> element,
this can contain a <code>cite</code> attribute, which indicates the page on the
internet where the quote can be found.

A short quote should normally be rendered with quotation marks around
it. According to [http://www.w3.org/TR/html401/struct/text.html#h-9.2.2.1 the HTML specification], these should be
inserted by the user-agent so that they can be correctly nested and
made aware of the language being used in the document.
 
An example of <code>&lt;q&gt;</code> in action:
 
<pre>&lt;p&gt;This did not end well for me. Oh well, 
              &lt;q lang="fr"&gt;c'est la vie&lt;/q&gt; as the French say.&lt;/p&gt;</pre>

=== Emphasis ===
 
HTML contains four elements for indicating emphasis of some kind, such as important text like warnings, or subtle differences in meaning. For visual browsers this normally means applying a different colour, font or making the text bolder or italicised. For users of screen readers this can result in a different voice or other auditory effect.

==== &lt;em&gt; ====

For emphasis that subtly changes the meaning of a sentence, you use the <code>&lt;em&gt;</code> element, like 
so:
 
<pre>&lt;p&gt;&lt;em&gt;Please&lt;/em&gt; remember to unplug the kettle at night.&lt;/p&gt;</pre>

==== &lt;i&gt; ====

The <code>&lt;i&gt;</code> element used to mean italic in HTML4, and this was considered a bit naughty, as it was more of a presentational element than a semantic one (it just described what the element looked like, rather than what its meaning was - see below for more on these kinds of elements). HTML5 however redefines the meaning of <code>&lt;i&gt;</code>, saying that it "represents a span of text in an alternate voice or mood, or otherwise offset from the normal prose, such as a taxonomic designation, a technical term, an idiomatic phrase from another language, a thought, a ship name, or some other prose whose typical typographic presentation is italicised."

This does sound rather confusing, so here are some examples of where <code>&lt;i&gt;</code> would be appropriate:

<pre>&lt;p&gt;As we sailed into port, we spied the &lt;i&gt;Black Pearl&lt;/i&gt; moored at the dock.&lt;/p&gt;
 
&lt;p&gt;Book: &lt;i&gt;Living with a Diminutive Stature&lt;/i&gt;, Bruce Lawson, Peachpit Press,
published &lt;time pubdate="2011-08-01"&gt;1st August 2011&lt;/time&gt;,
ISBN 999-0-388-99999-6&lt;/p&gt;
 
&lt;p&gt;She really does add that little bit of &lt;i lang="fr"&gt;je ne sais quoi&lt;/i&gt;.&lt;/p&gt;</pre>

==== &lt;strong&gt; ====

The <code>&lt;strong&gt;</code> element indicates strong importance for its contents: that they are more important than surrounding content. For example:

&lt;p&gt;There are a total of twenty different species living inside this enclosure. &lt;strong&gt;Warning: Do not feed them: they will eat your shoes&lt;/strong&gt;.&lt;/p&gt;

==== &lt;b&gt; ====

The <code>&lt;b&gt;</code> element again used to be frowned upon because it described the look of the content, not its meaning. HTML5 has therefore redefined this element too: it is now meant to markup content that is stylistically offset from the rest of the text, but no more important in terms of its meaning. So for example, consider the most significant words in a product review or document abstract. An example follows:

<pre>&lt;p&gt;In this article, Chris Mills will show you how to combine &lt;b&gt;HTML5&lt;/b&gt;, &lt;b&gt;CSS3&lt;/b&gt;, &lt;b&gt;coloured card&lt;/b&gt;
and &lt;b&gt;string&lt;/b&gt; to create an attractive mobile for your child's bedroom.&lt;/p&gt;</pre>

==== Combining emphasis elements ====

You can combine and nest these different types of emphasis. For example, if an entire sentence was to be emphasised, but there was also a
point within that sentence that was more important, you could use
the <code>&lt;strong&gt;</code> and <code>&lt;em&gt;</code>elements together to indicate stronger emphasis than normal, like
so:
 
<pre>&lt;p&gt;&lt;em&gt;Please note: the kettle &lt;strong&gt;must&lt;/strong&gt; be unplugged every evening, otherwise it will explode -
&lt;strong&gt;killing us all&lt;/strong&gt;&lt;/em&gt;.&lt;/p&gt;</pre>

=== Small print ===

Another element  that was presentational and therefore naughty in HTML4, but that has been redefined in HTML5 is <code>&lt;small&gt;</code>.  It used to be a presentational element for making text appear smaller, but in HTML5 it is now used to mark up small print, such as legal restrictions, disclaimers, copyright notices, attribution statements, or licensing information. For example:

<pre>&lt;p&gt;&lt;small&gt;This content is released under a &lt;a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/"&gt;
Creative Commons Attribution Share-alike license&lt;/a&gt;.&lt;/small&gt;&lt;/p&gt;</pre>

=== Telling the time ===

New to HTML5, the <code>&lt;time&gt;</code> element gives you a way to unambiguously markup any times and dates you include in your text, allowing you to display them however you want to your readers, whilst including a consistent ISO-formatted date that machines can read. Here's an example:

<pre>&lt;p&gt;I was born on the &lt;time datetime="1978-06-27"&gt;27&lt;sup&gt;th&lt;/sup&gt; June 1978&lt;/time&gt;.&lt;/p&gt;</pre>

Because you can put whatever you want inbetween the opening and closing tags, you could write this any number of ways, while still keeping the date precise and machine readable:

<pre>&lt;p&gt;&lt;time datetime="1978-06-27"&gt;June 27 1978 - my birthday&lt;/time&gt;.&lt;/p&gt;</pre>

You can also add a time on to the date, appended to the end of the ISO-formatted string after a capital T, in 24 hour clock format:

<pre>&lt;p&gt;&lt;time datetime="1978-06-27T21:00"&gt;9pm on my birthday&lt;/time&gt;.&lt;/p&gt;</pre>
 
You can just specify the time if you want

<pre>&lt;p&gt;&lt;time datetime="21:00"&gt;9pm&lt;/time&gt;.&lt;/p&gt;</pre>

Although note that you can't currently specify a non-specific date, such as "August 2011" or "2011" - this is a bit limiting for say, museum web sites.

You can also add a number of seconds (after another colon), milliseconds (after a period) and a time zone offset (after a dash) after the time value. Check out the following:

<pre>&lt;p&gt;&lt;time datetime="1978-06-27T21:00:00.006-08:00"&gt;9pm and 6 milliseconds
on my birthday, in Pacific standard time&lt;/time&gt;.&lt;/p&gt;</pre>
 
Finally, you can also add a pubdate attribute to a <code>&lt;time&gt;</code> element, to specify that this datetime is the date and time that the particular piece of content was published:

<pre>&lt;p&gt;Published on &lt;time datetime="2011-07-20" pubdate&gt;July 27&lt;sup&gt;th&lt;/sup&gt; 2011&lt;/time&gt;.&lt;/p&gt;</pre>

== Presentational elements — never use these ==
 
The HTML 4 specification includes several elements that are widely
described as “presentational” because they only specify what the
content within them should look like, and not what it means. Most of these have been removed in the HTML5 specification.
 
We will describe them briefly here, but note that this is mostly of historic interest — these elements should never be used in any modern web page, although they are still used in HTML e-mails, which follow a non-standard set of rules. The effect of all of these elements should be achieved in another way, such as using CSS. 

=== &lt;font face="…" size="…"&gt; ===

The text within should be rendered by the browser using a font different from the default — instead, fonts should be set using CSS.

=== &lt;strike&gt; ===

The text within has been struck-through with a line — if this is merely a presentational effect, this should be achieved with CSS. Alternatively, if the text is actually being marked as having been deleted or unwanted it should be marked up with the <code>&lt;del&gt;</code> element, described in [[Lesser - known semantic elements]].

=== &lt;u&gt; ===

The text within has been underlined — this is almost always a visual effect, and so should be achieved with CSS.

=== &lt;tt&gt; ===

The text within is presented in a “teletype” or monospaced font — this should be achieved with CSS or a more appropriate semantic element such as <code>&lt;pre&gt;</code> (a block level element), shown above, or <code>&lt;code&gt;</code>, an inline element.

=== &lt;big&gt; ===

This makes the size of the text inside bigger — this should be achieved with CSS.
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=em
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=time
|Chrome_supported=Yes
|Chrome_version=6.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.1
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.0
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=em
|Android_supported=Yes
|Android_prefixed_supported=No
|Android_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_phone_supported=Yes
|IE_phone_prefixed_supported=No
|IE_phone_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=time
|Android_supported=Yes
|Android_version=2.2
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_phone_supported=Yes
|IE_phone_version=7.5
|IE_phone_prefixed_supported=No
|IE_phone_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=4.0
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}