{{Page_Title|The Basics of HTML}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Byline
|Name=
|URL=
|Published=
}}
{{Summary_Section|In this article, you will learn the basics of HTML and gain some insight into the structure and content of an HTML
document.
}}
{{Guide
|Content=== Introduction ==
 
This article summarises the purpose and structure of HTML in a very high-level fashion, including how elements work, and what character references are. The articles that follow will go into more detail on specific parts of the HTML language.
 
== What is HTML? ==
 
Most desktop applications that read and write files use specific file
formats. For example, Microsoft Word uses ".doc" files and
Microsoft Excel uses ".xls". These files contain the
instructions on how to build the documents when they are opened, 
the contents of the document, and ''metadata'' about the
document such as the author, the last modified date, and possibly
even a list of changes.
 
[[html|HTML (''HyperText Markup Language'')]] is a language used to describe the 
contents of web documents. It uses a syntax containing
markers (called ''elements'') that are wrapped around content in
the document to indicate how user agents (e.g., web browsers) should interpret that
portion of the document.
 
A ''user agent'' is any software that is used to access web
pages on behalf of users. There is an important distinction to be made
here — all types of desktop browsers (such as Internet Explorer, Opera,
Firefox, Safari, and Chrome) as well as alternative browsers for other devices 
(such as the Wii Internet channel, and mobile phone browsers like Opera Mini and WebKit on the iPhone) 
are user agents, but not all user agents are
browsers. For example, the automated programs that Google and Yahoo! use
to index the web for their search engines are user agents,
but no human being is controlling them directly.
 
== What HTML looks like ==
 
HTML is a plain textual representation of content and its general meaning. For example:

<syntaxhighlight lang="html5"><p id="example">This is a paragraph.</p></syntaxhighlight>
 
The <code>&lt;p&gt;</code> part is a marker, commonly called a ''tag'', that means
"what follows should be considered as a paragraph".  Because it is at the start of the content it affects, it is an "opening tag". Likewise, the
<code>&lt;/p&gt;</code> tag indicates the end of the paragraph, and is thus a "closing tag". The opening
tag, closing tag, and everything in between is called an ''element''.  Note:
Many people use the terms "element" and "tag" interchangeably, which is incorrect. 
(The <code>id="example"</code> is an ''attribute-value pair''; we'll come back to these later.)
 
In most browsers there is a "Source" or "View Source" option, commonly under
the "View" menu. Try this now: go to a web site, choose this option, and spend some time looking at the HTML that makes up the page.

== The structure of an HTML document ==
 
A typical HTML document might look like this:
 
<syntaxhighlight lang="html5"><!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Example page</title>
  </head>
  <body>
    <h1>Hello world</h1>
  </body>
</html></syntaxhighlight>

That document might look like this when rendered in a web browser:

[[File:HTMLrender.png]]
 
The document starts with a document type element, or ''doctype'', in this case the HTML5 doctype. 
This mainly serves to get the browser to render the HTML in what is called "standards mode", so it will work correctly. 
It also lets validation software know what version of HTML to validate your code against. 
 
Next, you can see the opening tag of the <code>&lt;html&gt;</code> element. This
is a wrapper around the entire document. The closing <code>&lt;/html&gt;</code> tag is the last thing in any HTML document. 
The <code>html</code> element should always have a <code>lang</code> attribute. This specifies the primary language for the page. For example, <code>en</code> means "English", <code>fr</code> means "French". There are tools available to help you find the right language tag, such as Richard Ishida's [http://rishida.net/utils/subtags/ Language Subtag Lookup tool].
 
Inside the <code>html</code> element, there is the <code>[[html/elements/head|head]]</code> element. This is a
wrapper that contains information about the document ("data about the data", or ''metadata''). This is described in more detail in 
[[html/elements/head|The HTML head element]]. Inside the <code>head</code> is the <code>[[html/elements/title|title]]</code> element, 
which defines the "Example page" heading in the brower's title bar. The <code>head</code> element should always contain a 
<code>meta</code> element with a <code>charset</code> attribute that identifies the character encoding of the page. 
(The one exception is when the page is encoded in UTF-16, but you should avoid that encoding anyway.) 
You should use UTF-8 whenever possible. See [http://www.w3.org/International/getting-started/characters this W3C article] for more about character encodings.
 
After the <code>[[html/elements/head|head]]</code> element there is a <code>[[html/elements/body|body]]</code> element, which is the
wrapper that surrounds the actual content of the page — in this case, a level-one heading (<code>[[html/elements/hn|h1]]</code>) element, which contains the text "Hello world".

And that's our document in full.

== The syntax of HTML elements ==
 
A basic element in HTML consists of two markers around a block of content.
Elements also often contain other elements, referred to as ''nested elements''. The body of
a document invariably contains many nested elements.
Structural elements such as <code>article</code>, <code>header</code>, and <code>div</code> create the overall structure of the document, 
and will themselves contain headings, paragraphs, lists,
and other elements. Paragraphs can contain elements that create links to other
documents, quotes, emphasis, and so on.
Nearly any element can contain nested elements, although
there are exceptions: some elements do not contain either text or nested elements, 
for example <code>img</code>.
 
An element within another element is also referred to as a "child" element. So in the above example, <code>abbr</code> is a child of 
<code>h1</code>, which is itself a child of <code>header</code>. Conversely, the <code>header</code> element
would be referred to as the "parent" of the <code>h1</code> element, which is the parent of <code>abbr</code>. 
This parent/child concept is important, as it forms the basis of CSS (Cascading Stylesheet Specification) and is heavily used in JavaScript.
 
Elements can also have attributes, which can modify the appearance and/or behaviour
of the element and introduce extra meaning. Let's look at another example.
 
<syntaxhighlight lang="html5"><header>
  <h1>The Basics of 
    <abbr title="Hypertext Markup Language">HTML</abbr>
  </h1>
</header></syntaxhighlight>

This looks like so when rendered in a browser:

[[File:htmlrender2.png]]
 
In this example, a <code>header</code> element contains an <code>h1</code>
heading element, which in turn
contains some text. Part of that text is wrapped in an <code>abbr</code> element
(used to specify the expansion of abbreviations), which has a <code>title</code> attribute, the value of which is <code>Hypertext Markup
Language</code>.
 
Many attributes in HTML are common to all elements, though some are
specific to certain elements. They are always of the form
<code>keyword="value"</code>. The value is often surrounded by single or double quotes. While this is not required in HTML5 
(except when the attribute value has multiple words separated by white space), you should always quote values, 
as it is good practice and can make the code easier to read. In addition, some HTML dialects do require quoting of attributes, 
for example XHTML 1.0, and it doesn't hurt to do so in dialects that don't require it.
 
Attributes and their possible values are mostly defined by the [http://www.w3.org/TR/html401/index/attributes.html W3C HTML specifications].
You cannot make up your own attributes without invalidating the HTML, and this can confuse user agents and cause problems interpreting the web 
page correctly.<!-- The only real exceptions are the <code>id</code> and <code>class</code> attributes — their values are entirely under your control, as they are for defining custom meanings.-->

== Block and inline elements ==
 
There are two general categories of elements in HTML, which
correspond to the types of content and structure they
represent: ''block'' elements and ''inline'' elements.

Block elements are at a higher level, normally helping to define the
structure of the document. It may help to think of block
elements as those that start on a new line, breaking away
from the previous content. Some common block level elements include
paragraphs, lists, headings, and tables.

Inline elements are are contained within block 
elements and typically surround only small parts of the document's content. 
Inline elements do not cause a new line to
appear in the document; rather, they 
appear inside a line of text. Some common inline elements include
hypertext links, bold or italic text, spans, and short quotations.

Note: HTML5 redefines the element categories in HTML: see
[http://www.whatwg.org/specs/web-apps/current-work/complete/section-index.html#element-content-categories Element content categories]. 
While these definitions are more accurate and less ambiguous, they are more difficult to understand than "block" and "inline". 
We will therefore stick with these terms in this course.

== Character references ==
 
One last item to mention in an HTML document is how to include
special characters. In HTML the characters <code>&lt;</code>, <code>&gt;</code> and <code>&amp;</code> are special.
They start and end parts of the HTML document, rather than
representing the printable less-than, greater-than, and ampersand characters. 
For this reason they must always be coded in a special way in document content.

One of the easiest mistakes to make in a web page is to use &lt; and &gt; signs in text and have the browser
render your content in an unexpected way. For example, if you write
"The paragraph tag (&lt;p&gt;) is very common.", intending for it to look just like that, the browser will render it as 
The paragraph tag (<p>) is very common.</p>

This is clearly not what you wanted or expected.

The solution to this problem is to encode, or "escape", the two signs by representing them with character references. 
The character reference for less-than is "&amp;lt;", and the character reference for greater-than is "&amp;gt;".
Thus, to get that line to look the way you want, you would write
"The paragraph tag (&amp;lt;p&amp;gt;) is very common", which the browser would render as
"The paragraph tag (&lt;p&gt;) is very common", as you intended.
In these encodings, the ampersand (&amp;) starts the reference and the semicolon (;) ends it.

Character references can also be numeric. For example, you can escape an ampersand character with either
its shorthand word <code>&amp;amp;</code> or its numeric reference <code>&amp;#38;</code>.
<!--
One of the earliest mistakes a web author can make is to use an
ampersand in a document and then have something unexpected appear.
For example, writing "Imperial units measure weight in stones&amp;pounds" 
could actually end up appearing as "…stones£s" in some browsers.
 
This is because the literal string "&amp;pound;" is actually a character
reference in HTML. A character reference is a way of including a
character into a document that is difficult or impossible to enter
using a keyboard, or in a particular document encoding.
 
The ampersand (&amp;) introduces the reference and the semi-colon (;) ends
it. However, many user agents can be quite forgiving of HTML mistakes
such as leaving out the semi-colon, and treat "&amp;pound" as a character
reference. References can either be numbers (numeric references) or
shorthand words (entity references).
 
An actual ampersand has to be entered into a document as "&amp;amp;",
which is the character entity reference, or as "&amp;#38;" which is
the numeric reference. 
-->

Web Platform Docs includes a [[html/entities#HTML_Entities_Table|Table of Common HTML Entities]] for reference.

Other than these characters, you should try to avoid using character references unless you are dealing with an invisible or ambiguous character. 
If you use the UTF-8 character encoding you can represent any character (other than those mentioned above) without escaping them.

For more information about working with character escapes, see [http://www.w3.org/International/questions/qa-escapes Using character escapes in markup and CSS].
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Languages|guides/the_basics_of_html}}









{{API_Name}}


{{Examples_Section
|Not_required=Yes
|Examples=
}}

{{Related_Specifications_Section
|Specifications=
}}