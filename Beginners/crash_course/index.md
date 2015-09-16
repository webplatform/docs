---
title: Part 2: A crash course in website code
notes:
  - "(Note1: Tried to handle the below-mentioned stuff. Please run a check and then you can remove these notes. Thanks)\n(Note2: I'm making it Ready to Use. Note1 still needs to be processed.)\nThere are plenty of notes and idea but all incomplete.\nEditorial notes:\n\n Explain what HTML, CSS, and JavaScript are, show how to create some really trivially simple examples\n Show what a simple site structure might look like\n Go through simple HTML anatomy\n Show what an HTML page looks like, explain its purpose. Show head, body, title, and a few other things\n Add some really simple bits to it. headings and paragraphs, bullet points, an image maybe\n explain simple common gotchas - quote problems, incorrect paths, bad nesting, missing out attributes\n Next, go through simple CSS anatomy\n Show how simple CSS selectors work\n Go through how to apply CSS to HTML - 3 ways\n explain simple CSS gotchas - bad pathing, missing semi colons, missing attributes, incorrect adding of classes to elements (I've seen people try to use <class=\"heading\">content</class>) \n next, show simple javascript anatomy and explain how it works\n show some really simple JS use\n explain simple JS gotchas, and explain that it needs quite a bit more understanding than HTML or CSS. But it has more power.\n Take the user through the steps towards getting web space (use a free service, such as http://www.biz.nf/), and get them to set up their FTP, and upload their simple files.\n Show them how they can now view their files on another computer."
readiness: 'Ready to Use'
summary: "This part assumes you want to build a website with almost no prior knowledge. It will start on HTML and CSS to allow you to do that right away. Obviously, we can't teach it all at once, so we will start with certain basic features we expect you might be interested in, and build on from there.\n"
tags:
  - Basic
  - Pages
uri: 'Beginners/crash course'

---
## Summary

This part assumes you want to build a website with almost no prior knowledge. It will start on HTML and CSS to allow you to do that right away. Obviously, we can't teach it all at once, so we will start with certain basic features we expect you might be interested in, and build on from there.

If you have terms you don’t understand, you can see the [Beginners/glossary](/Beginners/glossary) section.

You will quickly find that once you get the hang of how this works, you will be able to figure out how to add the features you want just by looking at the HTML and CSS code and applying that code to your site, or an offline test site.

## Beginners submenu

The **[Beginners](/Beginners)** section covers the various aspects of web development separated in 9 parts, you can navigate through them using this list.

-   [1. The beginning](/Beginners/the_beginning)
-   **2. A crash course in web site code**
-   [3. Planning](/Beginners/planning)
-   [4. Structuring our content with HTML](/Beginners/html)
-   [5. Styling our content with CSS](/Beginners/css)
-   [6. Programming fundamentals](/Beginners/programming)
-   [7. JavaScript](/Beginners/javascript)
-   [8. Advanced topics](/Beginners/advanced)
-   [9. Browser testing](/Beginners/browser_testing)
-   [Glossary](/Beginners/glossary)

## HTML, CSS, and JavaScript

We're assuming you've had your general introduction with HTML, CSS, and JavaScript at the former article of this series. Here we're going to get a bit advanced.

The main file that's uploaded to a server is the HTML file, which includes all the content, directions for servers and browsers, and links to other files (like stylesheets or script files). The HTML markup is used to render text in a specific way by the browser.

Suppose you have a book in which you use a yellow highlighter pen to highlight main concepts. You further use a black ball point pen to circle around the things you find confusing. You have created a markup language of your own. Suppose your language grows inflated with more conventions and at the same time, becomes popular. Now, you need a resource that contains the descriptions of those, right? Like this:

-   **Yellow highlight**: main concept
-   **Blue underline**: definition of a main concept
-   **Black encircle**: difficult or confusing concept

and so on. HTML is just that. It was created to give markup to scientific documents. So if you wanted to show emphasis, you used `em`, not a yellow highlight.

CSS is essentially used for styling the elements and portions of the HTML document. Suppose you really need a yellow highlight instead on emphasis. Here's what you'll do:

``` html
.important {
  background-color: yellow;
}
```

 Note that a CSS rule can only target HTML elements. So there needs to be HTML code too!

``` html
<p class="important">
 Heisenberg's Uncertainty Principle
</p>
```

 We gave the `p` (which means a paragraph) a **class** of "important". A class is a reusable object, that's why you can give something else a class of important too and thus reuse the same style.

JavaScript is pretty dangerous and notorious. We cannot explicitly elaborate on that.

So, in essence, the code becomes like this:

**HTML**:

