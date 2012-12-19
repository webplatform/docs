{{Page_Title|DOCTYPES and markup styles}}
{{Flags
|High-level issues=Move Candidate
|Editorial notes={{Editorial/Move_Candidate
| Seems out of place.  Should be under /html/tutorials/ or /html/guides
}}
}}
{{Byline}}
{{Summary_Section|In this article we will explore the different doctypes you are likely to come across on your journey around the Web, as well as look at how XHTML and HTML differ.}}
{{Guide
|Content=== Introduction ==
The doctype appears just above the <code>&lt;html&gt;</code> tag, at the very start of each document you write:

<pre>&lt;!DOCTYPE html&gt;
&lt;html lang="en-GB"&gt;
&lt;head&gt;
  &lt;meta charset="utf-8"&gt;
  &lt;title&gt;My fabulous document&lt;/title&gt;

   ... etc</pre>

The doctype explains what type of HTML is to be expected and therefore what spec validators (for example [http://validator.w3.org/ the W3C HTML validator]) should validate your document against.

== Standards versus quirks mode ==

The doctype also serves to make the browser render the page in so called "standards mode".  In standards mode, browsers generally try to render the page according to the CSS specifications — they trust that the person who created the document knew what they were doing. 

On the other hand, if a browser finds an outdated, incomplete of missing doctype at the start of the page, they use “quirks mode”, which is more backwards compatible with old practices and old browsers. Quirks mode assumes that the document is old or that it has not been created with web standards in mind — it means that the web page will still render, but the browser will work a bit harder in doing so, and you’ll likely get a strange or ugly result, which you weren’t quite expecting.  The differences are mostly related to how CSS is rendered, and only in a few cases about how the actual HTML is treated. As a web designer or developer, you will get the most consistent results by making sure that all browsers use their Standards rendering mode, hence you should stick to web standards, and use a proper doctype!

== The HTML5 doctype and friends ==

In this course, we are sticking with the HTML5 doctype:

<pre>&lt;!DOCTYPE html&gt;</pre>

There is no disadvantage to using this doctype, and it is certainly a lot easier to remember than the others! This is the one we'd recommend you use going forward, as even if you don't plan to start using any of the new HTML5 features in your work yet, it will still validate most of the HTML 4/XHTML 1.0 features (there are a couple of exceptions where features have been removed from the spec, but as you'll learn later, validation is merely a useful tool, and not the be all and end all of everything), and will be future proof for when you do start using new HTML5 features. There are however, other doctypes that you may come across when working on various projects. Let's look at some of the others you might bump into.

=== The HTML 4.01 strict doctype ===

<pre>&lt;!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01//EN"
"http://www.w3.org/TR/html4/strict.dtd"&gt;</pre>

The HTML 4.01 strict doctype validates against the HTML 4.01 spec, although it doesn't allow any presentational markup or deprecated elements (such as <code>&lt;font&gt;</code> elements) or framesets to be used. It validates loose HTML style markup, such as minimized attributes and non-quoted attributes (eg. <code>required</code>, rather than <code>required="required"</code>).

=== The HTML 4.01 transitional doctype ===

<pre>&lt;!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
"http://www.w3.org/TR/html4/loose.dtd&gt;</pre>

The HTML 4.01 transitional doctype validates against the HTML 4.01 spec. It allows some presentational markup and deprecated elements (such as <code>&lt;font&gt;</code> elements) but not framesets. Again, it validates loose HTML style markup.

=== The XHTML 1.0 strict and transitional doctypes ===

<pre>&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd"&gt;</pre>

and

<pre>&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;</pre>

These are the exact XHTML 1.0 equivalents of the HTML 4.01 doctypes we discussed above, so functionally they are the same, except that they won't validate loose HTML style markup: it all needs to be well formed XML.

=== The HTML 4.01 and XHTML 1.0 frameset doctypes ===

If you want to use framesets and still have your markup validate, you can use one of these two doctypes:

<pre>&lt;!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN"
"http://www.w3.org/TR/html4/frameset.dtd"&gt;

&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd"&gt;</pre>

They are functionally the same as HTML 4.01 transitional and XHTML 1.0 transitional respectively, but they allow the use of framesets. But please don't use framesets: they are evil and outdated. We don't even tell you how to use them anywhere in this course. Every time you use a frameset on a web page, a fairy dies. So please don't. Think of the fairies.

=== Other doctypes ===

You may also occasionally see other doctypes on your travels, but they are not mentioned here because they are outdated. Don't use any other doctypes. Not by choice, anyway.

=== Loose versus strict syntax  ===

Table 1 shows the main syntax differences between HTML and XHTML:
                          
{{{!}} border="1"
{{!}}-
!HTML 
!XHTML
{{!}}-
{{!}} Elements and attributes are case insensitive, eg <code>&lt;h1&gt;</code> is the same thing as <code>&lt;H1&gt;</code>.
{{!}} Elements and attributes are case sensitive; they are all lowercase. 
{{!}}-
{{!}} Certain elements don’t need a closing tag (eg paragraphs, <code>&lt;p&gt;</code>), while others (called “empty elements”) shouldn't have a closing tag (eg images, <code>&lt;img&gt;</code>).
{{!}} All elements must be explicitly closed (eg <code>&lt;p&gt;A paragraph&lt;/p&gt;</code>). Elements without content should be closed using a slash in the start tag (eg <code>&lt;hr&gt;&lt;/hr&gt;</code> and <code>&lt;hr/&gt;</code> mean the same thing).
{{!}}-
{{!}} Attribute values may be written without being enclosed in quotes.
{{!}} Attribute values must be enclosed by quotes.
{{!}}-
{{!}} Shorthand can be used for certain attributes (ie <code>&lt;input required&gt;</code>).
{{!}} The full attribute form must be used for all attributes (eg <code>&lt;input required="required"&gt;</code>).
{{!}}-
{{!}}}

Table 1: Differences between HTML and XHTML. (current commented out because tables won't render at the moment)

In terms of what syntax style you should use, pick something you are comfortable with. We'd recommend that you start off using strict XML syntax, as it is guaranteed to work in any situation. Later on you can adjust your style to suit, when you understand what you are doing a bit better. Just remember these rules:

* If you are using the HTML5 doctype or an HTML 4.01 doctype, you can use whatever style you want
* If you are using an XHTML doctype, you need to use XML well-formed syntax
* Whichever style you are using, best practice is to:
** Close all open elements, so for example <code>&lt;p&gt;paragraph&lt;/p&gt;</code>, not <code>&lt;p&gt;paragraph</code>
** Nest them properly, for example <code>&lt;p&gt;paragraph with bold &lt;strong&gt;word&lt;/strong&gt;&lt;/p&gt;</code>, not <code>&lt;p&gt;paragraph with bold &lt;strong&gt;word&lt;/p&gt;&lt;/strong&gt;</code>

This last rule is very important. If you don't do this, your HTML will not be well formed, and CSS and JavaScript may not work reliably, as they rely on having a well-formed Document Object Model (DOM). For more on the HTML DOM, read [http://www.w3.org/wiki/Traversing_the_DOM#Growing_trees Growing trees].

==== A note for teachers ====

A few teachers have asked us what style they should teach beginners, and what doctype they should recommend. HTML5 allows you to use loose HTML style syntax so validating against the HTML5 doctype won't pick up markup that would be considered erroneous in XHTML. this is a shame, as strict XHTML syntax is a good style to get beginners to stick to. So what should you do?

Well, the whole point of HTML5 having such loose syntax is because a lot of it really doesn't actually matter in terms of pages working ok in browsers, and HTML5 reflects more what web developers have actually done historically, rather than what the W3C thinks they should be doing. So therefore, you don't really need to stick to most of these rules; you can go forward with HTML5 using whatever syntax style you are used to. But, obviously when teaching newcomers you need to teach them a style to stick to, otherwise all kinds of chaos could ensue. We would recommend that you use the HTML5 doctype and the new elements, but get them to stick to XHTML strict rules.

The below should give you some good arguments for why:

* "HTML5 doesn't need closing tags": Yes, but you really ought to include them, to make sure an unambiguous DOM is formed, which gives you the results you were expecting when you start to apply CSS/JS to your HTML.
* "HTML5 doesn't need trailing slashes for empty tags": yes, you don't really need to include these.
* "HTML5 is case insensitive": Yes, but you should still stick to a consistent style, because it can create confusion otherwise when different students collaborate on projects, and also it could create syntax errors - eg if a student gets confused and starts using upper/lowercase in file paths. Unix servers are case sensitive. Also, your students won't always be working with HTML5 in the real world - they may come across a CMS that uses HTML4 strict, or XHTML 1.0 transitional, or whatever. Using XHTML syntax rules ensures that your HTML will work pretty much anyway, regardless of doctype and style.
* "HTML5 doesn't require <code>&lt;html&gt;</code>, <code>&lt;head&gt;</code> and <code>&lt;body&gt;</code> elements": Yes, but it is a general best practice that should be adhered to - including <code>&lt;body&gt;</code> and <code>&lt;head&gt;</code> breaks the code up naturally into two distinct areas of functionality, making it more human readable. And including the <code>&lt;html&gt;</code> tag is important for various things, such as JavaScript events, and also for accessibility - you should include a <code>lang</code> attribute to indicate the document's primary language, as a common best practice.
* "HTML5 allows stray text (not in a container)":  No. This is a bad practice - it will be likely to form an unexpected DOM - less control of your code.
* "HTML5 allows attribute values without quotes": Yes, but sometimes this will break down, eg when you have a <code>class</code> attribute containing two class names, for example <code>&lt;div class="one two"&gt;&lt;/div&gt;</code>. If you wrote <code>&lt;div class=one two&gt;</code> you may confuse the browser - it may think <code>two</code> is a new attribute.

Validation HTML5 for XHTML style syntax a bit of a pain - as a suggestion, you could use http://validator.w3.org, but set the doctype to "XHTML 1.0" instead of "detect automatically". This will take your HTML5 document and validate it as XHTML 1.0, giving you error messages as appropriate. Of course, it will also give you error messages for the HTML5 elements, because they are undefined as far as XHTML 1.0 is concerned.

=== Serving "real" XML ===

You may also be interested to know that most of the XHTML on the Web is actually HTML written with well-formed XML syntax. Even if the doctype is an XHTML one, it will be sent to the client as HTML unless you:

* save the file with an <code>.xhtml</code> file extension
* Include a line of code called the XML declaration before your doctype, which looks like this:

<pre>&lt;?xml version="1.0" encoding="UTF-8"?&gt;</pre>

We wouldn't recommend that you do this however: old versions of Internet Explorer (6 and below) switch into Quirks mode if they find the XML declaration at the start of the document, which is bad, as we looked at earlier. In addition, IE 6-8 will try to download files saved as XHTML rather than display them in the browser, which you definitely do not want!

Therefore you should just stick to not trying to serve documents as proper XHTML! Carry on people, nothing to see here.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOCTYPE, HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{API_Name}}


{{Examples_Section
|Not_required=Yes
|Examples=
}}

{{Related_Specifications_Section
|Specifications=
}}