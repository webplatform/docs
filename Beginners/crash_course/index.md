{{Page_Title|Part 2: A crash course in web site code}}
{{Flags
|State=In Progress
|Editorial notes=There are plenty of notes and idea but all incomplete.

Editorial notes:
* Explain what HTML, CSS, and JavaScript are, show how to create some really trivially simple examples
* Show what a simple site structure might look like
* Go through simple HTML anatomy
* Show what an HTML page looks like, explain its purpose. Show head, body, title, and a few other things
* Add some really simple bits to it. headings and paragraphs, bullet points, an image maybe
* explain simple common gotchas - quote problems, incorrect paths, bad nesting, missing out attributes
* Next, go through simple CSS anatomy
* Show how simple CSS selectors work
* Go through how to apply CSS to HTML - 3 ways
* explain simple CSS gotchas - bad pathing, missing semi colons, missing attributes, incorrect adding of classes to elements (I've seen people try to use <class="heading">content</class>) 
* next, show simple javascript anatomy and explain how it works
* show some really simple JS use
* explain simple JS gotchas, and explain that it needs quite a bit more understanding than HTML or CSS. But it has more power.
* Take the user through the steps towards getting web space (use a free service, such as http://www.biz.nf/), and get them to set up their FTP, and upload their simple files.
* Show them how they can now view their files on another computer.
|Checked_Out=No
}}
{{Summary_Section|This part assumes you want to build a website with almost no prior knowledge. It will start on HTML and CSS to allow you to do that right away. Obviously, we can't teach it all at once, so we will start with certain basic features we expect you might be interested in, and build on from there.

If you have terms you don’t understand, you can see the [[Beginners/glossary]] section.

You will quickly find that once you get the hang of how this works, you will be able to figure out how to add the features you want just by looking at the HTML and CSS code and applying that code to your site, or an offline test site.
}}
{{Basic Page}}
<!--
Note to contributors: This part provides a very quick "hands dirty" session on HTML, CSS and JavaScript. This page is a rework from the original author, David Herz and hopefully follows the spirit of his idea.

We're not giving all the information - we are just trying to get the reader comfortable and give him/her a sense of achievement to begin with, before they get bored by all the details ;-)

-->
{{:Beginners/Submenu}}

== HTML, CSS, and JavaScript ==

We're assuming you've had your general introduction with HTML, CSS, and JavaScript at the former article of this series. Here we're going to get a bit advanced.

The main file that's uploaded to a server is the HTML file, which includes all the content, directions for servers and browsers, and links to other files (like stylesheets or script files). The HTML markup is used to render text in a specific way by the browser.

Suppose you have a book in which you use a yellow highlighter pen to highlight main concepts. You further use a black ball point pen to circle around the things you find confusing. You have created a markup language of your own. Suppose your language grows inflated with more conventions and at the same time, becomes popular. Now, you need a resource that contains the descriptions of those, right? Like this:

* '''Yellow highlight''': main concept
* '''Blue underline''': definition of a main concept
* '''Black encircle''': difficult or confusing concept

and so on. HTML is just that. It was created to give markup to scientific documents. So if you wanted to show emphasis, you used <code>em</code>, not a yellow highlight.

CSS is essentially used for styling the elements and portions of the HTML document. Suppose you really need a yellow highlight instead on emphasis. Here's what you'll do:

<syntaxHighlight>
.important {
  background-color: yellow;
}
</syntaxHighlight>

Note that a CSS rule can only target HTML elements. So there needs to be HTML code too!

<syntaxHighlight>
<p class="important">
 Heisenberg's Uncertainty Principle
</p>
</syntaxHighlight>

We gave the <code>p</code> (which means a paragraph) a '''class''' of "important". A class is a reusable object, that's why you can give something else a class of important too and thus reuse the same style.

JavaScript is pretty dangerous and notorious. We cannot explicitly elaborate on that.

So, in essence, the code becomes like this:

'''HTML''':
<syntaxHighlight>
<p class="important">
 Heisenberg's Uncertainty Principle: Two properties of an object cannot be known for sure at a given instant.
</p>
<p id="alphaParticle">
 Alpha-Particle Bombarding Experiment: It was carried out to figure that there's lot of empty space in an atom.
</p>
<p class="important">
 M-Theory: According to this more robust form of string theory, there are actually 11 dimensions in the universe!
</p>
</syntaxHighlight>

'''CSS''':
<syntaxHighlight>
.important {
  background-color: yellow;
}
#alphaParticle {
 background-image: url(electron.png);
}
</syntaxHighlight>

As you can easily understand, we styled the important class and also the '''#alphaParticle". What's that? Well, the hash denotes an ID. An ID is different from a class because it can only be assigned to one HTML element.

== An HTML document ==

This is a basic HTML document.

<syntaxHighlight>
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
</syntaxHighlight>

Note that there are essentially two types of markings.  

There is the paired <code>&lt;tag-name&gt;tag contents&lt;/tag-name&gt;</code>, which is how we tell the computer to deal with any block of text from a letter to defining the beginning and end of a whole
document.  

Then there is the <code>&lt;tag-name _______________ /&gt;</code> where those are instructions to describe on how to deal with certain situations. The <code>meta</code> are about the server communication. In this particular case, we are saying that the file is written in <code>UTF-8</code> (i.e. a format that supports multiple language characters at once), and <code>link</code> is for asking which file to download along with the HTML document to take care of the visual aspects ("stylesheets"). These stylesheets are a collection of style rules, written in CSS.

== Let's make a website ==

For your first HTML document, please cut and paste the above into a text editor of your choice and save it as <tt>example.html</tt>, but leave the file opened.

'''Important''': Make sure the file-extension is appended to <tt>.html</tt>. In Windows, you might have to go to Tools>File Options>Show Extensions of Common Files before this works.

Now go to your browser, choose Open, open this file and see what happens and leave this page open too.

Now add the following (or whatever other text you want) in your editor.  Why not put it after the paragraph that's already there:

<syntaxHighlight>
<h2>Your Second-Level Heading Here</h2>
<p>Write something <em>add emphasis</em> finish your paragraph and add a list along with maybe?</p>
<ul>
	<li>List Item One.</li>
	<li>List Item Two.</li>
</ul>
</syntaxHighlight>

Save it.

Go back to your browser and refresh the page and notice what's changed.

Did you see we entered a list there too? A list is a cool part of a webpage. The <code>ul</code> tells the browser that an "unordered list" has begun. For an ordered list (with numbers or alphabets), you'll need an <code>ol</code>.

Now play a little by trying some other stuff (nothing is better than experimentation when it comes to learning!)
* <code>h3</code> instead of <code>h2</code>, or <code>h4</code>, <code>h5</code>, <code>h6</code>; those are [[html/elements/hn|headlines elements]] to differentiate titles from body text.
* Instead of <code>em</code>, try <code>strong</code>, <code>sup</code>, <code>sub</code>, or the <code>b</code> [[html/elements|tags]] in the same way.

Want to call another document?

Create a file beside <tt>example.html</tt>, and call it <tt>example2.html</tt>. Empty the <code>body</code> tag, and just write something inside the <code>body</code> tag.

We will call <tt>example2.html</tt>, from our <tt>example.html</tt> sandbox document. Add this line:

<syntaxHighlight>
<a href="example2.html" title="Another HTML file">Calling example2</a>
</syntaxHighlight>

Did you notice how we sneaked up the <code>a</code> there? That's an anchor. It anchors, or holds, a URL (uniform resource locator), or more commonly a link, to a separate place (which can be a file, another webpage, an email address, etc.). The <code>href</code> attribute tells the URL of the target file.

Now, whenever you click on this link, you'll be taken to <tt>example2.html</tt> instantaneously. Congratulations, you learned something that's pretty much the cornerstone of the web!

== Some other things you need to take care of ==
To be a good web-coder, you need to learn some good practices.

* '''Right use of quotes''': Quotes are used to quote something, somebody, or some saying. But some people use them for style and presentational purposes. Please don't do that. A <code>q</code> tag denotes a quote.

* '''Get your paths right''': Many beginning coders face problems when they wrongfully enter paths. Suppose you have an image one directory up named <tt>house.jpg</tt>. When you call it within the page, you'll need a code like this: <code>&lt;img src="../house.jpg"&gt;</code>. If you have some knowledge of UNIX operating systems, you'll understand what's going on here. Actually, we're telling the browser that the "path" of the picture is at "../", which means one directory up. Besides this, there are many other problems in file paths, that's why you should double-check them and URLs, if any, and inspect them when something goes wrong in the webpage.

* '''Avoid bad nesting''': It's a common problem to do nesting in an illogical and confusing manner. Always try to maintain the hierarchy. A small example will be this:

<syntaxHighlight>
<div>
  <p>To-Do List</p>
    <ul>
      <li>Destroy Mars.</li>
      <li>Conquer Atlantis.</li>
      <li>Enslave all Moon citizens.</li>
      <li>Eat solar plasma in the new Solar Heights.</li>
    </ul>
  </p>
</div>
</syntaxHighlight>

Good nesting allows you to see what's going on and a logical hierarchy is always good, like for the time when others debug or check your code, or when you do the same after some months.

* '''Don't miss out the attributes''': HTML attributes are very important and they make a webpage and entire websites more meaningful and suitable for screen readers and other accessibility devices. Some attributes you should never miss out are: <code>lang</code> (for telling the browser which language the webpage is written in), <code>title</code> (for specifying the name of the browser window/tab and naming elements), <code>href</code> (used mostly in links, if you skip it, the link won't point to anywhere), and <code>alt</code> (the alt attribute is used to display/read text content when an HTML element, like an image, cannot be loaded).

== Simple CSS anatomy and application ==
CSS is a detailed language, and for its graceful implementation, we've created the [[Beginners/css|Part 5]], but here, you should learn about the simple anatomy of CSS and applying it on HTML elements.

CSS is a language for styling the HTML elements we create. It includes sets of rules. Suppose we need to color all paragraphs silver. These will be the code piece for this:

'''HTML''':
<syntaxHighlight>
<h1>How to destroy Mars</h1>
<p>It'll be really bad to do this, as the world would be very disappointed, 
but for the sake of darkness, we must perform this deed.</p>
<p>First, prepare a rocket with infinite fuel. Check this 
page again when you're done. Goodbye.</p>
</syntaxHighlight>

'''CSS''':
<syntaxHighlight>
p {
  color: silver;
}
</syntaxHighlight>

The rule will color all paragraphs (we have two) silver, but will leave everything else the way it's meant to be. '''Note''': We don't recommend blowing up Mars.

The <code>p</code> we used in the CSS is a selector. Selectors select an HTML element and then apply the required styles to it. No selection: no styles applied.

== JavaScript primer ==

JavaScript is a scripting language that works much like your common programming languages. At the extreme end, you can create animations, classes, and functions, and in the least, you can add simple browser interactivity on the webpage.

<syntaxHighlight>
<script>
document.getElementById("intro").innerHTML = "This paragraph includes 
introductory information regarding the Martial Doomsday.";
</script>
</syntaxHighlight>

For this to work, like CSS, we need HTML. Suppose this is the HTML:

<syntaxHighlight>
<p id="intro">Hello!</p>
</syntaxHighlight>

Now, the "inner HTML" of this block will be replaced with the text we choose via the script. So, on the browser screen, the paragraph with the ID intro will show "This paragraph includes introductory information regarding the Martial Doomsday." instead of a Hello, even if the HTML says it should say Hello.

So, in essence, JavaScript targets HTML (via DOM, which you will learn about later) and manipulates it or its content. Further, JavaScript is used to add a layer of behavior or interaction, like showing confirm messages when you opt to reload or close a tab, displaying pop-up windows, etc.

JavaScript has more power than CSS or HTML, and consequently, it takes more time to be mastered.

== Getting online ==
Now that you're acquinted with HTML, CSS, and JavaScript, it's time to get online! Although you can create a <tt>.html</tt> file on your computer to do web designing, but getting online is the most interesting part.

For starter, you don't have to buy domains or hosting, we'll start with some free service. We'll pick biz.nf for this purpose. It comes with 250MB space, a webmail, and FTP access. The URL is http://www.biz.nf/.

First, let's make a few things clear:

* This service will give you some "web space". That means you'll have some space rented on someone's server. This service is called website hosting. By doing this, your website will get online and could be viewed by other computers too.

* You'll need to establish a connection to the server in order to upload your files, so that they're online. This connection cannot be establised by web. It needs a file-transfer protocol (FTP) client. We recommend installing FileZilla, the most popular and free FTP client that supports Windows, Mac, and Linux distributions too.

* You'll basically upload files (generally <tt>.html</tt>, <tt>.css</tt>, <tt>.js</tt> or images) to the server via the FTP client. Once successfully uploaded, they can be viewed by public by pointing to your domain.

So, you ready? Good.

First, make an account on biz.nf. Here's the URL again: http://www.biz.nf/.

Second, install FileZilla. The URL is https://filezilla-project.org/download.php?type=client.

Now, before going to the third step, make sure that you got the files you'll upload! The HTML file is the most important, and '''be sure to rename it to <tt>index.html</tt>''' otherwise it won't open on the server!

You'll learn good techniques of HTML, CSS, JavaScript, and more later on. This section is just meant for getting you started with basic requirements. Now, when you've prepared a good-looking <tt>index.html</tt> file, you can move on to the third step.

Third, upload your file via FileZilla. You'll get detailed instructions of your FTP account (like login details) at the biz.nf website after signing up.

Whenever you feel like looking at your website, just open a web browser and input your domain name! It would be something like mydomain.co.nf. You can open this domain from any computer and the same page will open! Congratulations, you're now online.

Whenever you need to make changes, do so in your local <tt>index.html</tt> file and re-upload it to the server via your FTP client. You'll be surprised to see that all that code has turned into plain text!

However, note that what you'll be currently seeing is an example of basic markup. There's much more to web design. Do you like the content, styling, and behavior of this website? You can make one like this too! Just follow with us through the chapters.
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}