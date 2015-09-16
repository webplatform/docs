---
title: 'The history of the Web'
tags:
  - Tutorials
  - WSC
uri: 'tutorials/The history of the Web'

---
## Introduction

> Where shall I begin, please your Majesty?
>
> Begin at the beginning, the King said gravely, and go on till you come to the end: then stop.
>
> *Alice’s Adventures in Wonderland; Lewis Caroll*

Everything has to begin somewhere, so lets start with a focused history lesson. Below we'll give you a brief overview of the creation of the Internet, the World Wide Web, and the web standards that this entire series focuses upon.

If any terms are unfamiliar to you, don’t worry: if they’re important for learning web development they’ll be defined in the later articles that go into more depth on each subject, and you can always search them out using your search engine of choice! If you are already familiar with the history of the Internet or the World Wide Web, feel free to skip to the section on [[web standards](http://www.w3.org/wiki/The_history_of_the_Web#The_coming_of_web_standards)].

## The Internet’s origins

On the fourth of October in 1957 an event occurred that would change the world. The Soviet Union successfully launched the first satellite into Earth’s orbit. Called Sputnik 1, it shocked the world — especially the United States of America, who had their own programme of satellite launches underway, but had yet to launch.

This event lead directly to the creation of the US Department of Defence, ARPA, due to a recognised need for an organisation that could research and develop advanced ideas and technology. Perhaps their most famous project (certainly the most widely used) was the creation of the Internet.

In 1960, psychologist and computer scientist Joseph Licklider published a paper entitled Man-Computer Symbiosis, which articulated the idea of networked computers providing advanced information storage and retrieval. In 1962, whilst working for ARPA as the head of the information processing office, he formed a group to further computer research, but left the group before any actual work was done on the idea.

The plan for this computer network (to be called [ARPANET](http://en.wikipedia.org/wiki/ARPANET)) was presented in October 1967, and in December 1969 the first four-computer network was up and running. The core problem in creating a network was how to connect separate physical networks without tying up network resources for constant links. The technique that solved this problem is known as packet switching and it involves data requests being split into small chunks (packets,) which can be processed quickly without blocking communication from other parties — this principle is still used to run the Internet today.

This concept received wider adoption, with several other networks springing up using the same packet switching technique — for example, X.25 (developed by the International Telecommunication Union) formed the basis of the first UK university network JANET (allowing UK universities to send and receive files and emails) and the American public network CompuServe (a commercial enterprise allowing small companies and individuals access to time-shared computer resources, and then later Internet access.) These networks, despite having many connections, were more like private networks than the Internet of today.

This proliferation of different networking protocols soon became a problem, when trying to get all the separate networks to communicate. There was a solution in sight however—Robert Kahn, whilst working on a satellite packet network project for ARPA, started defining some rules for a more open networking architecture to replace the current protocol used in ARPANET. Later joined by Vinton Cerf from Stanford University, the two created a system that masked the differences between networking protocols using a new standard. In the publication of the draft specification in December 1974, this was called the Internet Transmission Control Program.

This specification reduced the role of the network and moved the responsibility of maintaining transmission integrity to the host computer. The result was that it became possible to easily join almost all networks together. ARPA funded development of the software, and in 1977 a successful demonstration of three different networks communicating was conducted. By 1981, the specification was finalised, published and adopted; and in 1982 the ARPANET connections outside of the US were converted to use the new TCP/IP protocol. The Internet as we know it had arrived.

## The creation of World Wide Web

[Gopher](http://en.wikipedia.org/wiki/Gopher) was an information retrieval system used in the early 1990s, providing a method of delivering menus of links to files, computer resources and other menus. These menus could cross the boundaries of the current computer and use the Internet to fetch menus from other systems. It was very popular with universities looking to provide campus-wide information and large organisations looking to centralise document storage and management.

Gopher was created by the University of Minnesota. In February, 1993, they announced that it was going to charge licensing fees for the use of their reference implementation of the Gopher server. As a consequence, many organisations started to look for alternatives to Gopher.

The European Council for Nuclear Research (CERN) in Switzerland had such an alternative. Tim Berners-Lee had been working on a information management system, in which text could contain links and references to other works, allowing the reader to quickly jump from document to document. He had created a server for publishing this style of document (called hypertext) as well as a program for reading them, which he had called WorldWideWeb. This software had first been released in 1991, however, it took two events to cause an explosion in popularity and the eventual replacement of Gopher.

On the thirtieth of April 1993 CERN released the source code of WorldWideWeb into the public domain, so anyone could use or build upon the software without charge.

Then, later in the same year, the NCSA released a program that was a combined web browser and Gopher client, called Mosaic. This was originally only available on Unix machines and in source code form, but in December 1993 Mosaic provided a new version with installers for both Apple Macintosh and Microsoft Windows. Mosaic rapidly increased in popularity, and with it the Web.

The number of available web browsers increased dramatically, many created by research projects at universities and corporations, such as Telenor (a Norwegian communications company), which created the first version of the Opera browser in 1994.

### The browser wars

The popularisation of the web brought commercial interests. Marc Andreessen left NCSA and together with Jim Clark founded Mosaic Communications, later renamed to Netscape Communications Corporation, and started work on what was to become Netscape Navigator. Version 1.0 of the software was released in December 1994.

Spyglass Inc. (the commercial arm of NCSA) licensed their Mosaic technology to Microsoft to form the basis of Internet Explorer. Version 1.0 was released in August 1995.

A rapid escalation soon followed, with Netscape and Microsoft each trying to get a competitive edge in terms of the features they support in order to attract developers. This has since become known as the browser wars. Opera maintained a small but steady presence throughout this period, and tried to innovate and support web standards as well as possible in these times.

## The coming of web standards

During the browser wars, Microsoft and Netscape focused on implementing new features rather than on fixing problems with the features they already supported, and adding proprietary features and creating features that were in direct competition with existing features in the other browser, but implemented in an incompatible way.

Developers at the time were forced to deal with ever increasing levels of confusion when trying to build web sites, sometimes to the extent of building two different but effectively duplicate sites for the two main browsers, and other times just choosing to support only one browser and block others from using their sites. This was a terrible way of working, and the inevitable backlash from developers was not far away.

### The formation of the W3C

In 1994, Tim Berners-Lee founded the World Wide Web Consortium (W3C) at the Massachusetts Institute of Technology, with support from CERN, DARPA (as ARPA had been renamed to) and the European Commission. The W3C’s vision was to standardize the protocols and technologies used to build the web such that the content would be available to as wide a population of the world as possible.

During the next few years, the W3C published several specifications (called recommendations) including [HTML 4.01](http://www.w3.org/TR/html401/), the format for [PNG images](http://www.w3.org/TR/PNG/), and [Cascading Style Sheets](http://www.w3.org/Style/CSS/) versions 1 and 2.

However, the W3C did not (and still do not) enforce their recommendations. Manufacturers only had to conform to the W3C documents if they wished to label their products as W3C-compliant. In practice, this was not a valuable selling point as almost all users of the web did not know, nor probably care, who the W3C were (this is still the case, to a large extent). Consequently, the browser wars of the nineties continued unabated.

### The Web Standards Project

In 1998, the browser market was dominated by Internet Explorer 4 and Netscape Navigator 4. A beta version of Internet Explorer 5 was then released, and it implemented a new and proprietary dynamic HTML, which meant that professional web developers needed to know five *different* ways of writing JavaScript.

As a result, a group of professional web developers and designers banded together. This group called themselves the [Web Standards Project (WaSP)](http://www.webstandards.org/). The idea was that by calling the W3C documents standards rather than recommendations, they might be able to convince Microsoft and Netscape to support them.

The early method of spreading the call to action was to use a traditional advertising technique called a roadblock, where a company would take out an advert on all broadcast channels at the same time, so no matter how a viewer would flick between channels, they would get exactly the same message. The WaSP published an article simultaneously on various web development focused sites including builder.com, Wired online, and some popular mailing lists.

Another technique the WaSP used was to ridicule the companies involved with the W3C (and other standards bodies) that focused more on creating new, often self-serving, features rather than working to get the basic existing standards supported correctly in their products to start with (this includes some browser companies that shall remain nameless here). This doesn't mean that the WaSP ridiculed the W3C themselves, rather they ridiculed the companies that became W3C members and then misbehaved.

The W3C has a few full time staff, but most of the people who work on the standards are volunteers from member companies, eg. Microsoft, Opera, Mozilla, Apple, Google, IBM and Adobe, to name a few of the biggest ones.

This all sounds a bit negative, but the WaSP didn’t just sit there criticising people — they also helped. Seven members formed the CSS Samurai, who identified the top ten problems with the CSS support in Opera and other browsers (Opera fixed their problems, others did not).

### The rise of web standards

In 2000, Microsoft released Internet Explorer 5 Macintosh Edition. This was a very important milestone, it being the default browser installed with the Mac OS at the time, and having a reasonable level of support for the W3C recommendations too. Along with Opera's decent level of support for CSS and HTML, it contributed to a general positive movement, where web developers and designers finally felt comfortable designing sites using web standards, as they knew they would work to a reasonable level across multiple browsers.

The WaSP persuaded Netscape to postpone the release of the 5.0 version of Netscape Navigator until it was much more compliant (this work formed the basis of what is now Firefox, a very popular browser). The WaSP also created a Dreamweaver Task Force to encourage Macromedia to change their popular web authoring tool to encourage and support the creation of compliant sites.

The popular web development site A List Apart was redesigned early in 2001 and in an article describing how and why, stated:

> In six months, a year, or two years at most, all sites will be designed with these standards. […] We can watch our skills grow obsolete, or start learning standards-based techniques now.

That was a little optimistic — not all sites, even in 2008, are built with web standards. But many people listened. Older browsers decreased in market share, and two very high profile sites redesigned using web standards: Wired magazine in 2002, and ESPN in 2003 became field leaders in supporting web standards and new techniques.

Also in 2003, Dave Shea launched a site called the [CSS Zen Garden](http://www.csszengarden.com/). This was to have more impact on web professionals than anything else, by truly illustrating that the entire design can change just by changing the style of the page; the content could remain identical.

Since then, web standards usage have become "de rigeur" in the professional web development community. And in this series, we will give you an excellent grounding in these techniques so that you can develop clean, semantic, accessible and standards-compliant websites!

## The new breed of web standards

After 2003, web standards didn't just sit still. New practices started to really come to the forefront, with many web sites being more like desktop applications than static pages. This new breed of sites is way more complicated than what the web was really intended for, and we still have to concern ourselves with making them semantic, accessible and usable!

When HTML 4 was nearing completion, the W3C decided (in a [workshop run in 1998](http://www.w3.org/MarkUp/future/)) that in terms of markup languages, the future of the Web was XML and XHTML, not HTML ([comparison of XHTML and HTML](http://www.w3.org/wiki/The_web_standards_model_-_HTML_CSS_and_JavaScript#What_is_XHTML.3F)). So the W3C drew a line under HTML 4.01 and instead concentrated on the [XHTML 1.0](http://www.w3.org/TR/xhtml1/) spec, finished in early 2000. XHTML 1.0 is just the same as HTML 4.01, except that it uses the stricter markup syntax rules of XML (more on this later). [XHTML 2.0](http://www.w3.org/TR/xhtml2/) soon followed, which added a whole bunch of new powerful features, and aimed to be the next big thing on the Web.

The trouble with XHTML 2.0 is that it wasn't backwards compatible with the markup already on the Web — the elements worked differently, XHTML did not work properly in Internet Explorer, which still has the majority browser market share as of the time of writing, the developer tools available weren't ready for working with XML, and it didn't reflect what web developers were REALLY doing out there in the wild wild web.

In 2004, a group of like minded developers and implementers (including representatives from Opera, Mozilla and slightly later, Apple) got together and formed a breakaway spec group called the [WHATWG](http://www.whatwg.org/), with the aim of writing a better HTML markup spec that could handle authoring the new breed of web applications, without — crucially — breaking backwards compatibility.

The result was the [Web Applications 1.0 specification](http://www.whatwg.org/specs/web-apps/2005-09-01/), which documented existing interoperable browser behaviours and features, as well as new features for the Web stack such as APIs and new DOM parsing rules. After many discussions between W3C Members, on March 7 2007 the work on HTML was restarted with a new HTML Working Group in an open participation process. In the first few days, hundreds of participants joined to continue to work on the next version of HTML. One of the first decisions of the HTML WG was to adopt the Web Applications 1.0 spec and call it HTML5.

HTML5 is a really good thing for web developers and designers, because it:

-   Is mostly backwards compatible with what's already there — you don't need to learn completely new languages to use HTML5. The new markup features work in the same way as the old ones (although the semantics of some elements have been changed — we will cover these differences in a future article), and the new APIs are based on mostly the same JavaScript/DOM that developers have been programming in for years.
-   Adds powerful new features to HTML that were previously only available on the Web using plugin technologies like Flash, or with complex JavaScript and hacks. Form validation and video are prime examples.
-   Is better suited to writing dynamic applications than previous HTML versions (HTML was originally designed for creating static documents).
-   Has a clearly defined parsing algorithm so that all browsers implementing HTML5 will create the same DOM from the same markup, regardless of validity. This is a massive win for interoperability.

The evolution of CSS is not nearly as long winded and controversial as that of HTML, but it is still very interesting, and worth a mention here. The CSS2 specification was nearing completion around 1999/2000, and although it was a powerful language with many great features, its creators knew that it had limitations. There were a number of visual/stylistic things that CSS couldn't do, and that developers had to turn to hacks, JavaScript or plugins to achieve. This includes things such as animation, dynamic layouts, and using custom fonts on pages.

To begin to address this, work started on CSS3 as early as 2000. The spec writers decided on a modular structure, with different pieces of distinct functionality being broken down into manageable chunks. This made it easier not only for the writers to write, but also for the browsers to implement, and the web designers/developers to learn. A lot more features have been added since the first spec version in 2000, and we didn't start to see browser support for many of the features until about 2006. At the time of writing, CSS3 has over 40 modules in various stages of completion. You can track their progress and find out more at the W3C [CSS current work & how to participate](http://www.w3.org/Style/CSS/current-work) page.

You can find more out about CSS3 and HTML5 later on in the course.

## Summary

In this article we’ve looked at how the modern Internet was created as a result of the space race, how Tim Berners-Lee defined hypertext for a generation and how the commercial interests of two companies caused one of the most notable developer backlashes ever seen. The term web standards is now more widely used by web professionals than any other term applied by the [W3C](http://www.w3.org/) (in fact the W3C have started to use the term on their own pages), so that is what we are going to teach you — the *standards* way to build web sites.

## Further reading

If you want to know more, you may like to visit some of the following sites:

-   [The history of the Internet (wikipedia)](http://en.wikipedia.org/wiki/History_of_the_Internet)
-   [The history of the World Wide Web (wikipedia)](http://en.wikipedia.org/wiki/History_of_the_World_Wide_Web)
-   [The history of the W3C](http://www.w3.org/Consortium/history)
-   [The Web Standards Project](http://webstandards.org/), and their [history](http://www.webstandards.org/about/history/)
-   [A List Apart](http://www.alistapart.com/)
-   [CSS Zen Garden](http://www.csszengarden.com/)

## Exercise questions

Or you might like to try researching further, by answering these questions:

-   What browsers are available on the Internet today for users of Windows, Mac OS X and Linux?
-   What percentage of web users use each browser?
-   What browsers do mobile devices use when accessing web pages?
-   How many web standards have the W3C published, and which are widely supported by browser manufacturers today?

Note: This material was originally published as part of the Opera Web Standards Curriculum, available as [2: The history of the Internet and the web, and the evolution of web standards](http://dev.opera.com/articles/view/2-the-history-of-the-internet-and-the-w/), written by Mark Norman Francis, and [Get familiar with HTML5!](http://dev.opera.com/articles/view/get-familiar-with-html5/), written by Chris Mills. It is published under the [Creative Commons Attribution, Non Commercial - Share Alike 2.5](http://creativecommons.org/licenses/by-nc-sa/2.5/) license, which is compatible with the licenses of the originals.
