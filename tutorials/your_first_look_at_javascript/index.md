---
title: Your first look at JavaScript
readiness: 'Ready to Use'
summary: 'Now it is time to get your hands dirty. This article provides a basic introduction to coding with JavaScript.'
tags:
  - Tutorials
  - JavaScript
  - WSC
uri: 'tutorials/your first look at javascript'

---
## Summary

Now it is time to get your hands dirty. This article provides a basic introduction to coding with JavaScript.

## Introduction

In this article of the [Web Standards Curriculum](http://www.w3.org/wiki/Web_Standards_Curriculum), we will cover the basics of JavaScript — how and where to use it, what problems to avoid, and general basics to get you started on your journey towards becoming a top-notch JavaScript developer.

## What is JavaScript and how do you execute it?

JavaScript is a text-based language that does not need any conversion before being executed. Other languages like [Java and C++ need to be compiled to be executable](http://dev.opera.com/articles/view/38-programming-the-real-basics/#interpreted) but JavaScript is executed instantly by a type of program that interprets the code called a parser (pretty much all web browsers contain a JavaScript parser).

To execute JavaScript in a browser you have two options — either put it inside a `script` element anywhere inside an HTML document, or put it inside an external JavaScript file (with a .js extension) and then reference that file inside the HTML document using an empty `script` element with a `src` attribute. We will look at both of these methods inside this section.

JavaScript does not have to stay inside browsers. To run JavaScript in console environment, please check out [Mozilla Rhino](https://developer.mozilla.org/en-US/docs/Rhino/Download_Rhino); to run JavaScript in server environment, please check [node.js](http://nodejs.org/).

### Including your JavaScript inside your HTML document

The most basic inclusion of JavaScript inside your HTML page would look something like this:

``` html
<script>
  var x = 3;
  alert('hello there, I am JavaScript - x is ' + x);
</script>
```

 You could put this anywhere inside your document and it would execute, but some places are definitely better than others — see the [Where to put JavaScript](http://www.w3.org/wiki/Your_first_look_at_JavaScript#Where_to_put_JavaScript) section for guidance on this.

As there might be several different types of script available to use on web pages in the future, it makes sense to add the name of the script you are using as a MIME type:

``` html
<script type="text/javascript">
  var x = 3;
  alert('hello there, I am JavaScript - x is ' + x);
</script>
```

**Note:** You will find script examples on the web that have a `language="javascript"` attribute. This is not part of any standard and is utterly useless; delete this where you can. This is a throwback to the bad old days, when VBScript was also in popular use on web pages. VBScript usage died however, as it only works in IE.

In the past there was a need to comment out JavaScript with an HTML comment to prevent browsers from showing the code as HTML. As this only applies to very old browsers you do not need to bother with that any longer. However, if you are using strict XHTML as your DOCTYPE, you need to enclose any JavaScript in a CDATA block to make it validate (do not worry about why - it is not really important at this stage in your learning):

``` html
<script type="text/javascript">
/* <![CDATA[ */
  var x = 3;
  alert('hello there, I am JavaScript - x is ' + x);
/* ]]> */
</script>
```

 However, for strict XHTML documents, it is much more sensible not to embed any JavaScript but instead keep it in an external document.

### Linking to an external JavaScript file

In order to link to an external JavaScript (either on the same server or anywhere on the internet) all you have to do is to add a `src` attribute to your script element:

``` html
<script type="text/javascript" src="myscript.js"></script>
```

 Upon meeting this element in a page, browsers will then load the file `myscript.js` and execute it. Any content inside the `script` element itself will be skipped when you provide a `src` attribute. The following example will load the file `myscript.js` and execute the code in it, but will not execute the alert inside the `script` element at all.

``` html
<script type="text/javascript" src="myscript.js">
  alert('I am pointless as I will not be executed');
</script>
```

 Keeping your code in an external JavaScript file makes a lot of sense:

-   You can apply the same JavaScript functionality to several HTML documents and still keep maintenance easy: if there is a desired change in functionality all you need to do is change one single file.
-   Your JavaScript will be cached by browsers. Caching means that browsers will take a copy of your JavaScript and store it on the computer of the visitors surfing on your site. The next time this user loads the same script it will not be taken from your server but from their own computers — thus loading much faster.
-   You can easily find your script if you need to modify it, avoiding the need to scan through long HTML documents to find the place to fix a problem.
-   Fixing errors becomes easier as a debugging tool or error console will tell you which file contains the error and reliably report the line number.

You can add as many JavaScript files as you want to a document, but there are several considerations to make before going down that route.

## JavaScript and browser performance

Cutting up a lot of JavaScript into different files, each dealing with one task at a time, is a great idea to keep your functionality easy to maintain and allow for quick bug-fixing. For example, you could have several script blocks like these:

``` html
<script type="text/javascript" src="config.js"></script>
<script type="text/javascript" src="base.js"></script>
<script type="text/javascript" src="effects.js"></script>
<script type="text/javascript" src="validation.js"></script>
<script type="text/javascript" src="widgets.js"></script>
```

 However, the development benefits of this are diminished by the effect this has on the performance of your document. This differs slightly from browser to browser but the worst-case scenario (which is sadly enough still the second most-used browser) does the following:

-   Every time the browser encounters a `script` element, it will pause rendering (displaying) the document.
-   It will then load the JavaScript file defined in the `src` attribute (if you use a script on another server you also have to wait until the browser finds that server).
-   It then will execute the script before it goes on to accessing the next one.

All of this means that the display of your web site is slowed down until all of these steps happen for all the scripts you include. This can become annoying for your visitors.

One way around this is to use a backend script to create a single file from all the files you use. That way you have the benefit of keeping maintenance easy while simultaneously cutting down on delays to your web page display. There are several scripts like this on the web — one of them is written in PHP and [available from Ed Eliot](http://www.ejeliot.com/blog/73).

The delay in display also defines where you want to put your JavaScript in the document.

## Where to put JavaScript

Technically you can put JavaScript anywhere in your document. The decision you have to make is to weigh performance against making it easy for developers to find your scripts and ensuring that your JavaScript enhancements work immediately for your visitors.

The classic best practice for placing scripts was in the `head` of the document:

``` html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
    <script src="myscripts.js"></script>
  </head>
  <body>
    <!-- lots of HTML here -->
  </body>
</html>
```

This has the benefit of being a predictable location of scripts — developers know where to find them. It also has the benefit of ensuring that all JavaScript has been loaded and executed before the document is displayed.

The drawbacks are that your scripts delay the display of the document and that the script does not have access to the HTML in the document. You therefore need to delay the execution of any scripts that change the HTML of the document until the document has finished loading. This can be done with an [onload handler](http://www.onlinetools.org/articles/unobtrusivejavascript/chapter4.html) or one of the various [DOMready](http://dean.edwards.name/weblog/category/dom/onload/) or [contentAvailable](http://developer.yahoo.com/yui/examples/event/event-timing.html) solutions out there on the web — none of which are bullet-proof and most of which rely on browser-specific hacks.

Performance specialists have started to advocate placing your JavaScript at the end of the `body` instead:

``` html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <!-- lots of HTML here -->
    <script src="myscripts.js"></script>
  </body>
</html>
```

 This benefits your JavaScript by not delaying the display of the HTML and also means that any HTML you want to alter with JavaScript is already available.

You might confuse developers who maintain your code because this practice is not common yet. Another — more problematic — drawback is that the HTML becomes available before your JavaScript is loaded. While this is exactly what you want to achieve, it also means that visitors will start interacting with your interface before you get the chance to change it. Say for example you want to validate a form with JavaScript before it is submitted to the server — the form might get submitted before the script has been loaded. If you write your script as a mere enhancement (rather than relying on it) that is not a problem though — just an annoyance.

It is up to you to choose what fits the purpose of your website; you could even choose to do a mixture of both — put the scripts with very important functionality in the `head`, and call them in conjunction with the “nice-to-have” scripts at the end of the document.

``` html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
    <script src="myimportantscripts.js"></script>
  </head>
  <body>
    <!-- lots of HTML here -->
    <script src="myscripts.js"></script>
  </body>
</html>
```

 Whatever you do, make sure that the order of your scripts is right, as browsers will load and parse them one after the other. This also brings us to another thing to consider when using JavaScript.

## JavaScript security and the lack thereof

We cannot stress this enough. JavaScript is a wonderful language and can help you to build highly responsive and beautifully interactive web sites and applications, but where it falls down terribly is security. In short, there is no security model in JavaScript and you should not protect, encrypt, secure, or store anything vital or secret with it.

Every script on the page has the same rights — all of them can access each other, read out variables, access functions, and also override each other. If you have a function called `init()` in your first included script, and another one in your last included script, the original one will be overridden. We will come back to this problem in the [best practices article](http://dev.opera.com/articles/view/javascript-best-practices/) of this course.

All of this would not be much of an issue if you never used other people’s scripts. However, seeing that most online advertising and statistics-tracking is done with JavaScript this will not be the case — you will use third party scripts all the time.

Scripts can also read cookies; using the `prototype` of a function you can override any native JavaScript function. Lastly, JavaScript can easily be turned off so you can forget about JavaScript protection being a good security measure.

JavaScript is always readily available for reading and analyzing by other developers. Of course you can pack (remove all unnecessary whitespace) and obfuscate (use random variable and function names) your scripts, but even those can be reverse-engineered; in this case the only person you stop from using your code easily is yourself. The availability of the source code and the ability to read and analyze it is possibility the main factor for the success of JavaScript - for years we learned by peeking at other people’s solutions. Nowadays this is luckily over as there are good books and tutorials available.

Whereas packing and obfuscation are useless as security measures, they are often done on medium and large scripts before the code is put live on the web as part of the publication process. This helps to cut down on the amount of bandwidth required to serve the site to its users. Saving a few bytes here and there may not seem significant on your blog about kittens, but it can add up to massive savings when you are dealing with a site with usage figures like those of google.com.

## Techniques to avoid

The biggest problem with learning JavaScript is that there is a massive amount of outdated and possibly dangerous information out there. This is especially frustrating as a lot of this information is very well presented and gives a lot of beginners a “quick win” feeling of knowing JavaScript by copying and pasting some ready-made code.

As the environment JavaScript is being applied to is very much unknown (users can have any setup) and we do not know what decisions led to code we find on the web being created in a particular way, we should not point fingers at solutions. However, the following ideas are a thing of the past and you should only use them as a very last resort if you need them to support really old, bad browsers:

-   `document.write()` — you can write out content to the document using `document.write()` but there are several issues with this: you mix HTML and scripting and you need to add a script node exactly where you want the content to appear, which slows down your page. It is a very cool way of easily showing (for example in a tutorial or when testing/debugging your code) what the result of some piece of code is, but it is a bad example to show people, as you should never have to use it in live code.
-   `<noscript></noscript>` — as its name implies, the `noscript` element is the opposite to the `script` element. The content inside it will be shown to users that have JavaScript disabled. The main reason to use `noscript` is to provide alternative content for users who do not have JavaScript available in their browser. Users that have no JavaScript don't do that to make your life harder — they might do it because of a security policy, or because the browser they are using does not support JavaScript. But what you can provide inside `noscript` is limited, and you should not use it. Provide a note instead, telling users to enable JavaScript in their browser — for some users this is not possible.
-   `<a href="javascript:doStuff()">…</a>` — this was a very common way to invoke JavaScript functionality, most of the time when a button was not an option (you cannot style buttons in older browsers). The problem is that this is not a valid link as `javascript` is not an internet protocol (like `ftp://` or `http://`). If JavaScript is turned off the link still appears and gives the user false hope that something is going to happen.
-   `document.layers` and `document.all` — both of these solutions were the DOM equivalents in old browsers (Netscape 4.x and Internet Explorer 4 respectively) and unless you need to support those (sorry if you have to) this is unnecessary code.

## See also

### Exercise Questions

-   What does the following link do and what problems can that cause?

``` html
<a href="javascript: open('tac.pdf')">Read our Terms and Conditions</a>
```

-   Providing parameters for scripts is a powerful way of making them reusable. It is very important to keep the option to provide compact and easy to use parameters. What are the downsides of the following solution (which provides parameters that are compact and easy to use)?

``` html
<script src="badge.js"> var color = 'blue'; var background = 'yellow'; var width = 400; </script>
```

-   What is the issue with so called “global variables”, and how can they be avoided?
-   Where in the document would you put a large script that is nice to have but not vital to the functionality of the site? Why?
-   What is the problem with executing scripts like this:

``` html
<body onload="init()">
```
