---
title: 'Introduction to mobile web'
tags:
  - Pages
  - with
  - broken
  - file
  - links
  - Tutorials
  - WSC
uri: 'tutorials/Introduction to mobile web'

---
## Introduction

The [Web Standards Curriculum Table of contents](http://www.w3.org/wiki/Web_Standards_Curriculum) is about advocating best practices for the web and providing complete coverage of all the skills you need to create modern Web sites, in doing so making the Web a better place for all of us to work and browse. This mini series expands the core web standards curriculum articles, look at all the skills and concepts you should take on board to help optimize your Web sites so that they run successfully on mobile (and other alternative) devices. I’ll start by taking a look at the subject area in general and special considerations for marking up and running pages on mobile devices, then move on to styling, scripting and testing as they relate to **mobile web development**.

## A definition of the mobile web

The mobile web is one of those over-used terms that has lost all of its meaning, or worse yet, continues to confuse and perpetuate the mobile myth. If you were to ask web developers to define what the mobile web means, you would get as many different answers as people you asked. It is important then, to define what I mean by the mobile web and how you should be discussing and thinking about it.

The W3C has been pushing the idea of One Web. [This] means making, as far as is reasonable, the same information and services available to users irrespective of the device they are using. However, it does not mean that exactly the same information is available in exactly the same representation across all devices. The context of mobile use, device capability variations, bandwidth issues and mobile network capabilities all affect the representation. Furthermore, some services and information are more suitable for and targeted at particular user contexts. Source: the [W3C Mobile best practices one web](http://www.w3.org/TR/mobile-bp/#OneWeb) page.

Having a second web just for mobile devices is contrary to the W3C’s vision and is not what we mean by mobile web. You should refrain as much as is possible from maintaining a second version of your web sites specifically targeted at mobile devices. This requires a bigger initial outlay and becomes a maintenance nightmare. You should be able to create a Web site that offers an acceptable user experience on desktop and mobile browsers.

Using Web Standards and best practices, you should be able to make your site mobile friendly without too much extra work. The mobile web is an ever-growing corner of the market that businesses cannot afford to ignore. In a number of countries, more people use mobile phones to access the Web than desktop computers, and somewhere in 2008 the percentage of the world's population that carries mobile phones broke past the 50% barrier - an estimated 4 billion phones. An estimated 1 billion of these are capable of Internet access — too big a market to ignore. ([Source: Forum Nokia](http://www.forum.nokia.com/I_Want_To/Mobilise_Websites/Why_mobilise_websites.xhtml).)

## Challenges associated with the mobile web

The mobile web has always been confusing and difficult for many people to get used to developing for, due mainly to lots of over-hyped jargon and terms that the average web developer has never seen or needed to deal with. Things like content carriers, WAP and the deck, many of which aren't really relevant to the subject area any more. When we create traditional HTML websites, we simply upload them to our server space with our Web-hosting provider and that’s it. It didn’t matter if the customer was coming from America, Europe, Asia or elsewhere, or if they were on a dial-up modem at home or a super-fast fiber optic connection at a University; all the infrastructure between your Web site and the customer’s desktop computers worked the same way every time.

This is not true when we are talking about mobile devices accessing the Web. In the world of mobile carriers, different companies use different hardware for their cell towers, they compress the data differently or not at all, and factors like signal strength and availability can vary a lot. This is before we even get to the capabilities of the software on the device itself!

While that sounds daunting, you shouldn’t let it scare you. As a web developer or designer, all you need to understand to create your Web site in a mobile friendly way is that there are some considerations you need to take into account. These limitations include styling, scripting and thorough testing on a variety of devices. Your existing skill-set for creating traditional web sites is much the same as for mobile web sites. The rest of this article will summarize all of these points to help give you a feel for the topic and address all of the areas to consider. Future mobile articles will give these areas a deeper treatment.

## Mobile limitations

While creating a site that will work on mobile devices largely involves sticking to the same web standards and best practices as you need to use for desktop browser-compatible sites, you still need to consider the limitations imposed by such compact devices. While the mobile infrastructure is getting better and more devices are equipped with WiFi, there are still some issues. Hopefully, over time, the following points will become obsolete, but for the near future these are still critical considerations today, and will remain so for some time. You must realize that the capabilities of mobile devices differ greatly and that the top of the range smartphones, such as the iPhone, HTC Touch Diamond and Samsung Omnia (and other S60 and Windows Mobile-based phones), constitute only a small percentage world-wide of the overall Web-enabled phone population.

### Screen size/resolution

For those of you too young to remember, there was a time when you would visit a Web site and they would have a small disclaimer along the lines of Best viewed in Netscape Navigator at 640x480. You couldn't guarantee the higher resolutions we take for granted today. On mobile devices, screen resolutions still vary greatly, and this doesn't look as if it will change any time soon.

When constructing a mobile version of your Web site, how can you be sure that your design will work across the different screen resolutions and dimensions? The simplest strategy is to keep your layout as simple and fluid as possible. The ultimate ideal is to keep your page contents all in a single column stacked on top of each other, so no matter how wide or skinny the screen resolution is, the information simply wraps. You will need to test how well your design works with and without CSS and JavaScript.

Using CSS media queries, JavaScript or the `viewport` meta tag, it is possible to send some CSS targeted specifically to mobile devices without any server-side coding. You will learn more about these later on in this series of articles.

### Input mechanisms

Mobile devices have very different methods of input than desktop machines. When you are at work, your desktop machine probably has a full QWERTY keyboard, a multi-button mouse, possibly a number pad, etc. On a mobile device, you might only have a number pad. You can’t guarantee a full QWERTY keyboard or a pointing device. This makes data entry, even cycling through links, a different experience than when at a stationary desk.

If you have built your Web site using progressive enhancement, then its functionality should not depend on any of these advanced input devices, but should be accessible to everyone using just about any form of input device.

### Processing power and available memory

Mobile devices generally have less memory than their desktop brethren. This creates limitations in the amount of processing they can handle, which limits implementations of JavaScript, Flash and other technologies. These tend to drain batteries, create a slower user-experience and increase the bandwidth - this last point can increase the cost to the user of downloading your web content if they are paying by the kilobyte, which many are. As we’ll see later, these processor limitations account for the mobile web’s evolution along the XML path rather than the HTML/SGML path.

### Available fonts and colours

On your desktop computer, you can happily install all sorts of fonts and families, from serif to san-serif, from symbols to wingdings, but on mobile devices, you are not so privileged. Some devices have as few as one standard fixed-width font, and perhaps a bold or italic variant. This makes corporate branding a nightmare. Not to mention all your nicely designed navigation items in variable width fonts looking bad!

Along with limited fonts, some devices have a limited colour palette, although this is less of an issue now - most new phones come with thousands of colours, and monochrome phones are rare now.

### Web standards support

Not all phones are equipped with web browsers that share the capabilities of today’s modern desktop browsers. Some have full support for the common Web Standards like HTML, CSS and JavaScript. Some only support a certain subset of these standards or use different standards entirely (see the next section for a discussion of WML, cHTML and XHTML-MP). Some support HTML, but not CSS or JavaScript. Other mobile browsers such as [Opera Mini](http://www.opera.com/mini/) use a proxy system in which a server farm retrieves the requested web page, optimizes and reduces it in file size, then sends it to the browser for display.

The strategy here is to test, test, test, and make sure your Web sites degrade gracefully on lower-capability browsers.

Note that you can test web sites on Opera Mini using the [Opera Mini Simulator](http://www.opera.com/mini/demo/) if you haven't got a phone handy.

## Mobile advantages

Mobile devices do have some advantages over their desktop and even laptop cousins. When you are designing sites for mobile devices, it is possible to take advantage of some of these features to enrich the experience over other devices.

### Mobile means moving about!

Mobiles (and laptops for that matter) can go with you wherever you go, which opens up a whole world of new possibilities for location-aware applications — applications that give you appropriate data depending on where you are, for example restaurant suggestions, transport details, cinema times and locations, location of your friends, etc. Current location can be captured by some devices, through means such as GPS, web services and triangulation, and you can use this information in your web applications in various ways, for example through the experimental [W3C Geolocation API](http://www.w3.org/TR/geolocation-API/), or through a location broker API such as [Yahoo! Fire Eagle](http://fireeagle.yahoo.net/). I won’t cover LBS any more in this article series, as it is an advanced topic, and the technologies to allow you to do so are largely at a pretty early stage. Here are some links to some more details about some of the important technologies around this area:

-   [Google Latitude](http://www.google.com/latitude/)
-   [Yahoo! Fire Eagle](http://fireeagle.yahoo.net/)
-   [W3C Geolocation API spec](http://www.w3.org/TR/geolocation-API/)
-   [GeoRSS: Geographically encoded objects for RSS feeds](http://www.georss.org/)

### Cameras, phones and other hardware features

Mobile devices have many hardware features that desktop computers don’t. The two most obvious are:

-   **Camera**: You’ll be hard-pressed to buy a phone that doesn’t have a built-in camera these days and we are beginning to see APIs to allow web applications to interface with such devices.
-   **Phone**: Let’s not forget that the primary purpose of a mobile phone is to call people! This can be smoothly integrated into your website by using the little known `tel:` protocol. Just like you use a `mailto:` to link to an email address, you use `tel:` to link to a phone number. When you click the `tel:` link it causes the phone to dial

        <code><a href="tel:5121234567">Phone 5121234567 to book a table</a></code>

    Note the inclusion of the phone number in the link text as well — while this may seem a little repetitious, bear in mind that some browsing devices won’t support the `tel:` protocol, such as our old friend the desktop computer.

## Mobile web technologies

Your knowledge of Web Standards as applied to creating traditional web sites can easily be applied to developing mobile sites. There are however some additional acronyms and a bit of history to fully understand where we are today and how we got here. Depending on your target audience and the types of phones they are using, you might just be able to stick to standard HTML and CSS, or you might need to take a step back to something different.

### WML

WML stands for Wireless Mark-up Language and was created in 1998. Before that, there was no standard used specifically for mobile devices.

Just like web browsers use HTML for content structure, older mobile device browsers use WML - if you need to support really old mobile phones using WML browsers, you will need to know about it. WML is XML-based (an XML vocabulary just like XHTML and MathML, but not HTML) and does not use the same metaphor as HTML. HTML is a single document with some metadata packed away in the `head`, and a `body` encapsulating the visible page. With WML, the metaphor does not envisage a page, but rather a deck of cards. A WML file might have several pages or cards contained within it.

The following is an example WML file:

    <code><?xml version="1.0"?>
    <!DOCTYPE wml PUBLIC "-//WAPFORUM//DTD WML 1.1//EN"
    "http://www.wapforum.org/DTD/wml_1.1.xml">
    <wml>
      <card id="home" title="Example Homepage">
        <p>Welcome to the Example homepage</p>
      </card>
      <card id="contact" title="Example Contact Page">
        <p>Welcome to the Example Contact page</p>
      </card>
    </wml></code>

There are several downsides to using WML. Even though it does have a scripting language, it does not allow for very rich interactions or applications to be built. It was designed for very small screen and low-resolution devices. Older WML browsers do not support more widespread image formats such as GIF and JPEG. The corresponding image format, WBMP, supports only a black and white color scheme and it is difficult to create WBMPs as they are not easily supported in modern image manipulation tools. WML is also not easily interoperable with other markup formats, so having a WML version of your site does mean that you need to maintain two separate versions of a web site, which adds complexity, overhead and cost to the project.

We really do not recommend that you start creating sites using WML - this is really just a history lesson. For old, low power mobile devices there is [Opera Mini](http://www.opera.com/mini), which can run on pretty much any device with a JVM).

### Compact HTML

Around the same time as WML was created, CHTML was also born. CHTML stands for Compact HTML and is a subset of early versions of HTML from the late nineties. Since CHTML is much more like HTML it can be viewed in regular desktop browsers. Even back in 1998, they were beginning to realize the difficulty with maintaining multiple versions of a single Web site.

Eventually, CHTML evolved into i-mode HTML in Japan, but it has since been superseded by XHTML Basic and then XHTML Mobile Profile elsewhere. The use of Compact HTML has been relegated to history, but it was a perfect demonstration of the forward thinking of its creators in following the One Web philosophy.

### XHTML mobile profile

XHTML-MP is a subset of the XHTML mark-up, which is very similar to regular HTML but with a few more restrictions. Knowing standard HTML gets you 99% of the way towards understanding XHTML and XHTML-MP.

The history of XHTML-MP is an interesting one. After WML, XHTML-MP was independently proposed to bring mobile mark-up inline with the XHTML/HTML that developers were used to coding. The W3C decided to also get in on the game and created XHTML-Basic, which was very similar to XHTML-MP with the same intent. Then XHTML-MP 1.2 came about to add some functionality into the mark-up and XHTML-Basic version 1.1 appeared, echoing this. These two standards are pretty much interchangeable in terms of functionality.

Since XHTML-MP and XHTML-Basic are a subset of XHTML, they have more restrictions than standard HTML. This keeps mobile devices from having to support large amounts of code and processing that are used only by a small amount of sites. (For more information about the limitations in XHTML-Basic you can read [David Storey's article on mobile markup at dev.opera.com](http://dev.opera.com/articles/view/mobile-markup-xhtml-basic-1-1/).)

the below code shows an example XHTML-MP document (note the different doctype):

    <code><?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE html PUBLIC "-//WAPFORUM//DTD XHTML Mobile 1.1//EN"
     "http://www.openmobilealliance.org/tech/DTD/xhtml-mobile11.dtd">
    <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en">
      <head>
        <title>Example Page</title>
      </head>
      <body>
        <h1>Example XHTML-MP page</h1>
      </body>
    </html></code>

Note that one subtle difference between XHTML-MP and XHTML-Basic is that XHTML-Basic needs to be served up with a mimetype of `application/xhtml+xml`. Doing so tends to break older versions of Internet Explorer, which attempt to download or display the file as XML, rather than render it as a Web page. XHTML-MP on the other hand commonly uses a mimetype of `application/vnd.wap.xhtml+xml`, but can also be served as `application/xhtml+xml` or even `text/html` so that any browser can display it.

### XHTML

Finally, there is plain XHTML. This is the XML version of your vanilla HTML. If you are a competent Web Developer, then this should be nothing new to you. In fact, if you are not creating anything wildly specific, you might be producing XHTML that is MP/Basic compliant already. You can easily switch the doctype and see if you get any validation errors.

As we’ve seen, all of the mark-up languages available to mobile devices are from the XML family. The idea behind this is to streamline the code in the browser so the already less powerful mobile browsers do not have to deal with incorrectly nested elements and other common mark-up mistakes that can cause errors and increase the amount of processing power needed to render the Web page.

As more and more mobile devices are using slimmed down versions of their desktop counterpart’s rendering engines, the ability to browse standard (X)HTML pages is increasing. And of course, you can stick with an HTML doctype if you wish — many mobile browsers will support those too; I am recommending an XHTML doctype really so that a strict set of rules is enforced, hopefully leading to fewer errors, smaller downloads, and less processing strain for mobile devices viewing your site. But it is up to you.

## CSS and Semantic Mark-up

Many of the design and layout tricks that we have developed over the years to keep our mark-up as semantic as possible, fall down on mobile devices.

### Image Replacement

One example is image replacement for headlines - the use of CSS to create a background image on a heading element and then shift the text off the page to display just the background image, which could be a company logo, or a really fancy typographically appealing version of the text heading. This allows designers to have more control over the design of the heading while at the same time keeping the original text heading present so that it can be read by screen readers and search engines.

Sadly, some browsers on mobile devices support some or none of the CSS standard. When optimizing for mobile devices, you are generally trying to cut down on file size and HTTP requests while retaining design values and functionality. It is very difficult though - no matter which way you move to optimize or improve user experience for some mobile browsers, you will lose ground on the other facets.

Let's look at simple image replacement use case, to give you more of an idea of this. The below example uses a nice tiled blue gradient background image, and demonstrates how difficult it can be to get the exact corporate logo and colours you want, while at the same time keeping it semantic when targeting devices that do not support CSS.

Figure 1 shows the final result we'd like.

[finished heading with background gradient and image replacement](/w/index.php?title=Special:Upload&wpDestFile=mobile_figure1.jpg)

Figure 1: Our finished heading, with background gradient and image replacement.

The markup for this heading looks like so:

    <code><h1>ABC co.</h1></code>

The process by which we would optimize this heading might go something like this.

1.  You'd first specify a solid blue background color on the heading as a default.

<!-- -->

    h1 { background-color: blue; }

1.  We can then do our trick of moving the `ABC co.` off the page with a negative text indent, and replace it with a background image of the company logo.

<!-- -->

    h1 span { text-indent: -9999px; background-image('logo.png'); }

This gives us the rendering shown in Figure 2.

[heading text has been replaced with a background image](/w/index.php?title=Special:Upload&wpDestFile=mobile_figure2.jpg)

Figure 2: Our heading text has been replaced with a background image.

1.  Next, we can progressively enhance the CSS to include the gradient background image.

<!-- -->

    h1 { background-color: blue; background-image: url('gradient.gif'); }

This results in display along the lines of Figure 3.

[the company logo, and our background gradient](/w/index.php?title=Special:Upload&wpDestFile=mobile_figure3.jpg)

Figure 3: We now have the company logo, and our background gradient.

We have achieved our basic goal, but need to remember how this looks in browsers that do not support aspects of CSS or CSS at all.

Some browsers don't support CSS background images (even desktop web-browsers don't always support them when printed), because of this your company logo would not appear and the text is still positioned off the page so the header would end-up looking like Figure 4:

[No background image means we do not see the company logo](/w/index.php?title=Special:Upload&wpDestFile=mobile_figure4.jpg)

Figure 4: If the browser does not support CSS background images, we don't see the company logo!

Other browsers mess up the text indenting, so you see both, which doesn't look great - see Figure 5.

[In some browsers we see the original text as well as the background image](/w/index.php?title=Special:Upload&wpDestFile=mobile_figure5.jpg)

Figure 5: In some browsers we see the original text as well as the background image

The only way around this is to avoid using the text-swapping trip and change the mark-up so the image is included using an `image` element, not a CSS background image property:

    <h1><img src="logo.png" alt="ABC co. Logo"/></h1>

This would give you the rendering shown in Figure 6 - the same as when we started - but the mark-up isn't as clean.

[HTML img element means more heading support but the markup is less clean](/w/index.php?title=Special:Upload&wpDestFile=mobile_figure6.jpg)

Figure 6: Using an HTML `img` element means more support for heading, but the markup is less clean.

However, some poorer devices can't even render background colors, so your fancy transparent logo image ready for any background style will appear as white text on a white background - see Figure 7!

[no background colours means white on white](/w/index.php?title=Special:Upload&wpDestFile=mobile_figure7.jpg)

Figure 7: No support for background colours means that your image will appear white on white - terrible!

As a last resort, we'll reluctantly decide to make the logo background color solid blue instead to make it visible across as many browser types as possible and drop the use of the gradient background image altogether - see Figure 8.

[The logo background is now solid blue, so it is visible on devices without background colour support](/w/index.php?title=Special:Upload&wpDestFile=mobile_figure8.jpg)

Figure 8: The logo background is now solid blue, so it is visible on devices without background colour support.

While this is not optimal mark-up, but gives the most consistent rendering across all devices. As with any development, there are trade-off to what can and can't be achieved, you need to be aware of these problems and address them accordingly.

## Summary

This article was just a brief introduction to the world of mobile Web Development, including some of the technical and design hurdles you need to be aware of before getting started. I touched on issues with CSS, mark-up and some of the limitations and advantages across the different mobile browsers.

All of these different renderings and interpretations are not to be considered bugs (well some are) but instead features of the device. Sure the phone might not support a colour screen or JavaScript, but the battery will probably last longer. As you optimize for specific devices, it changes the functionality on others. This might seem like a major issue to developers and designers stuck in a pixel perfect world, but in reality these differences are acceptable — even expected. The idea of One Web does not mean exactly the same look and feel across all devices. Just as this is an unobtainable goal on the desktop, it is even more so on mobile devices.

The sooner you accept this and move on, the sooner you can begin to develop better Web sites. From screen-size and resolution, to installed fonts and colors, to image and HTML support, not all phones are created equal, so the best you can do is present the best, most flexible, equivalent design you can — which does not mean identical. This is where testing is key! Testing is an important part of any web development process, but especially so for mobile devices due to the diverse range of devices and capabilities.

## Exercise questions

-   How many versions of your website should you create to support the mobile web?
-   Explain progressive enhancement
-   Do mobile devices support XHTML?
-   What image format is natively supported in WML?
-   How do you mark-up a telephone number as a link?

Note: This material was originally published as part of the Opera Web Standards Curriculum, available as [Mobile 1: Introduction to the mobile web](http://dev.opera.com/articles/view/introduction-to-the-mobile-web/), written by Brian Suda. Like the original, it is published under the [Creative Commons Attribution, Non Commercial - Share Alike 2.5](http://creativecommons.org/licenses/by-nc-sa/2.5/) license.
