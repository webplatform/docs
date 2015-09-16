---
title: 'The principles of unobtrusive JavaScript'
readiness: 'Almost Ready'
summary: 'In this article, we discuss an important concept of JavaScript — unobtrusiveness, or how to write JavaScript so that it enhances a website experience, but is not vital for it to run.'
tags:
  - Tutorials
  - JavaScript
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - QuirksMode.org
uri: 'concepts/programming/the principles of unobtrusive javascript'

---
## Summary

In this article, we discuss an important concept of JavaScript — unobtrusiveness, or how to write JavaScript so that it enhances a website experience, but is not vital for it to run.

## Introduction

In the preceding articles we’ve talked a lot about HTML and CSS and how to properly implement them, and we’ve also been through the basics of JavaScript—what it is, what it can do for you, and why you should know about it. Before we go on to look at practical JavaScript usage in detail, we need to stop and think about how to use JavaScript sensibly so that it doesn’t exclude anyone from your web site. This is the core idea behind **unobtrusive JavaScript**. To better understand what this is and why we need it, at this point in the [Web Standards Curriculum](http://www.w3.org/wiki/Web_Standards_Curriculum) let’s consider the many uncertainties involved in JavaScript programming:

-   Some browsers may ignore your script completely because they don’t support JavaScript or their support is too old-fashioned.
-   Even when a browser can support JavaScript, users may turn it off for security reasons, or their corporate firewall may block it by removing all `<script>` tags.
-   Even when a browser supports JavaScript, it may not understand parts of your script because it has a proprietary implementation of some parts of the DOM specification (IE is usually the culprit here).
-   Even when the script is interpreted correctly, it may depend on HTML that is very complicated and/or might change in unpredictable ways.
-   Even when your programming context is blessed with perfect HTML, you cannot be certain of the input device your users will use. Many scripts work only when the user uses a mouse, and forget about people who use the keyboard instead (a lot of disabled users cannot use a mouse, and some people simply prefer the keyboard).
-   Even when your script avoids all these dangers and works perfectly, other programmers may not understand it.

That’s a rather long list of problems, most of which are not technical in nature, but rather conceptual, or, if you wish, philosophical. In addition, while the last two problems may also occur in other programming languages, the first four are unique to the JavaScript progamming environment, so programming experience won’t help you there.

In short, unobtrusive JavaScript is a way of writing JavaScript so that your site visitors are not shut out of your site for one of these reasons—even if your JavaScript is not working correctly for them, they should still be able to use your site, albeit at a more basic level. This article will discuss the principles and practice of unobtrusive JavaScript, and set you up nicely for the rest of the course.

## Unobtrusive JavaScript defined

In order to effectively work around the problem listed above it’s of prime importance to understand what you're doing and why. What we need is a theory of proper JavaScript development.

Such a theory is provided by Unobtrusive JavaScript. It is not a technique as such; unobtrusive JavaScript is not a matter of adding one `makeUnobtrusive()` function to your scripts in order to enter nirvana. Instead, it’s a way of thinking. To make sure that your scripts do not inconvenience anyone, you should make sure your scripts do not make any assumptions.

Now, “not making assumptions” is a rather tall order. Fortunately we can break unobtrusiveness down into three catgeories: your script must be unobtrusive to users, browsers, and fellow programmers.

-   **Assumption: everybody’s browser supports JavaScript.** *Not true*: In order to be unobtrusive to users, taking away the script should not preclude them from using your site, even though their interaction will be far less rich than that of users whose browser does support JavaScript.
-   **Assumption: all browsers work the same.** *Not true*: In order to be unobtrusive to browsers, your script should steer clear of plain errors and compatibility problems, and take special devices such as speech browsers or mobile phones into account.
-   **Assumption: everybody else will understand my code.** *Not true*: In order to be unobtrusive to fellow programmers, your script should consist of clear, clean code and feature a lot of comments to say what your code is (supposed to be) doing.

This article will treat the first two assumptions in some detail. The third category will be treated in a separate article.

In addition to avoiding these assumptions, unobtrusive JavaScript requires you to properly separate your JavaScript code from your HTML. Since that's by far the most technical aspect of this programming philosophy, we’ll cover it first and return to our assumptions later on.

## Separation of structure and behaviour

Just as we should separate our structure and presentation by putting all CSS in a separate file and eschewing the use of `style` attributes or other such presentational markup, we should also separate our HTML structure and JavaScript behaviour. The reasons are the same: it separates your concerns, keeps your code clean, and allows you to work on the JavaScript without touching either HTML or CSS.

The basic rule is simple: an HTML file should not contain any JavaScript, just as it should not contain any CSS. There are two things JavaScript authors put in their HTML files: embedded scripts and event handlers. Removing them is the simplest way to achieve separation of structure and behaviour.

As you learned in the last article, embedded scripts are bits of JavaScript code inside an HTML page, between `<script>` tags. They can easily be moved to an external JavaScript file, so they pose no problems.

Inline event handlers, such as `<a href="somewhere.html" onmouseover="hideAll()">` are slightly harder to remove. This defines which event handlers (JavaScript functions) should run when a certain event takes place. What we have to do to make this unobtrusive is port the event handler assignment to a separate script file. That means the external script first has to find the correct element, and then assign an event handler to it.

To learn more about event handlers, check out our [Handling Events With Javascript](http://www.w3.org/community/webed/wiki/Handling_events_with_JavaScript) article.

The easiest way of allowing an element to be found is giving it an ID. For instance:

    <!-- HTML: -->
    <a href="somewhere.html" id="somewhereLink">

    <!-- JavaScript: -->
    var x = document.getElementById('somewhereLink');
    if (x) {
      x.onmouseover = hideAll;
    }

The `hideAll()` function is executed whenever the user mouses over the link, and this bit of code is thus equivalent to `<a href="somewhere.html" onmouseover="hideAll()">`.

Better still, these two lines of code work on every single page that contains an element with `id="somewhereLink"`, so that you don’t have to repeat yourself time and again. And if the page does not contain such an element, the `if (x)` check makes sure that no error messages are generated: it assigns the event handler only when element `x` in fact exists.

And what if the user’s browser doesn’t support JavaScript? Obviously, the mouseover won’t work. The link is still a link, though, and can still be followed.

Now our code, in addition to becoming cleaner, has also become more maintainable.

For instance, it’s often a good idea to pair `mouseover` events with `focus` events. A `mouseover` only works when the user uses a mouse. People who don’t use a mouse will put the keyboard focus on the link they want to click on, and that triggers a `focus` event. If we register our event-handling function on this event, too (meaning, if we tell the function that it is to be triggered by this event), we’ve made sure that our application also works with the keyboard.

This is very easy to do when the script is properly separated from the HTML:

    var x = document.getElementById('somewhereLink');
    if (x) {
      x.onmouseover = ''x.onfocus ='' hideAll;
    }

By adding 12 characters we have made this part of our application keyboard-accessible. Easy, right?

Now let’s think about what we’d have to do if we used inline event handlers. We’d have to manually go through all links on the entire site and add an `onfocus="hideAll()"` to all links that have an `onmouseover` event handler. Not only would we waste a lot of time that we could have spent on something useful, it’s also an error-prone way of working because it’s very easy to forget one link in an obscure template that’s only used in very specific situations, or simply mistype one of the `onfocus` lines.

Therefore, just as it is wise to separate your HTML and CSS, it’s an equally good idea to separate your HTML and JavaScript. Removing embedded scripts and inline event handlers is quite easy, and it immediately improves the quality and maintainability of your code.

## Adding a usability layer

Now that we’ve treated the most technical part of unobtrusive JavaScript, it’s time to return to the assumptions we discussed before. The most important one is never to assume that everybody supports JavaScript, and this ties in directly with the overall purpose of adding scripts to a web site.

The purpose of JavaScript is to add a layer of usability to your site. Note the "adding" bit: if the script *is* the entire usability layer (in other words, if the site is unusable without JavaScript), you've made a serious mistake and your script is not unobtrusive.

### Example—form validation

An example will clarify this, so let’s discuss form validation. User input in a form should *always* be checked on the server before it’s added to the database. Trusting data that any random (possibly malicious) user fills in to your forms is one of the quicker and surer ways to get your site hacked—we should always check data submissions before accepting them.

The disadvantage of server-side form validation, though, is that it may take a little while. The user submits the form to the server, and the server generates a response page that notifies the user of submission success or errors. No matter how quickly the server reacts, there will always be some small delay time between submission and message—let’s call it half a second.

Even worse, if the user has made a mistake—such as not filling in her address—she has to correct the problem and submit the form once again, leading to another half-second wait. That’s not really a lot of time, but it adds up in the user’s mind, especially if she has to go back and forth a few times.

It’s here that JavaScript enters the picture. If you add a script that checks the form before sending it off to the server, typical user errors will be caught without a round-trip to the server, and the interface will appear to work much faster and more smoothly.

So using a JavaScript form validation script is a good idea. However—and this is the point—you should use JavaScript *in addition to* server-side form validation. The former gives you a smoother interface, but only the latter gives you proper security (it is easy to get around JavaScript validation if you intend to cause mischief: you just turn JavaScript off), as well as a fallback option in case the user's browser does not support Javascript.

As of early 2009 (this may well change in the near future) Opera has an advantage over other browsers in that it supports the HTML 5 [Web Forms 2.0 specification](http://www.whatwg.org/specs/web-apps/current-work/multipage/forms.html#forms), which is basically an advanced way of doing forms in HTML, including some baked in client-side form validation features that don’t require JavaScript, and therefore can’t be worked around by turning it off. To learn more about Web Forms 2.0, check out our [Improve your forms using HTML 5](http://dev.opera.com/articles/view/improve-your-forms-using-html5/) article.

### Principles

This example highlights a few important principles:

1.  Your site should work without JavaScript.
2.  If JavaScript happens to be enabled, you can present your users with an extra layer of usability; a layer that allows them to perform their tasks more quickly, and that avoids jarring page reloads where possible.
3.  JavaScript is unsafe. That is, you should \*never\* trust in JavaScript-only routines for crucial tasks such as checking user input in a form. After all, a malicious user can just turn JavaScript off and thus bypass your defenses.

Now what, exactly, does “Your site should work without JavaScript” mean? It means that any user, whatever browsing device and software he uses, must be able to read the content of your site and use the navigation, and other critical functionality. Nothing more, but (more importantly) nothing less.

The important part is that it’s *not* necessary to offer noscript users **the same** functionality as script-enabled users. In the form validation example, noscript users must wait for half a second before they see the results of their form submission and thus get a slightly worse user experience than scripting-enabled browser users.

In fact, this is a general rule. When JavaScript is disabled, usability suffers, and your job as a web developer becomes making sure that people can use the basics of your site: content and navigation. All other features become optional.

### Example—popups

As another example, consider popup windows. Sometimes they’re genuinely useful to have, and creating them is quite easy—if a browser supports JavaScript. However, if it doesn’t, its users will not see the popup. How do you keep your site accessible while still giving JavaScript-enabled browsers a smoother interface?

    In HTML:
    <a href="somewhere.html" class="popup">Go somewhere</a>

    In JavaScript:
    var x = document.getElementsByClassName('popup'); // a custom function
    for (var i=0;i<x.length;i++=1) {
        x[i].onclick = function () {
            window.open(this.href,'popup','arguments');
            return false;
        }
    }

The crucial thing here is the `href` attribute of the link. It defines the page that should be shown in the popup, but in addition it makes sure that if JavaScript is disabled, the user can still follow the link. So this example is perfectly accessible without JavaScript—just less nice.

When JavaScript is enabled you add an extra layer of usability: the popup. You find all the links that have a `class="popup"` and add an `onclick` event handler that opens a popup. Which page should the popup show? The one defined in the link’s `href` attribute (`this.href`).

Different example, same principles. First make sure that any user can access the information; then add a bit of JavaScript on top of it to make the interface work more smoothly.

### Example—Ajax

This theory is sometimes hard to apply in practice, especially when you’re relatively new to web development and want to create, say, an Ajax site. A useful trick to get the hang of this technique is thinking in layers. What’s the basic functionality of the site? This functionality should be placed in the bottom-most layer, the one that’s accessible with or without JavaScript. On top of that, you can apply any number of JavaScript-driven usability layers that make the site easier to use. These layers do not interfere with basic site functionality; they just offer some nice extras.

An example will clarify this general rule. Suppose your site is about comparing mobile phones. The basic functionality of this site will be something along these lines:

1.  Search for certain mobile phones, either by type or by more general criteria such as “supports wifi” or “can be synchronised with my desktop computer”.
2.  Get a list of phones that match your search.
3.  Sort this list by price, name/type, or relevancy.

All these functions can be created without using one single line of JavaScript, and your first task is to do just that. So you create:

-   A search page.
-   A list page, generated by the server, based on your search.
-   Links in that list page that fetch a differently ordered list from the server.

Once you’ve made these scriptless pages you have created a basic layer that will more or less work in any browser on any device.

After you've done that, you can add JavaScript functionality to these bare-boned pages. The most obvious one is a sorting script. After all, the data necessary for the sorting—such as prices and features—is already in the table on the page, and you don’t need another round-trip to the server to get it. You just have to write a script that reads the data from the table and then sorts the `<tr>`s of that table.

Once you've written your script you should make sure that the user can actually use it. Giving the user a link for that purpose is the most obvious solution.

The important point here is that you *already have links* in the table: the links that fetch a differently ordered list from the server. By far the best solution is therefore to overrule the default behaviour of these links, just as we did in the popup example.

So you write an extra function that assigns `onclick` event handlers to these links to make sure a click on them calls your sort script instead of the page on the server.

Thus, all users see the same sort links, but their exact behaviour depends on whether their browser can handle the extra JavaScript layer of usability. If it can, it starts up your script, if it can’t, it fetches a new page from the server.

Overruling default behaviour of HTML element is a prime example of unobtrusive JavaScript. If the user’s browser supports your scripts, fine, execute them. If it doesn’t, fall back to the default behaviour of the HTML element. As long as you adhere to this principle your script will be unobtrusive.

## Clean, semantic HTML

Scripts run in the context of web pages. What kind of web pages? In theory, any page will do, as long as there are some HTML elements that you can manipulate. In practice however you’ll quickly find that standard-compliant web pages that use semantic, structured HTML and properly separate their HTML and CSS are much easier to work with than WYSIWYG-generated, table-based monstrosities.

Suppose you’re working on a news site and want every page to contain a clickable table of contents that links to all headlines in the news article. The simplest way of doing that is to scan the page for all header tags (`<h1>`, `<h2>`, etc.), create a list, and make sure that a click on the list takes the user to the appropriate header. Script done, next job. (Incidentally, this script is unobtrusive, too. The jump-to-header functionality is a nice-to-have extra, but if it’s not there the user can still read the page and use the navigation.)

Now suppose that the website you’re working on is not lucky enough to have been created with the semantic HTML and CSS that you've learned about. Suppose it looks like this:

    <div class="contentcontainer">
      <p class="maincontent"><b class="headline">McCain suspends campaign to spend more time with his economy</b><br>
      In a move that shocked political observers ... [etc etc]</p>
    </div>

Can you still write a table of contents script for such a badly marked-up page? Sure you can. Just loop through all the `<b>` tags and specify that every one of them that has a `class="headline"` is in fact a headline—and your script would work.

Nonetheless, one thing you’ve lost now is the structural nesting that is implicit in the heading levels. A clean, semantic page immediately imparts the knowledge that a `<h3>` heading will be a sub-header of the preceding `<h2>`, and your script can use that fact to its advantage.

In a non-semantic page such as the one above you’ll have to find other ways to determine whether a certain `<b class="headline">` is meant as a main header, a sub-header, a sub-sub-header or something else.

Now even *that* problem can be solved, but that’s not the point. The point is that if the HTML author uses proper header tags to mark up the headers, you are *absolutely certain* that your script will find the correct information no matter where or when it runs. Conversely, if an HTML author uses stuff like `<b class="headline">`, he doesn’t really know what he's doing, which means a later version of the HTML could easily switch to for instance \<strong\> or \<span\> tags. And every time the HTML is changed, you have to change your script, too.

Therefore scripts that work with clean, semantic pages are usually easier to write and always *far* easier to maintain that scripts that work with tag soup.

## Browser compatibility

Unobtrusive JavaScript also calls for scripts being unobtrusive to browsers. In practice this means that the script should work in as many browsers as possible, and if it doesn’t work it should’t give error messages; it should instead degrade gracefully, leaving the site visitor with a page that will still offer functionality that works. This sounds great, but it’s one of the hardest aspects of JavaScript development to master.

JavaScript guru Douglas Crockford calls the browser “the most hostile programming environment in the world.” Not only is the browser not a true application platform (yet) with a bad track record for providing things like debuggers (though there, too, things are changing for the better), but the sheer number of differences between them can quickly drive beginning JavaScripters mad.

Unfortunately browser incompatibilities are a fact of life. As soon as you try to write any non-trivial JavaScript, you’ll find out that the behaviour of the various browsers can differ significantly. Most commonly you’ll find that your script works in all browsers except for IE, though other browsers, too, have their share of problems.

The root cause of these incompatibilities is that most major browsers have their own JavaScript engine to parse, interpret and execute your scripts, and these engines differ from one another.

The most common source of problems is Internet Explorer; there are quite a few functionalities that work differently from the other browsers, or are just plain unsupported. The MSIE team is working on making its browser more standards-compliant, but it hasn’t finished that job yet. So you can expect some trouble.

Even if this problem were magically solved, plenty of incompatibilities would continue to exist, simply because a certain JavaScript engine may not yet support a certain method, or because its programmers made an honest mistake in implementing it.

So there’s a problem here, and it’s not going away any time soon. How do we cope with it?

The best strategy is acceptance and focusing on the nitty-gritty technical details, which will be treated later in this series. Learning all browser incompatibilities by heart is unfortunately impossible, but there are several aids for the starting JavaScript programmer. [QuirksMode.org](/w/index.php?title=QuirksMode.org&action=edit&redlink=1) offers compatibility tables that clearly show which methods and properties are supported by which browsers, and provides copious bug notes.

In addition, many people have traveled this road before. Some of them decided to create JavaScript libraries that work around the worst problems for you. Therefore, using a library to solve browser incompatibilities is a viable strategy.

Nonetheless, a word of caution. As a beginning JavaScripter, you should seriously consider writing your first large project without the help of libraries. The reason is that a well-rounded JavaScripter *must* work hard to gain a deep-seated understanding of what is going on under the hood. Doing so will give you a finely-honed feeling for the ways browsers can mangle your scripts, which helps your development as a JavaScript programmer.

So yes, use libraries to work around problems, but resist the urge to start using them right away. Try to work without them in order to get an idea of what you’re up against.

## Summary

Unobtrusive JavaScript is more of a programming philosophy than a technique. By far its most important component is a clear sense of which functionality belongs in which layer. All absolutely crucial site functions should be coded in plain HTML, but once you’ve created that base you can add a JavaScript layer on top of the basics in order to give browsers that support it a nicer, cleaner, faster-seeming interface.

Further, unobtrusive JavaScript

1.  separates structure and behaviour, in order to make your code cleaner and script maintenance easier
2.  pre-empts browser incompatibilities
3.  works with a clean, semantic HTML layer

Unobtrusive JavaScript is not that hard. It’s mostly a trick of the mind; once you’ve spent a few hours in planning one unobtrusive JavaScript, you’ll find that making the right decisions becomes easier and easier.

Once you’ve grown used to unobtrusive JavaScript, you won’t want to go back to the old obtrusive model.
