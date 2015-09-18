---
title: 'Part 1: The beginning'
notes:
  - "Truncate content that is duplicate.\nLook at scratchpad https://docs.webplatform.org/wiki/TEST:beginners \n\nAlso, maybe get in touch with CommonCraft and ask to embed their video about the World Wide Web http://www.commoncraft.com/video/world-wide-web"
readiness: 'Almost Ready'
summary: 'The very first part of our beginner''s material gives you some important background on how website works in what we commonly call &quot;front end&quot; layer. Note that we limit our topics to what happens on the web browser and that typical sites would have code written that is executed on the server side that generates the HTML.'
tags:
  - Basic_Pages
uri: 'Beginners/the beginning'

---
## Summary

The very first part of our beginner's material gives you some important background on how website works in what we commonly call &quot;front end&quot; layer. Note that we limit our topics to what happens on the web browser and that typical sites would have code written that is executed on the server side that generates the HTML.

## Beginners submenu

The **[Beginners](/Beginners)** section covers the various aspects of web development separated in 9 parts, you can navigate through them using this list.

-   **1. The beginning**
-   [2. A crash course in web site code](/Beginners/crash_course)
-   [3. Planning](/Beginners/planning)
-   [4. Structuring our content with HTML](/Beginners/html)
-   [5. Styling our content with CSS](/Beginners/css)
-   [6. Programming fundamentals](/Beginners/programming)
-   [7. JavaScript](/Beginners/javascript)
-   [8. Advanced topics](/Beginners/advanced)
-   [9. Browser testing](/Beginners/browser_testing)
-   [Glossary](/Beginners/glossary)

## Course Introduction

### Who is this for?

Our beginner’s guide is written for complete beginners to the world of website code, who don't know what to learn first, and just need a single point that will lead them in the right direction with confidence. This series of articles guides you through all the basics of web design and development, so you can get up to speed relatively quickly, learning just enough to not feel lost and overwhelmed, and get comfortable with the area in general.

This particular course's approach is different from most other web development introductory courses because it tries to give you important background information of how the web works. Most web development courses avoid this, because they're not actually interested in telling you how the bricks are made: They just want you to start building the house. Although a time-saving exercise, we think that you should know the basics of how the web works if you're going to be a web developer.

Also, this course is for front-end web developers. That means we teach you how the front, or client side of the web works, not the processing, or back, side. We teach you how to create webpages with languages like HTML, CSS, and JavaScript (which we'll explain later). This course is not for back-end web developers, who are responsible for hosting web servers (which we'll also explain later).

If any term is hard to understand, kindly refer to the [glossary for beginners](/Beginners/glossary). Happy reading!

### What it will teach, and what it won't

This course will teach you enough about web design and front-end development that you'll be free to explore on your own and experiment with the technologies that make the web work. In short, you'll be confident and comfortable with the usage and coding of web technologies like HTML, CSS, and JavaScript. Further, it will make you familiar with the structuring, planning, and testing of websites, offline or online.

This course won't teach you about back-end processing and server-side scripting. Also, this course specifically won't go in much details of other interesting and efficient web technologies like SVGs, accessibility best practices, or JavaScript APIs. For learning them, you'll have to visit our [main page](/Main_Page).

## What is the web?

The Internet is a global network of networks of computers that connects computers from all around the world. The World Wide Web, or web, is a virtually interconnected spiderweb-like nexus (and thus the name) of information connected to each other by **links**. In short, the World Wide Web is a part of the Internet. There are other services under the Internet too, like emails, fax, FTP, microblogging, instant messaging, etc..

The links point to other websites and the Internet is used to get there. Most computers in the network merely consume information from other places (also know as **clients**), whereas others can consume information from other places and send information to other computers that ask for it (**servers**).

The main components which the web depends on are:

