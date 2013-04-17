{{Page_Title|Part 2: A crash course in web site code}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|This part of our beginners course aims to provide you with a very quick and dirty introduction to coding a web page, so you can get comfortable with what it takes.}}
{{Basic Page}}
Note to authors: this part provides a very quick "hands dirty" session on HTML, CSS and JavaScript. We're not giving all the information - we are just trying to get the reader comfortable and give him/her a sense of achievement to begin with, before they get bored by all the details ;-)

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

<pre>Notes from David Herz

More of my proposed text:

This course assumes you want to build a web site.  It will start on HTML and
CSS to allow you to do that right away.  Obviously, we can't teach it all at
once, so we will start with certain basic features we expect you might be
interested in, and build on from there.  You will quickly find that once you
get the hang of how this works, you will be able to figure out how to add
the features you want just by looking at the html and css code tables and
applying that code to your site.  Let's get started.

While you can code on any word processor or the notepad program that came
with your computer, and figure out how to save the file as text and rename
it .html or some silly process like that, you will probably have a more
enjoyable experience if you download a program like notepad++ (free at
_whatever the site is_) for coding purposes (we call this an editor).

Link to next page to start coding; next page:

I take your example from the The web standards model — HTML CSS and
JavaScript page:

This is a basic HTML document.

<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="utf-8">
 <title>The Title Bar Title Goes Here</title>
 <link rel="stylesheet" href="stylename.css" type="text/css"
media="screen">
</head>
<body>
<h1>Headings Go Here</h1>
<p>This designates a paragraph
 This is the body of the document, and all your good stuff goes here. </p>
</body>
</html>

Please note there are essentially two types of markings.  There is the
paired <**>text</**>, which is how we tell the computer to deal with any
block of text from a letter to defining the beginning and end of a whole
document.  Then there is the <%%%% _______________> where this block gives
an instruction to the program as to how to deal with certain situations,
such as the meta or link above which tell the computer what character set to
use and what style, respectively, but does not have a closing mark like the
first style.

For your first HTML document, please cut and paste the above into your
editor, and save it as example.html, but leave the document open.  Now go to
your browser, press open, open this file and see what happens.  Leave this
page open too.

Now add the following (or whatever other text you want) in your editor.  Why
not put it after the paragraph that's already there:

<h2>Your second level heading here</h2>
<p>write something <em>add emphasis</em> finish your paragraph </p>

Save it.  Go back to your browser and refresh the page, what happens.  Now
play a little.  Try h3 instead of h2, or h4, h5, h6.  What about h7?
Instead of em, try <strong>more text</strong> or use i in the same way.

You might want to add color.  This is a little more complicated, and for
this we'll have to introduce you to the style sheet, but don't worry that's
what happens next.

As to the code above, I very much think it should be, and our standard mode
for teaching should be, a table with the code on the left, and an
explanation for what each element does on the right.  So take all my
comments below, and pretend they are off to the right.  This way people can
see the code, and get what it does right there.

<!DOCTYPE html> <!this tells the browser what version of HTML it is dealing
with; there are others and we want to make sure there is no confusion.>
<html lang="en"> <!this is how we open every document; the language part is
optional, but makes sure your document doesn't look like gobbledy gook when
someone in Korea opens your document in a browser that defaults to Korean>
 <head> <!required part of every HTML document>
   <meta charset="utf-8">
   <title>Example Page</title>
	<link rel="stylesheet" href="style1.css" type="text/css"
media="screen">
		<!link to style sheet in same directory why this syntax??
		type tells us the type of file, the .css is apparently not
sufficient;
		media tells us to what to apply it, in this case the screen
as we 
		might not want this to print>
	<! or <style>
			style definition
		  </style> allows you to do this in the same document
without consulting
		  the style sheet>
 </head>
 <body>
   <h1>Hello world</h1>
 </body>
</html>

So that's about all I have time for tonight.</pre>
{{Notes_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}