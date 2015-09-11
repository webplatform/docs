---
title: Validating your HTML
tags:
  - Pages
  - with
  - broken
  - file
  - links
  - Tutorials
  - WSC
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - doctype
uri: 'tutorials/Validating your HTML'

---
## <span>Introduction</span>

So you’ve written a few HTML pages, and they seem to display ok to you, but there are a few things not quite right with them. What is the best way to start finding out what is wrong, and ensure that these pages (and any future pages you write) will be displayed properly across browsers, with no errors?

Validation is the answer! There are many tools available, from the W3C and other places, that allow you to validate the code on your sites. The most common three validators you’ll use are:

-   [Validator.nu](http://html5.validator.nu/): A new-school validator that validates HTML5, ARIA, SVG 1.1 and MathML 2.0: it goes through the entire document pointing out places where your markup doesn’t follow that doctype correctly (ie. where there are errors). This is the one we recommend if you are using the HTML5 doctype, like we do throughout most of this course.
-   [The W3C MarkUp Validator](http://validator.w3.org/): This looks at the (X)HTML doctype you are using for the document you give it to check, and then checks your markup accordingly. This is the one we recommend if you are using an HTML4 or XHTML1.x doctype. It does validate HTML5, but validator.nu is arguably more up to date.
-   [The W3C Link Checker](http://validator.w3.org/checklink): This looks through a document you give it to check, and tests all the links inside that document to make sure they are not broken (ie. the `<href>` values point to resources that don’t exist).
-   [The W3C CSS Validator](http://jigsaw.w3.org/css-validator/): As you’ve probably guessed, this will go through a CSS (or HTML/CSS) document and check that the CSS follows the CSS specs properly.

In this article, we will cover how to use the first two of these, showing you how to validate markup, interpreting the typical kinds of results the validator gives you. The link checker is very obvious, and we'll cover debugging CSS later on in the course.

## <span>Errors</span>

In computer programming, there are broadly speaking two kinds of problems with code:

-   syntactical errors — these are where a mistake in the writing of the code causes the computer to be unable to execute or compile the program properly.
-   programming (or logic) errors — these are where the code does not completely reflect the intent of the programmer.

With most programming languages, the first error is incredibly easy to spot — your program will just refuse to run or compile until the error is fixed. This makes finding and fixing these types of bugs much easier in those general head-scratching moments of “So why isn’t it doing what I want?”

HTML is not a programming language. Syntax errors in a web page do not commonly cause the web browser to refuse to open the page (although XHTML tends to be a lot stricter than HTML — at least when served as "[[proper XML](http://www.w3.org/wiki/Doctypes_and_markup_styles#Serving_.22real.22_XML)]"). This is one of the biggest reasons for the rapid adoption and spread of the web.

[The first web browser, WorldWideWeb](http://www.w3.org/People/Berners-Lee/WorldWideWeb.html) (written by Tim Berners-Lee) was also an editor, allowing people to create web pages without learning HTML first. This editor created invalid HTML. This could have been fixed, but it established an important precedent that exists in all web browsers to this day — that allowing people access to the content is more important than complaining about errors to people that won’t understand them or be in a position to fix them.

## <span>What is validation?</span>

Although web browsers will accept bad (*invalid* is the official term) web pages and do their best to render the code by making a best guess of the author’s intention, it is still possible to check whether the HTML has been written correctly, and indeed it is a good idea to do so, as you’ll see below. We call this “validating” the HTML.

The validation program compares the HTML code in the web page with the rules of the accompanying [doctype](/w/index.php?title=doctype&action=edit&redlink=1) and tells you if and where those rules have been broken.

## <span>Why validate?</span>

There is a common feeling amongst some web developers that if a web page looks fine in browsers, it doesn’t matter if it doesn’t validate. They describe validation as an ideal goal, but not something that is a black-and-white issue.

There is some wisdom in this attitude. The HTML4 specification is not perfect, and some things that were arguably correct — such as [starting an ordered list at a point other than 1](http://www.w3.org/wiki/HTML_lists#Beginning_ordered_lists_with_numbers_other_than_1) — were invalid HTML. HTML5 fixes quite a lot of spec issues including this one, but you may still run into situations where the validation may need to be broken. As the saying goes:

*Learn the rules so you know how to break them properly.*

There are two very powerful reasons to validate your HTML as you author it:

-   You are not always perfect, and neither is your code — we all make mistakes, and your web pages will be higher quality (ie. work more consistently) if you weed out all the mistakes.
-   Browsers change. In the future, it is likely that browsers will be less forgiving when parsing invalid code, not more forgiving.

Validation is your early-warning system about introducing bugs into your markup that can manifest in interesting and hard-to-determine ways. When a browser encounters invalid HTML, it has to take an educated guess as to what you meant to do—and different browsers can come up with different answers.

## <span>Different browsers interpret invalid HTML differently</span>

Valid HTML is the only contract you have with the browser manufacturers. The HTML specification says how you should write it, and how they should interpret your document. In recent times, standards compliance of browsers has reached the point where, as long as you write valid code, all the major browsers should interpret your code the same. This is almost always the case for HTML anyway, with other standards having a few more differences in support here and there.

But what if you pass a browser invalid code? What happens then? The answer is that the browser error handling comes into play to work out what to do with the code. It basically says “ok, this code doesn’t validate, so how do we present this page to the end user? Let's fill in the gaps like this!”

It sounds great doesn’t it? If you leave a few errors in your page, the browser will fill in the gaps for you? Not so, as each browser does things differently. For example:

    <p><strong>This text should be bold</p>
    <p>Should this text be bold? How does the HTML look when rendered?</p>

    <p><a href="#"></strong>This text should be a link</p>
    <p>Should this text be a link? How does the HTML look when rendered?</p>

The errors are that the `<strong>` element is incorrectly nested across multiple block elements, and the anchor element is not closed. When you try to render this across different browsers, they interpret the code in very different ways:

-   Opera makes the subsequent elements children of the bold element.
-   Firefox adds extra bold elements between the paragraphs, which were not present in the markup.
-   Internet Explorer puts the text “This text should be a link” outside the anchor tag that creates the link.

This original version of this example can be found in Hallvord Steen’s article [Same DOM errors, different browser interpretations](http://www.thinkvitamin.com/features/dev/same-dom-errors-different-browser-interpretations) — read this for a much deeper treatment of HTML errors, and some information about debugging tools.

None of the different browsers’ behaviours is incorrect; they’re all trying to fill in the gaps of your incorrect code. The bottom line is, *avoid invalid markup if at all possible in your page*!

Note that HTML5 fixes this, as for the first time in the history of HTML it defines how browsers should handle badly-formed markup. At the time of writing however, support for this HTML5 error handling was not widespread across browsers, so you can't yet rely on it.

## <span>How to validate your pages</span>

Now we’ve explored all the theory behind validating your HTML, we’ll talk about the easy part — the actual validation! Ok, that’s not completely accurate. Putting a URL into a validator and seeing if the page is valid or not is easy; working out what is wrong and fixing the errors is sometimes not so easy, as the error messages can sometimes be a little bit cryptic. I’ll go through some examples below.

The example we’ll be looking at in this section is as follows (you can also [download or view the HTML](http://dev.opera.com/articles/view/24-validating-your-html/example_validation.html)):

    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
    <html xmlns="http://www.w3.org/1999/xhtml" lang="en">
      <head>
        <title>Validating your HTML</title>
      </head>
      <body>
        <h2>The tale of Herbet Gruel</h2>
        <p>Welcome to my story. I am a slight whisp of a man, slender and fragile, features wrinkled and worn, eyes sunken into their sockets like rabbits cowering in their burrows. The <em>years have not been kind to me</em>, but yet I hold no regrets, as I have overcome all that sought to ail me, and have been allowed to bide my time, making mischief as I travel to and fro, 'cross the unyielding landscape of the <a href="http://outer-rim-rocks.co.uk" colspan="3">outer rim</a>.</p>

        <h3>Buster</h3>
        <p>Buster is my guardian angel. Before that, he was my dog. Before that, who knows? I lost my dog many moons ago while out hunting geese in the undergrowth. A shot rang out from my rifle, and I called for Buster to collect the goose I had felled. He ran off towards where the bird had landed, but never returned. I never found his body, but I comfort myself with the thought that he did not die; rather he transcended to a higher place, and now watches over me, to ensure my well-being.

        <h3>My possessions</h3>
        <p>A travelling man needs very little to accompany him on the road:</p>
        <ul>
          <li>My hat full of memories</li>
          <li>My trusty walking cane</li>
          <li>A purse that did contain gold at one time</li>
          <li>A diary, from the year 1874<li>
          <li>An empty glasses case</li>
          <li>A newspaper, for when I need to look busy</li>
        </ul>
      </body>

This simple page consists of three headings, three paragraphs, one hyperlink, and one unordered list. It uses the XHTML 1.0 Strict doctype as its rule set to validate against. There are a few errors in the document, which you’ll discover below using the W3C HTML validator. We used XHTML 1.0 strict because it is more likely to throw up errors than the HTML5 doctype.

### <span>The W3C HTML validator</span>

The [W3C has an online validator available](http://validator.w3.org/) — navigate to this by right/ctrl-clicking on the hyperlink you see here and selecting the “Open in new tab” option — it’ll be useful to be able to switch tabs to get between the validator and this article as you go through this example.

Note that you can also validate pages in the W3C validator from directly within the Opera browser by simply right/Ctrl-clicking and selecting the “Validate” option.

You’ll notice that the validator has three tabs available across the top of the interface:

-   Validate by URI: Allows you to enter the address of a page already on the internet for validation.
-   Validate by File Upload: Allows you to upload an HTML file for validation.
-   Validate by Direct Input: Allows you to paste the contents of an HTML file into the window for validation.

Whichever method you use should give you the same result; it’s easiest to test the example page from here by copying the full example code from above, and pasting it into the third tab along. Doing so should give you the result shown in Figure 1:

[The results of validating the sample document is 17 errors](/w/index.php?title=Special:Upload&wpDestFile=figure10.gif)

Figure 1: The results of validating the sample document — 17 errors!

This may sound worrying, especially when we tell you that there aren’t 17 errors in the document! Don’t despair — it is reporting more errors than there actually are because often an error at the top of the page will cascade, making the validator report more errors further down, as it looks like more elements are not closed or incorrectly nested. You just have to think about what the error messages mean, and look for obvious errors in the markup. Table 1 below shows all of the errors we fixed to make the page validate, along with our logic for working out what was wrong, and the fixes we applied to solve the problem.

|Error message|Logic|Fix made|
|:------------|:----|:-------|
|Line 8, Column 461: there is no attribute "colspan"|We know that there is a `colspan` attribute, and it is valid HTML, so why is it saying it doesn’t exist? Wait, maybe it means it is being used on an element that you shouldn’t use it on? Sure enough, it is being used on an `<a>` element — wrong!|Removed the `colspan` attribute from the `<a>` element.|
|Line 13, Column 7: document type does not allow element "h3" here; missing one of "object", "applet", "map", "iframe", "button", "ins", "del" start-tag . \<h3\>My possessions\</h3\>|Again, from first glance this seems strange — the `<h3>` element is properly closed, and allowed in this context. You should note that often, this error message means that there is an unclosed element nearby…|Added a closing `<p>` tag to the line above the heading in question.|
|Line 19, Column 40: document type does not allow element "li" here; missing one of "ul", "ol", "menu", "dir" start-tag. \<li\>A diary, from the year 1874\<li\>|This one is pretty easy — you can see from the line it is pointing you to, at a glance, that the end `<li>` tag has a missing closing slash (/)|Added a closing slash to the line in question.|
|Line 23, Column 9: end tag for "html" omitted, but OMITTAG NO was specified . \</body\>|Again, it doesn’t take much to work out that this means the end `<html>` tag is missing. The error message explanation even starts with You may have neglected to close an element.|Added the missing end `<html>` element.|

With these errors fixed, the validator now gives a rather satisfying success message, as shown in Figure 2:

[A success message to say that all my errors have been fixed](/w/index.php?title=Special:Upload&wpDestFile=figure20.gif)

Figure 2: A success message to say that all my errors have been fixed.

This is about all there is to it really. You just need to keep your wits about you, and remember what doctype your page is being validated against. [Download or view a fixed version of the HTML](http://dev.opera.com/articles/view/24-validating-your-html/example_validation_fixed.html)

## <span>Summary</span>

After reading this article, you should be comfortable with using the online W3C validator to validate your HTML. This really is the tip of the iceberg with regards to validation — there are more complicated tools listed below, which will help you out as your pages start to get larger and more complicated.

## <span>Further tools to check out</span>

-   [Opera Dragonfly](http://www.opera.com/dragonfly/) (built into Opera)
-   [General validation bookmarklet](https://www.squarefree.com/bookmarklets/validation.html)
-   [The Firefox web developer toolbar extension](http://chrispederick.com/work/web-developer/)
-   [The IE developer toolbar](http://www.microsoft.com/downloads/details.aspx?FamilyID=e59c3964-672d-4511-bb3e-2d5e1db91038&displaylang=en)
-   [Safari tidy](http://zappatic.net/safaritidy/)
-   [HTML tidy](http://tidy.sourceforge.net/)

## <span>Exercise questions</span>

-   What happens when a browser parses invalid HTML?
-   What is the problem with this?
-   Will using a frameset in a document validated against the HTML 4 Strict doctype generate an error?

Note: This material was originally published as part of the Opera Web Standards Curriculum, available as [24: Validating your HTML](http://dev.opera.com/articles/view/24-validating-your-html/), written by Mark Norman Francis. Like the original, it is published under the [Creative Commons Attribution, Non Commercial - Share Alike 2.5](http://creativecommons.org/licenses/by-nc-sa/2.5/) license.