-   **Web Clients**: Computers that get information from web servers. The most common form of web clients are web browsers which have a good user interface and do not require technical information to use. Browsers make the web open. Nowadays, a client can be a smartphone application, a tablet browser, a built-in Android surfer for a television, a screen reader, a browser on a laptop, and so on.
-   **Web Servers**: Computers that serve information to web clients on requests.
-   **DNS**: Stands for "Domain Name System." A set of servers communicating together databases of Internet’s way to refer to another computer into human words. DNS turns a domain name like "en.wikipedia.org" into an IP address ("208.80.154.224:80" in this case), where the server is located.
-   **Hypertext**: The text of the web, what web servers give to web clients. The text of the web includes many things and has changed over time, but there are two important aspects to the text of the web we shall mention below. You can read a Wikipedia article on hypertext [here](http://en.wikipedia.org/wiki/Hypertext).
-   **Hyperlink**: A link that refers to another set of hypertext. If this link refers to a different domain name, the web client will need to use DNS to find the right IP address of the server.
-   **HTTP**: Stands for HyperText Transfer Protocol. The protocol of how web requests from clients and information from web servers should be written so they understand each other.

[INSERT IMAGE OF TOWN AND CITY CONNECTED BY ROAD, WITH DELIVERY VAN GOING ALONG ROAD TOWARDS TOWN. I'D LIKE IT TO EXPRESS SOMETHING LIKE THE FOLLOWING]

Imagine the web as being like a series of towns and cities connected by roads. One town (the client, a regular web user) wants to get a supply of chocolate (website) from the awesome chocolate maker in the city, so the town's mayor (web browser) writes a letter (web request written in HTTP) to send to the chocolate maker in the city. The town's mayor has the name of the business of the chocolate maker (domain name), but doesn't actually know the address, so they give it to the postman, and the postman takes it there (DNS uses the domain name and sends the request to the right IP address using the Internet). The chocolate maker is happy to give the town some of its chocolate supply, so it sends a delivery van full over right away (the hypertext of the website, web response packaged in HTTP), travelling by the main road (the Internet). Once it gets to the town, the mayor distributes the chocolate to all her townsfolk (displays the web page), and everyone is happy.

Read [How does the Internet work?](/concepts/internet_and_web/how_does_the_internet_work) for more information.

This may sound complicated, but most of this is done transparently, without you having to worry about it. As a beginning web developer, the part you have to worry about is the making of the actual chocolate: That is, the website's content. You don't need to worry about the packaging that is HTTP because web servers deal with that. You just need to make the chocolate because you're the chocolate maker, not the delivery van driver. Have fun!

## Why is the web such a good thing and why should you learn?

The web is the future and the next human revolution. Soon, we'll see smart devices taking over our traditional world. Our televisions, phones, computers, and even other devices like refrigerators, cars, printers, gaming consoles, are going to be integrated seamlessly. The web is going to do that.

Wearable technology, robotics, activity synchronization, fitness tracking, these realms cannot be fully explored without the presence of web. For starters, data fed into wearable technologies is web-first, your activity synchronization is already making your life easier with concepts like browser bookmarks, calendar, contacts, and email sync, etc.

Under these conditions, the web is going to get very big. Desktops aren't the web. Desktops, laptops, smartphones, and tablets are the web. But, we never know what the web will be like. That's what makes web so good to learn and know about. This picture by Brad Frost in [one of his articles](http://bradfrost.com/blog/post/this-is-the-web/) sums it up pretty well:

![webfuture.png](//static.webplatform.org/e/e7/webfuture.png)

## What is accessibility and why is it important

Accessibility is the practice for designing the web for all, not just the visual browsers. There are many devices that aren't like the traditional pieces of software, like screen readers, Braille output, magnifiers, joysticks, etc. As Jennifer Robbins puts it,

> Although intended for users with disabilities such as poor vision or limited mobility, the techniques and strategies developed for accessibility also benefit other users with less-than-optimum browsing experiences, such as handheld devices, or traditional browsers over slow modem connections or with the images and JavaScript turned off. Accessible sites are also more effectively indexed by search engines such as Google. The extra effort in making your site accessible is well worth the effort.

It's common good practice and a human expression to make our websites accessible.

## Bricks of websites: HTML, CSS, JavaScript

Websites are generally documents. In fact, you can create a website from a simple text editor. However, these documents use special markup for different elements, and one can further enhance their looks by styling those elements. For now, you don't have to worry about the style part.

Remember that in our story, the mayor sent a letter to the chocolate maker and they sent back chocolate. However, web clients and web servers send pieces of text to each other and for the World Wide Web to work, they need to be able to read that text. Because of that, there's an organization called the World Wide Web Consortium, or W3C, that decides how the Web should work with official web standards. All web clients and web servers are expected to adhere to these standards and also be able to communicate from older web clients and servers somehow. They define how hypertext on the web should be sent with [the HTTP specification](http://www.w3.org/Protocols/rfc2616/rfc2616.html).

They also decide how the webpage should be displayed with languages called HTML (which stands for HyperText Markup Language), CSS (which stands for Cascading Style Sheets), and JavaScript. These are the languages you'll be using to structure web pages as a front-end web developer. Websites are made of these languages and used by the web browser to display a webpage. There are specifications for these languages, too, but they're not as straightforward to read as the HTTP specification. That's why we have introductory web development courses like these!

Read [The web standards model](/concepts/internet_and_web/the_web_standards_model) for more details on the why and what of web standards.

Just to get you introduced to these languages, we've added descriptions and examples of them below. Enjoy!

**HyperText Markup Language (HTML)**: This language is used to manufacture and outline **the content** of your webpage. It gives your webpage a title and content like regular text, styled text such as bold or italics, paragraphs, lists, tables, and more. It also gives your webpages links to other webpages and allows for embedding of images (by specifying URLs or local directories). HTML is made of **elements** specified by **tags**, like `<div>` and `<p>` and these elements have **attributes** that can change the elements and be used by CSS or JavaScript. A webpage can be simply HTML, but such a webpage would be rather plain and probably unattractive, so the languages of CSS and JavaScript are used.

[INSERT IMAGE OF HTML ELEMENTS AND WHAT THEY CREATE ON THE RENDERED PAGE, SOMETHING LIKE I'VE SHOWN BELOW. ALSO INCLUDE HOUSE OR WALL JUST SHOWING THE BARE ROOF AND BRICKWORK]

The following snippet of HTML code:

    <h1>The title of my story</h1>
    <p id = "thisIsAnAttribute">It was a dark and stormy night.
    Somewhere, an owl hooted.</p>

results in the following:

# The title of my story

It was a dark and stormy night. Somewhere, an owl hooted.

**Cascading Style Sheets (CSS)**: This language is used to style and position the HTML content. It gives your webpage a clean look and more professionalism and a better user interface along with it: It can be used to center your elements, give them background, give them color, putting them into place, and making them how they should be. Note that CSS **rules** or styles can only be applied on an HTML element, by "selecting" them via **selectors**, so if there's no HTML element, CSS cannot work.

[INSERT IMAGE OF CSS AND HTML BEING ADDED TOGETHER TO PRODUCE SOME STYLED TEXT, SOMETHING LIKE I'VE SHOWN BELOW. ALSO INCLUDE HOUSE IMAGE THAT BUILDS ON THE LAST ONE, SHOWING THE HOUSE NOW DECORATED WITH PAINT AND NICE COLOURED TILES?]

Let's apply the power of CSS to our above snippet:

    h1 {
        color: blue;
    }
    p {
        color: red;
    }

This results in the following:

# The title of my story

It was a dark and stormy night. Somewhere, an owl hooted.

Note that there are three parts of a CSS rule. First, we use the selector to select a specific element (`h1`). We then specify arguments. The properties, or attributes are needed to tell the browser what exactly is being manipulated (`color`) and finally the value of that property is specified (`blue`). As with other programming languages, the arguments part is placed within curly braces (`{these}`) and each argument is terminated by a semi-colon (`;`).

**JavaScript**: This language is used to add dynamic functionality to your webpage. It provides the majority of the interactions in webpages, aside from simple things like text-boxes (that are from HTML). JavaScript leads to things happening to the webpage when things are clicked or a key is pressed. JavaScript is a scripting language that is *very* powerful and actually makes webpages a bit dangerous, so be careful with it! Even though JavaScript was originally for the web, JavaScript is actually used in lots of things other than it, but this course will focus on its application to the web.

[INSERT IMAGE OF CSS AND HTML AND JAVASCRIPT BEING ADDED TOGETHER TO PRODUCE SOME STYLED TEXT WITH SOME FUNCTIONALITY, LIKE A POPUP WINDOW OVER THE TOP OF THE PARAGRAPH SHOWING HOW MANY CHARACTERS THE PARAGRAPH CONTAINS. ALSO INCLUDE HOUSE IMAGE THAT BUILDS ON THE LAST ONE, SHOWING THE DECORATED HOUSE WITH SOME COOL FUNCTIONALITY ADDED. HOW ABOUT A SATELLITE DISH ON THE ROOF, AND A WALL MOUNTED TV SEEN THROUGH THE WINDOW?]

Because JavaScript is pretty dangerous, the wiki editor doesn't allow any JavaScript code in the wiki article, so we can't demonstrate it to you. However, think about you clicking the above paragraph and then new text replacing the old text. That's what the following JavaScript code does:

    var paragraph = document.getElementById("thisIsAnAttribute");
    paragraph.onclick = function() {
        this.innerHTML = "Then, the owl flew away into the dark night sky, creating a rather mellow sight, yet happy despite it all.";
    };

Finally, you now understand the building blocks of the mighty web. Interestingly, a major part of the battle is won already! We will expand on these languages in this course and get you started coding in the next article itself!