``` html
<p class="important">
 Heisenberg's Uncertainty Principle: Two properties of an object cannot be known for sure at a given instant.
</p>
<p id="alphaParticle">
 Alpha-Particle Bombarding Experiment: It was carried out to figure that there's lot of empty space in an atom.
</p>
<p class="important">
 M-Theory: According to this more robust form of string theory, there are actually 11 dimensions in the universe!
</p>
```

**CSS**:

``` html
.important {
  background-color: yellow;
}
#alphaParticle {
 background-image: url(electron.png);
}
```

 As you can easily understand, we styled the important class and also the *\#alphaParticle*. What's that? Well, the hash denotes an ID. An ID is different from a class because it can only be assigned to one HTML element.

## An HTML document

This is a basic HTML document.

``` html
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="utf-8">
 <title>The Title Bar Title Goes Here</title>
 <link rel="stylesheet" href="stylename.css" type="text/css" media="screen">
</head>
<body>
<h1>A Level-One Heading</h1>
<p>This designates a paragraph
 This is the body of the document, and all your good stuff goes here.</p>
</body>
</html>
```

 Note that there are essentially two types of markings.

There is the paired `<tag-name>tag contents</tag-name>`, which is how we tell the computer to deal with any block of text from a letter to defining the beginning and end of a whole document.

Then there is the `<tag-name _______________ />` where those are instructions to describe on how to deal with certain situations. The `meta` are about the server communication. In this particular case, we are saying that the file is written in `UTF-8` (i.e. a format that supports multiple language characters at once), and `link` is for asking which file to download along with the HTML document to take care of the visual aspects ("stylesheets"). These stylesheets are a collection of style rules, written in CSS.

## Let's make a website

For your first HTML document, please cut and paste the above into a text editor of your choice and save it as `example.html`, but leave the file opened.

**Important**: Make sure the file-extension is appended to `.html`. In Windows, you might have to go to Tools\>File Options\>Show Extensions of Common Files before this works.

Now go to your browser, choose Open, open this file and see what happens and leave this page open too.

Now add the following (or whatever other text you want) in your editor. Why not put it after the paragraph that's already there:

``` html
<h2>Your Second-Level Heading Here</h2>
<p>Write something <em>add emphasis</em> finish your paragraph and add a list along with maybe?</p>
<ul>
    <li>List Item One.</li>
    <li>List Item Two.</li>
</ul>
```

 Save it.

Go back to your browser and refresh the page and notice what's changed.

Did you see we entered a list there too? A list is a cool part of a webpage. The `ul` tells the browser that an "unordered list" has begun. For an ordered list (with numbers or alphabets), you'll need an `ol`.

Now play a little by trying some other stuff (nothing is better than experimentation when it comes to learning!)

-   `h3` instead of `h2`, or `h4`, `h5`, `h6`; those are [headlines elements](/html/elements/hn) to differentiate titles from body text.
-   Instead of `em`, try `strong`, `sup`, `sub`, or the `b` [tags](/html/elements) in the same way.

Want to call another document?

Create a file beside `example.html`, and call it `example2.html`. Empty the `body` tag, and just write something inside the `body` tag.

We will call `example2.html`, from our `example.html` sandbox document. Add this line:

``` html
<a href="example2.html" title="Another HTML file">Calling example2</a>
```

 Did you notice how we sneaked up the `a` there? That's an anchor. It anchors, or holds, a URL (uniform resource locator), or more commonly a link, to a separate place (which can be a file, another webpage, an email address, etc.). The `href` attribute tells the URL of the target file.

Now, whenever you click on this link, you'll be taken to `example2.html` instantaneously. Congratulations, you learned something that's pretty much the cornerstone of the web!

## Some other things you need to take care of

To be a good web-coder, you need to learn some good practices.

-   **Right use of quotes**: Quotes are used to quote something, somebody, or some saying. But some people use them for style and presentational purposes. Please don't do that. A `q` tag denotes a quote.

-   **Get your paths right**: Many beginning coders face problems when they wrongfully enter paths. Suppose you have an image one directory up named `house.jpg`. When you call it within the page, you'll need a code like this: `<img src="../house.jpg">`. If you have some knowledge of UNIX operating systems, you'll understand what's going on here. Actually, we're telling the browser that the "path" of the picture is at "../", which means one directory up. Besides this, there are many other problems in file paths, that's why you should double-check them and URLs, if any, and inspect them when something goes wrong in the webpage.

-   **Avoid bad nesting**: It's a common problem to do nesting in an illogical and confusing manner. Always try to maintain the hierarchy. A small example will be this:

``` html
<div>
  <p>
    To-Do List
  </p>
  <ul>
    <li>Destroy Mars.</li>
    <li>Conquer Atlantis.</li>
    <li>Enslave all Moon citizens.</li>
    <li>Eat solar plasma in the new Solar Heights.</li>
  </ul>
</div>
```

 Good nesting allows you to see what's going on and a logical hierarchy is always good, like for the time when others debug or check your code, or when you do the same after some months.

