{{Page_Title|The Basics of HTML}}
{{Flags
|Checked_Out=No
}}
{{Byline}}
{{Summary_Section|In this article, you will learn the basics of HTML in order to gain some insight into the structure and content of an HTML
document.
}}
{{Guide
|Content=== Introduction ==
 
This article summarises the purpose and structure of HTML in a very high-level fashion, including how elements work, and what character references are. The articles that follow will drill down into much more detail on specific parts of the HTML language.
 
== What is HTML ==
 
Most desktop applications that read and write files use a special file
format. For example, Microsoft Word understands “.doc” files and
Microsoft Excel understands “.xls”. These files contain the
instructions on how to rebuild the documents next time you open 
them, what the contents of that document are, and “metadata” about the
article such as the author, the date the document was last modified,
even things such a list of changes made so you can go back and forth
between versions.
 
[[html|HTML (“HyperText Markup Language”)]] is a language to describe the 
contents of web documents. It uses a special syntax containing
markers (called “elements”) which are wrapped around the text within
the document to indicate how user agents (eg. web browsers) should interpret that
portion of the document.
 
A user agent is any software that is used to access web
pages on behalf of users. There is an important distinction to be made
here—all types of desktop browser software (Internet Explorer, Opera,
Firefox, Safari, Chrome etc.) and alternative browsers for other devices (such as the Wii Internet channel, and mobile phone browsers such as Opera Mini and WebKit on the iPhone) 
are user agents, but not all user agents are
browser software. The automated programs that Google and Yahoo! use
to index the web for their search engines are also user agents,
but no human being is controlling them directly.
 
== What HTML looks like ==
 
HTML is just a plain textual representation of content and its 
general meaning. For example:

<syntaxhighlight lang="html5"><p id="example">This is a paragraph.</p></syntaxhighlight>
 
The “<code>&lt;p&gt;</code>” part is a marker (which we refer to as a “tag”) that means
“what follows should be considered as a paragraph”.  Because it is at the start of the content it is affecting, this particular tag is an "opening tag". The
“<code>&lt;/p&gt;</code>” is a tag to indicate where the end of the paragraph is (which we refer to as a “closing tag”). The opening
tag, closing tag and everything in between is called an “element”. The <code>id="example"</code> is an attribute; you'll learn more about these later on.
Many people use the terms element and tag interchangeably however, which is not strictly correct. 
 
In most browsers there is a “Source” or “View Source” option, commonly under
the “View” menu. Try this now - go to your favorite website, choose this option, and spend some time looking at the HTML that makes up the structure of the page.

== The structure of an HTML document ==
 
A typical example HTML document looks like so:
 
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

This looks like so when rendered in a web browser:

[[File:HTMLrender.png]]
 
The document first starts with a document type element, or doctype. This mainly serves to get the browser to render the HTML in what is called "standards mode", so it will work correctly. It also lets validation software know what version of HTML to validate your code against. Don't worry too much about what this all means for now. We will come back to this later. What you can see here is the HTML5 doctype.
 
After this, you can see the opening tag of the <code>html</code> element. This
is a wrapper around the entire document. The closing <code>html</code> tag is the last thing in any HTML document. The html element should always have a <code>lang</code> attribute. This specifies the primary language for the page. For example, <code>en</code> means "English", <code>fr</code> means "French". There are tools available to help you find the right language tag, such as Richard Ishida's [http://rishida.net/utils/subtags/ Language Subtag Lookup tool].
 
Inside the <code>html</code> element, there is the <code>[[html/elements/head|head]]</code> element. This is a
wrapper to contain information about the document (the metadata). This is described in more detail in [[html/elements/head|The HTML head element]]. Inside the head is the <code>[[html/elements/title|title]]</code> element, which defines the “Example page” heading in the menu bar. Your <code>head</code> element should always contain a <code>meta</code> element with a <code>charset</code> attribute that identifies the character encoding of the page. (The one exception is when the page is encoded in UTF-16, but you should avoid that encoding anyway.) You should use UTF-8 whenever possible. Read [http://www.w3.org/International/getting-started/characters more about character encodings].
 
After the <code>[[html/elements/head|head]]</code> element there is a <code>[[html/elements/body|body]]</code> element, which is the
wrapper to contain the actual content of the page—in this case, only a level-one header (<code>[[html/elements/hn|h1]]</code>) element, which contains the text “Hello world.”

And that’s our document in full.
 
Elements often contain other elements. The body of
the document will invariably end up involving many nested elements.
Structural elements such as <code>article</code>, <code>header</code> and <code>div</code> create the overall structure of the document, and will
contain subdivisions. These will contain headings, paragraphs, lists
and so on. Paragraphs can contain elements that make links to other
documents, quotes, emphasis and so on. You will find out more about
these elements in later articles.

== The syntax of HTML elements ==
 
A basic element in HTML consists of two
markers around a block of text, and in almost every case elements can contain
sub-elements (such as <code>html</code> containing <code>head</code> and <code>body</code> in the
example above). There are some exceptions to the rule: some elements do not contain text or sub-elements, for example <code>img</code>. You'll learn more about these later on.
 
Elements can also have attributes, which can modify the behaviour
of the element and introduce extra meaning. Let's have a look at another example.
 
<syntaxhighlight lang="html5"><header>
  <h1>The Basics of 
    <abbr title="Hypertext Markup Language">HTML</abbr>
  </h1>
</header></syntaxhighlight>

This looks like so when rendered:

[[File:htmlrender2.png]]
 
In this example a <code>header</code> element (used to mark up header sections of documents) contains an <code>h1</code>
element (first, or most important level header), which in turn
contains some text. Part of that text is wrapped in an <code>abbr</code> element
(used to specify the expansion of abbreviations), which has a <code>title</code> attribute, the value of which is set to <code>Hypertext Markup
Language</code>.
 
Many attributes in HTML are common to all elements, though some are
specific to a given element or elements. They are always of the form
<code>keyword="value"</code>. The value is often surrounded by single or double quotes: this is not necessary in HTML5, except when the attribute value has multiple words, in which case you need to use quotes to make it clear that it is a single attribute value, and not several attributes. Saying all this, I would however recommend that you stick to quoting values for now, as it is good practice and can make the code easier to read. In addition, some HTML flavours you may work with in the future DO require quoting of attributes, for example XHTML 1.0, and it doesn't hurt to do so in flavours that don't.
 
[http://www.w3.org/TR/html401/index/attributes.html Attributes and their possible values are mostly defined by the HTML specifications]—you cannot make up your own attributes without making the HTML invalid, as this can confuse user agents and cause problems interpreting the web page correctly. The only real exceptions are the <code>id</code> and <code>class</code> attributes—their values are entirely under your control, as they are for defining custom meanings .
 
An element within another element is referred to as being a “child”
of that element. So in the above example, <code>abbr</code> is a child of the
<code>h1</code>, which is itself a child of the <code>header</code>. Conversely, the <code>header</code> element
would be referred to as a “parent” of the <code>h1</code> element. This parent/child concept is important, as it forms the basis of CSS and is heavily
used in JavaScript.

== Block level and inline elements ==
 
There are two general categories of elements in HTML, which
correspond to the types of content and structure those elements
represent—block level elements and inline elements.

Block level means a higher level element, normally informing the
structure of the document. It may help to think of block level
elements being those that start on a new line, breaking away
from what went before. Some common block level elements include
paragraphs, list items, headings and tables.

Inline elements are those that are contained within block level
structural elements and surround only small parts of the document’s content,
not entire paragrahs and groupings of content. An inline element will not cause a new line to
appear in the document: they are the kind of elements that would
appear in a paragraph of text. Some common inline elements include
hypertext links, highlighted words or phrases and short quotations.

Note: HTML5 redefines the element categories in HTML: see [http://www.whatwg.org/specs/web-apps/current-work/complete/section-index.html#element-content-categories Element content categories]. While these definitions are more accurate and less ambiguous than the ones that went before, they are a lot more complicated to understand than "block" and "inline". We will therefore stick with these throughout this course.

== Character references ==
 
One last item to mention in an HTML document is how to include
special characters. In HTML the characters <code>&lt;</code>, <code>&gt;</code> and <code>&amp;</code> are special.
They start and end parts of the HTML document, rather than
representing the characters less-than, greater-than and ampersand. For this reason, they must always be used in escaped form in content.

Other than for these characters, you should try to avoid using character references unless you are dealing with an invisible or ambiguous character. If you use the UTF-8 character encoding you can represent any character (other than the three mentioned above) without escaping.
 
One of the earliest mistakes a web author can make is to use an
ampersand in a document and then have something unexpected appear.
For example, writing “Imperial units measure weight in stones&amp;pounds” could actually end up appearing as “…stones£s” in some browsers.
 
This is because the literal string “&amp;pound;” is actually a character
reference in HTML. A character reference is a way of including a
character into a document that is difficult or impossible to enter
using a keyboard, or in a particular document encoding.
 
The ampersand (&amp;) introduces the reference and the semi-colon (;) ends
it. However, many user agents can be quite forgiving of HTML mistakes
such as leaving out the semi-colon, and treat “&amp;pound” as a character
reference. References can either be numbers (numeric references) or
shorthand words (entity references).
 
An actual ampersand has to be entered into a document as "&amp;amp;",
which is the character entity reference, or as "&amp;#38;" which is
the numeric reference. Web Platform Docs includes a [[html/entities#HTML_Entities_Table | Table of Common HTML Entities]] for reference.

For more information about working with character escapes see [http://www.w3.org/International/questions/qa-escapes Using character escapes in markup and CSS].
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