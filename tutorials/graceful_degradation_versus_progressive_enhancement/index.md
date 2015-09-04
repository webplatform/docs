---
title: graceful degradation versus progressive enhancement
tags:
  - Tutorials
  - JavaScript
readiness: 'Ready to Use'
summary: 'This article discusses the important concepts of graceful degradation and progressive enhancement, and how they relate to JavaScript.'
uri: 'tutorials/graceful degradation versus progressive enhancement'

---
# Graceful degradation vs. progressive enhancement

## Summary

This article discusses the important concepts of graceful degradation and progressive enhancement, and how they relate to JavaScript.

## Introduction

In this part of the [Web Standards Curriculum](http://www.w3.org/wiki/Web_Standards_Curriculum) we discuss the difference between two development approaches: graceful degradation and progressive enhancement. Putting things simply, here are working definitions:

Graceful degradation
:   Providing an alternative version of your functionality or making the user aware of shortcomings of a product as a safety measure to ensure that the product is usable.
Progressive enhancement
:   Starting with a baseline of usable functionality, then increasing the richness of the user experience step by step by testing for support for enhancements before applying them.

You may think that these two approaches sound very similar, and that they should give you pretty much the same result, but there are differences to take note of, which we’ll look at below.

We’ll start by explaining the need for these techniques. Then we’ll look at a deeper definition, showing implementation examples and following up with a comparison and a guide to when you should use which. Let’s start by explaining why we need such special development approaches to web development.

## “Mobilis in mobile” — moving in a constantly changing environment

Just like Captain Nemo from “20,000 Leagues under the Sea”, web developers find themselves in a constantly changing and fluctuating environment that can be pretty hostile to what we try to achieve.

The web was invented and defined to be used with any display device, in any language, anywhere you want. The only thing expected of end users is that they are using a browsing device that can reach out to the web and understand the protocols used to transmit information — http, https, ftp and so on.

This means that we can’t expect anything of the setup or ability of our end users. We can also be fairly sure that our experience of the web as developers is totally different to the one of the people we want to reach.

There is no mandatory upgrade of technologies to reach content on the internet. People and companies will stick to a defined environment and not change or upgrade just because we want them to. A lot of people only want to consume the web and are oblivious to the technologies behind it — all they expect is to be able to reach the content we promise them. It is up to operating system and browser developers to make end users keep their system up-to-date — as web developers we don’t have any say in this.

All of this makes for a very fragile development environment, for example offices where the default is a 9-year old browser with scripting and plugins disabled (because of security reasons), low resolutions and computers that are barely managing the load of running office software are pretty common.

We could now go and claim that companies like these have “missed the boat” and there is no sense in trying to support outdated technology. But this attitude can cause us to forget that these people might be very important to the success of our products. In many cases they don’t have the necessary rights to change their technical setup. When it comes to accessibility things are even more obvious: a dyslexic end user cannot understand our convoluted instructions and a blind user can’t “click the green button to continue”, even though we’ve decreed that it is needed to use our systems.

We work in the unknown and we need to find a way to make it work. This is where both graceful degradation and progressive enhancement come into play.

## Graceful degradation and progressive enhancement in a nutshell

You’ve already seen a simple definition above; in this section I will provide a more technical definition, and look at what it really means to implement these methodologies.

So, **graceful degradation** is the practice of building your web functionality so that it provides a certain level of user experience in more modern browsers, but it will also *degrade gracefully* to a lower level of user in experience in older browsers. This lower level is not as nice to use for your site visitors, but it does still provide them with the basic functionality that they came to your site to use; things do not break for them.

**Progressive enhancement** is similar, but it does things the other way round. You start by establishing a basic level of user experience that all browsers will be able to provide when rendering your web site, but you also build in more advanced functionality that will automatically be available to browsers that can use it.

In other words, graceful degradation starts from the status quo of complexity and tries to fix for the lesser experience whereas progressive enhancement starts from a very basic, working example and allows for constant extension for future environments. Degrading gracefully means looking back whereas enhancing progressively means looking forward whilst keeping your feet on firm ground.

## An example of graceful degradation versus progressive enhancement

Let’s take a look at an example showing one approach that uses progressive enhancement and another one using graceful degradation.

### “Print this page” links

Arguably links that allow users to print the current document are useless — hitting the printer icon in their browser does the same thing. User testing however shows that as a last step in a booking process (eg on an airline web site) they are a good re-affirming call to action. Users feel in control and get the sense of finishing what they started.

The issue with “print this page” links is that there is no way to link to the print button of the browser in HTML — you need JavaScript to do that. In JavaScript it is easy — the `window` object of the browser has a `print()` method that can be called to start a printout. Probably the most common way of doing that is by using the `javascript:` pseudo protocol:

    <p id="printthis">
      <a href="javascript:window.print()">Print this page</a>
    </p>

This works when JavaScript is available and enabled, and the browser supports the `print` command. However, if JavaScript is not available (for example on some mobile devices) then this link will not work — clicking on it will do nothing at all. This creates an issue because, as the site developer, you promise your visitors this functionality. When they click the link and it doesn’t work they’ll feel confused and cheated and will rightfully blame you for delivering a bad user experience.

In order to make this less of a problem site developers normally go for the **graceful degradation** approach: tell the user that the link may not be working and what the reason for that is, and maybe even suggest an alternative solution to achieve what they want to do. A common trick is to use the `noscript` element. Anything inside this element will be shown to the end user when JavaScript is not available. In our case this could be the following:

    <p id="printthis">
      <a href="javascript:window.print()">Print this page</a>
    </p>
    <noscript>
      <p class="scriptwarning">
        Printing the page requires JavaScript to be enabled.
        Please turn it on in your browser.
      </p>
    </noscript>

This is considered degrading gracefully — we explain to the user that something is wrong and how to work around the issue. However, this assumes that visitors to your site:

-   Know what JavaScript is
-   Know how to enable it
-   Have the rights and the option to enable it
-   Feel happy about turning on JavaScript just to print a document

A slightly better approach would be to do this perhaps:

    <p id="printthis">
      <a href="javascript:window.print()">Print this page</a>
    </p>
    <noscript>
      <p class="scriptwarning">
        Print a copy of your confirmation.
        Select the "Print" icon in your browser,
        or select "Print" from the "File" menu.
      </p>
    </noscript>

This gets rid of some of the issues detailed above, but it does assume that browser print functionality is identical in all browsers. Plus the fact remains — the issue with this type of approach is that we offer some functionality fully knowing that it might not work, and then have to explain ourselves. Technically there is no need for the “print this” button, which is why a progressively enhanced approach to the same problem doesn’t assume that it’ll work.

If we were to solve this problem using **progressive enhancement**, the first step would be to find out if there is a non-scripting way of printing the page. There isn’t, which actually means that a link is the wrong choice of HTML element to use. If you want to provide functionality that is only available with JavaScript you should use buttons: by definition [buttons are there to support scripting functionality](http://www.w3.org/TR/html401/interact/forms.html#push-button). As the W3C spec says:

> push buttons: Push buttons have no default behavior. Each push button may have client-side scripts associated with the element's event attributes. When an event occurs (e.g., the user presses the button, releases it, etc.), the associated script is triggered.

The second step is to not assume that the user has JavaScript enabled and that the browser can print. Instead we just tell the user flat out that they need to print the document and leave the “how” up to them:

    <p id="printthis">Thank you for your order. Please print this page for your records.</p>

This works in any case. For the rest of the functionality we use [unobtrusive JavaScript](http://www.w3.org/wiki/The_principles_of_unobtrusive_JavaScript) to add a print button only when the browser supports it:

    <p id="printthis">Thank you for your order. Please print this page for your records.</p>
    <script type="text/javascript">
    (function(){
      if(document.getElementById){
        var pt = document.getElementById('printthis');
        if(pt && typeof window.print === 'function'){
          var but = document.createElement('input');
          but.setAttribute('type','button');
          but.setAttribute('value','Print this now');
          but.onclick = function(){
            window.print();
          };
          pt.appendChild(but);
        }
      }
    })();
    </script>

Notice how defensive the script is — we don’t assume anything.

-   By wrapping the whole functionality in an anonymous function and immediately executing it — this is what `(function(){})()` does — we don’t leave any global variables behind.
-   We test for DOM support and try to get the element we want to add the button to.
-   We then test if the element exists and if the browser has a `window` object and a `print` method (by testing if the `type` of this property is `function`).
-   If both are true, we create a new click button and apply `window.print()` as the click event handler.
-   The last step is to add the button to the paragraph.

This will work for every user regardless of technical environment. We never promise the user an interface element that doesn’t work — instead we only show it when it does work.

## When to use what

I might be an idealist but I really dislike the idea of graceful degradation. By building something and then making it barely work in other environments (or asking users to upgrade) I make a lot of assumptions about both the environment and the ability of the users to upgrade.

I find myself using a Blackberry when this laptop cannot find a wireless network and get very frustrated when web products tell me they need JavaScript enabled and I should turn it on. I can’t, and surely I’m an eligible user of your products — especially when I pay a lot of money for GPRS or EDGE access to your services.

However, **graceful degradation** becomes viable in a few situations:

-   You retrofit an old product and you don’t have the time, access or insight to change or replace it.
-   You just don’t have time to finish a product with full progressive enhancement (often a sign of bad planning or running out of budget).
-   The product you have is an edge case, for example very high traffic sites where every millisecond of performance means a difference of millions of dollars.
-   Your product by definition is so dependent on scripting that it makes more sense to maintain a “basic” version rather than enhancing one (Maps, email clients, feed readers).

In all other cases, **progressive enhancement** will make both the end users and you happier:

-   Regardless of environment and ability you deliver a product that works.
-   When a new browser comes out or a browser extension becomes widely adopted you can enhance to yet another level without having to touch the original solution — graceful degradation would require you to alter the original solution.
-   You allow technology to be what it is supposed to be — an aid to reach a goal faster than without it, not a “must” to be able to reach a goal in the first place.
-   If you need to add new features, you can do so after checking if they are supported at a certain stage, or you can add it to the most basic level of functionality and make it better in more sophisticated environments. In any case, the maintenance happens at the same spot and not in two different places. Keeping a progressively enhanced product up-to-date is much less work than maintaining two versions.

## See also

### Exercise Questions

-   The article showed print links as an example that could use either approach. What other examples can you think of?
-   Say you want to use JavaScript to make sure that a form field contains an email address before the form is submitted. What would be the different approaches and what other problems should be taken into consideration?
-   Say you want to display a map and you want to use progressive enhancement. What would be the base functionality you would start from?
-   Say you have an interface that consists of two dropdown form controls. Selecting an option in the first will change the available options in the second one. What could be a fallback for this kind of control? What issues could there be with it?

