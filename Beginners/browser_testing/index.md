---
title: 'Part 9: Browser testing'
notes:
  - 'Give more examples on ways to test in browser, not only automated commercial tools, but maybe talk about linting, etc.'
readiness: 'Almost Ready'
summary: 'To learn how web browsers react, it is quite useful to have automated tools. But modern browsers are now doing a very good job at behaving the same. Unless you are digging right away with technologies that are still in early adoption, you do not need browser testing tools.'
tags:
  - Basic_Pages
uri: 'Beginners/browser testing'

---
## Summary

To learn how web browsers react, it is quite useful to have automated tools. But modern browsers are now doing a very good job at behaving the same. Unless you are digging right away with technologies that are still in early adoption, you do not need browser testing tools.

## Beginners submenu

The **[Beginners](/Beginners)** section covers the various aspects of web development separated in 9 parts, you can navigate through them using this list.

-   [1. The beginning](/Beginners/the_beginning)
-   [2. A crash course in web site code](/Beginners/crash_course)
-   [3. Planning](/Beginners/planning)
-   [4. Structuring our content with HTML](/Beginners/html)
-   [5. Styling our content with CSS](/Beginners/css)
-   [6. Programming fundamentals](/Beginners/programming)
-   [7. JavaScript](/Beginners/javascript)
-   [8. Advanced topics](/Beginners/advanced)
-   **9. Browser testing**
-   [Glossary](/Beginners/glossary)

## Tools

There are many ways to test your web pages. It can be by installing multiple web browsers, have a set of computers and devices, maintain a set of Virtual Machines with the various versions you want to support or even use a service provider that will take snapshots for you.

If you are just starting, a web browser is more than enough.

**Also**: It is known and accepted that "[Websites do not *need* to look exactly the same in every browser](http://dowebsitesneedtolookexactlythesameineverybrowser.com/)". The previous link is a good example of the idea —try it in an old browser to see. There are many techniques possible to have older browsers to support features by detecting if they exist (called "feature sniffing" with [Modernizr](http://modernizr.com) for example), and conditionally add a library that will add support (we call them "Polyfils" or "shims"). The essential to remember here is that web technology changes quickly and we cannot expect old web browsers to support more recent features. Its as if we would ask a black and white television to be in color. But all that is beyond the scope of testing your site!

### In a Virtual Machine

If you want to test various versions of old web browsers but you do not see how you can have more than one version of a given web browser, you should consider using Virtual Machines ("VMs").

A VM is like a big file that you can load inside a software as if it was a computer. In fact, that software is emulating hardware and acts as if it was a separate physical machine. We call this "Virtualization". It therefore runs a computer *inside* another computer. People creating software and services "in the cloud" are heavily relying on similar technologies.

For example, if you have only a recent computer and you want to see how it will look like in Internet Explorer provided in Windows Vista, you can have a VM that runs Vista and Internet Explorer 7 along with Mozilla Firefox 3.

For this, you can get what we call a "Desktop Virtualization" software, there are a few on the market. Oracle [VirtualBox](https://www.virtualbox.org/) and VMWare both have free versions that can make anybody run VMs.

Once you have a Virtualization software, you will need to use or create your own VMs. While creating a VM is outside of the scope of this article, you can download from Microsoft —for free— one of their testing VMs. Take a look at [modern.ie](http://modern.ie).

With this in hand, you can test on various versions of the web browsers you want to support, without cluttering your own computer.

'*About Modern.ie VMs*: Note that those VMs are made only to test and cannot be used as a main work environment. The VM will eventually ask you delete the VM (e.g. after 30 days). A trick that you can do is to keep a copy of the downloaded archive and extract it again.

### Mobile devices

Doing serious mobile testing requires a serious mobile test lab. Here is some guidance for setting it up.

Below is a long list of devices you need. Although it would be wonderful if you could just buy them all at once, most web developers are not in that position. The guidelines that are about to follow are mostly for them.

Save about 100 euros (or dollars) per month for devices. Once you have saved enough, buy one. This will allow you to buy two high-end phones per year, or maybe four or five mid-range ones. Of course, the more money you allocate, the better.

You likely already have a personal iPhone or Android. The first phone to buy is the other one: an Android if you use an iPhone, an iPhone if you use an Android.

The second phone will be another Android. Make sure you buy one from a different vendor, running a different Android version, with a different screen size. The most important feature of Android is its differentiation, and your device lab should reflect that.

Postpone buying a Google device. Although they're very popular among web developers, actual consumers don't buy all that many. Instead, they buy from the established vendors such as Samsung and HTC. Thus, adding a Google device doesn't tell you all that much about how users are going to view your site.

Most likely, your third and fourth phone will also be Androids. Now it's time to pick up an older or cheaper one. Plenty of people use these phones, so you should be able to test your site in adverse conditions.

Then it's time for something completely different: a Windows Phone, or, especially if you're in the UK, a BlackBerry. Maybe it's also time to pick up a Nokia Asha, a Firefox OS, or something even more obscure.

Then consider a second iPhone, with a different screen size than your first one, and a few more Androids.

Devices you need:

-   iPhone, both an older (say 4S) and a newer one
-   A Windows Phone, most likely a Nokia, with Windows 8.1 and IE11
-   A BlackBerry 10 phone
-   Possibly a Nokia Asha (S40) and/or a Firefox OS device
-   Lots and lots of Androids

Androids you need:

-   At least two Samsungs: an older and a newer one; say an Android 4.1 or 4.2 and one on the latest version. You need the older one because Samsung switched browsers around Android 4.2 or 4.3
-   An HTC, Sony, LG, Huawei, Motorola, Xiaomi, or another vendor.
-   A Google Nexus device (maybe a tablet if most of your other devices are phones). Don't give this one priority, though.

### Automated browser testing

As for automated browser testing, its is only useful if you work on bigger projects and goes beyond the scope of this section.

There are a few automated browser testing services. They do not require you to install anything and they give you screenshots of the pages you are providing them on various browser versions, including the mobile ones.

Here is a list of browser testing:

-   [BrowserStack](http://www.browserstack.com/) (commercial)
-   [Browsershots](http://browsershots.org/) (Screenshots only)
-   [CrossBrowserTesting](http://crossbrowsertesting.com/) (commercial)
-   [SauceLabs](https://saucelabs.com/) (free and commercial plans).

For more information, check those [articles on cross-browser debugging](/concepts/cross_browser_techniques).