-   **Don't miss out the attributes**: HTML attributes are very important and they make a webpage and entire websites more meaningful and suitable for screen readers and other accessibility devices. Some attributes you should never miss out are: `lang` (for telling the browser which language the webpage is written in), `title` (for specifying the name of the browser window/tab and naming elements), `href` (used mostly in links, if you skip it, the link won't point to anywhere), and `alt` (the alt attribute is used to display/read text content when an HTML element, like an image, cannot be loaded).

## Simple CSS anatomy and application

CSS is a detailed language, and for its graceful implementation, we've created the [Part 5](/Beginners/css), but here, you should learn about the simple anatomy of CSS and applying it on HTML elements.

CSS is a language for styling the HTML elements we create. It includes sets of rules. Suppose we need to color all paragraphs silver. These will be the code piece for this:

**HTML**:

``` html
<h1>How to destroy Mars</h1>
<p>It'll be really bad to do this, as the world would be very disappointed,
but for the sake of darkness, we must perform this deed.</p>
<p>First, prepare a rocket with infinite fuel. Check this
page again when you're done. Goodbye.</p>
```

**CSS**:

``` html
p {
  color: silver;
}
```

 The rule will color all paragraphs (we have two) silver, but will leave everything else the way it's meant to be. **Note**: We don't recommend blowing up Mars.

The `p` we used in the CSS is a selector. Selectors select an HTML element and then apply the required styles to it. No selection: no styles applied.

## JavaScript primer

JavaScript is a scripting language that works much like your common programming languages. At the extreme end, you can create animations, classes, and functions, and in the least, you can add simple browser interactivity on the webpage.

``` html
<script>
document.getElementById("intro").innerHTML = "This paragraph includes
introductory information regarding the Martial Doomsday.";
</script>
```

 For this to work, like CSS, we need HTML. Suppose this is the HTML:

``` html
<p id="intro">Hello!</p>
```

 Now, the "inner HTML" of this block will be replaced with the text we choose via the script. So, on the browser screen, the paragraph with the ID intro will show "This paragraph includes introductory information regarding the Martial Doomsday." instead of a Hello, even if the HTML says it should say Hello.

So, in essence, JavaScript targets HTML (via DOM, which you will learn about later) and manipulates it or its content. Further, JavaScript is used to add a layer of behavior or interaction, like showing confirm messages when you opt to reload or close a tab, displaying pop-up windows, etc.

JavaScript has more power than CSS or HTML, and consequently, it takes more time to be mastered.

## Getting online

Now that you're acquainted with HTML, CSS, and JavaScript, it's time to get online! Although you can create an `.html` file on your computer to do web designing, getting online is the most interesting part.

For starters, you don't have to buy domains or hosting, we'll start with some free service. We'll pick biz.nf for this purpose. It comes with 250MB space, a webmail, and FTP access. The URL is <http://www.biz.nf/>.

First, let's make a few things clear:

-   This service will give you some "web space". That means you'll have some space rented on someone's server. This service is called website hosting. By doing this, your website will get online and could be viewed by other computers too.

-   You'll need to establish a connection to the server in order to upload your files, so that they're online. This connection cannot be establised by web. It needs a file-transfer protocol (FTP) client. We recommend installing FileZilla, the most popular and free FTP client that supports Windows, Mac, and Linux distributions too.

-   You'll basically upload files (generally `.html`, `.css`, `.js` or images) to the server via the FTP client. Once successfully uploaded, they can be viewed by the public by pointing to your domain.

So, you ready? Good.

First, make an account on biz.nf. Here's the URL again: <http://www.biz.nf/>.

Second, install FileZilla. The URL is <https://filezilla-project.org/download.php?type=client>.

Now, before going to the third step, make sure that you have the files you'll upload! The HTML file is the most important, and **be sure to rename it to `index.html`** otherwise it won't open on the server!

You'll learn good techniques of HTML, CSS, JavaScript, and more later on. This section is just meant for getting you started with basic requirements. Now, when you've prepared a good-looking `index.html` file, you can move on to the third step.

Third, upload your file via FileZilla. You'll get detailed instructions of your FTP account (like login details) at the biz.nf website after signing up.

Whenever you feel like looking at your website, just open a web browser and input your domain name! It would be something like mydomain.co.nf. You can open this domain from any computer and the same page will open! Congratulations, you're now online.

Whenever you need to make changes, do so in your local `index.html` file and re-upload it to the server via your FTP client. You'll be surprised to see that all that code has turned into plain text!

However, note that what you'll be currently seeing is an example of basic markup. There's much more to web design. Do you like the content, styling, and behavior of this website? You can make one like this too! Just follow with us through the chapters.

