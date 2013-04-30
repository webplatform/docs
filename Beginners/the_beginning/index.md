{{Page_Title|Part 1: The beginning}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|The very first part of our beginner's material:

* Explains what the Web is and how it works
* Describes what web standards are, and which web technologies you'll be learning about in this course
* Points you to the software you'll need to download in order to complete the rest of the course
}}
{{Basic Page}}
==Who is this course for?==

Our beginner's guide is written for complete beginners to the world of web site code, who don't know what to learn first, and just need a single point that will lead them in the right direction with confidence. This series of articles guides you through all the real basics of web development, so you can get up to speed relatively quickly, learning just enough to not feel lost and overwhelmed, and get comfortable with the area in general.

If you are already experienced in web development, then we would recommend that you start on the [[Main_Page|WPD main page]].

==What is the web, and how does it work?==

The Web is a global network of computers on which content can be stored, and accessed at will by anyone with a connection to that network (basically, anyone with an internet service and a computer of some kind that can connect to that service). Most computers in the network merely consume information from other places (also know as '''clients'''), whereas others can consume information from other places '''and''' send information to other computers that ask for it ('''servers'''.)

[INCLUDE A NICE SIMPLE IMAGE OF A SERVER SURROUNDED BY CLIENT MACHINES, AND SOME ARROWS AND CAPTIONS TO INDICATE CLIENTS REQUESTING A WEB PAGE, AND THE SERVER SENDING THE WEB PAGE TO THE CLIENTS TO DISPLAY?]
  
The technology that the Web runs on top of has its roots in an old US military project from the 1960s called ARPANET, but the Web really came into existance when Tim Berners-Lee, generally credited as being the creator of the Web, created a document management system in the early 90s in which you could put links between documents and add other features besides. It also included a central computer (known as a server) for serving the documents to other computers in the network, and a program for displaying the documents to the system's users (which was in effect the world's first Web browser — called WorldWideWeb).

Find more about the web's history and origins in [[concepts/internet and web/the history of the web|The history of the Web]]

The main components which allow us to access the Web are:

<ul>
<li><p>Web servers: The computers on which web sites are stored, ready for delivery to those who want to look at them.</p></li>
<li><p>Client: Any computing device, such as your laptop or mobile phone, that can be used to connect to and draw content from the web. Your device uses an application (usually a web browser) to '''request''' a web site/other data from a server; the server then sends back a '''response''', which includes all the information needed for your application to display the web site or other data you requested.</p></li>
<li><p>Web Browser: A program installed on a Client allowing it to access and display web sites, thereby allowing you to interact with the Web.</p></li>
<li><p>Networking Protocols: Agreed upon methods by which computers communicate with each other on a network, allowing the many different types of computers on the Web to talk to each other.  The term HTTP, for instance, means Hyper Text Transfer Protocol and tells your browser how to interface with the network to access information stored on the Web..</p></li>
<li><p>Transmission Protocols: The various agreed upon methods for transporting data around the Web, the most common being FTP, File Transfer Protocol.</p></li>
<li><p> DNS (Domain Name Server): This is essentially an address book for the Web that links common names to the numerical addresses at which all Web sites are stored. All Web sites are actually located at numerical addresses of the form ###.###.###.### called '''IP addresses'''. Domain Name Servers associate these addresses with domain names, so they are easier to handle for humans. So for example, the IP address of google.co.uk is 173.194.66.94 — try typing it in and you'll see we're right — but google.co.uk is far easier to remember!</p></li>
<li><p>Web Technologies: these are the different types of code that web developers use to create web sites. When a web site is requested from a server by a web browser, the data that is sent back to the web browser will consist of a series of files containing various information such as the text you want to show on the web page, the styles that text should have, etc. This is then read by the web browser, which assembles the files into a complete web page. </p></li>
</ul>

[INSERT IMAGE OF TOWN AND CITY CONNECTED BY ROAD, WITH DELIVERY VAN GOING ALONG ROAD TOWARDS TOWN. I'D LIKE IT TO EXPRESS SOMETHING LIKE THE FOLLOWING: Imagine the Web as being like a series of towns and cities connected by roads. One town (the client computer) wants to get a supply of chocolate (web site) from the awesome chocolatier in the city. So the town's mayor (web browser) writes a letter (web request) to send to the chocolatier in the city. The town's mayor has the address of the chocolatier (domain name), but is not sure how to actually get there, so she gives it to the postman, and he takes it there (this is basically what the Domain Name Server does when it is given a domain name). The city is happy to give the town some of its chocolate supply from the chocolatier, so it sends a delivery van full over right away (the code files, written using web standards), travelling by the main road (the transmission protocol). Once it gets to the town, the mayor distributes the chocolate to all her townsfolk (displays the web page), and everyone is happy (users are easy to please).]

This may sound complicated, but most of this is done transparently, without you having to worry about it. As a beginning web developer, the only part you have to worry about is the web technologies.

Read [[concepts/internet and web/how does the internet work|How does the Internet work?]] for more information.

==What are web standards?==

Web standards are the technologies that we use to build web pages; there are a number of different ones, but this material will address only three:

<ul>
<li><p>'''Hypertext Markup Language (HTML)''': This language is used to structure your data and give it meaning. Just like a school paper — with a cover page, table of contents, introduction, body, conclusion and bibliography — HTML code is used to separate blocks of information (such as a heading, paragraph, bulleted list, table, or definition) that can be manipulated and formated (via CSS, Cascading Style Sheets) in their own particular manner.  Probably the most important part of this is the Hypertext of HTML.  HTML defines how links operate, both within documents and to any other place accessible on the Web.</p>

<p>[INSERT IMAGE OF HTML ELEMENTS AND WHAT THEY CREATE ON THE RENDERED PAGE, SOMETHING LIKE I'VE SHOWN BELOW. ALSO INCLUDE HOUSE OR WALL JUST SHOWING THE BARE ROOF AND BRICKWORK] </p>

<pre>HTML:

&lt;h1&gt;The title of my story&lt;/h1&gt;
&lt;p&gt;It was a dark and stormy night.
Somewhere, an owl hooted.&lt;/p&gt;</pre>

renders as

=The title of my story=
<p>It was a dark and stormy night. Somewhere, an owl hooted.</p>

</li>


<li><p>'''Cascading Style Sheets (CSS)''': This language is used to style your content and position it on the page. For example, if you wanted to  make the text of your paragraphs red, and move them all downwards by 2 centimeters on a background of skulls and a border that looked like a cemetery fence, you would do that with CSS. In our paper analogy, CSS provides the instructions to make the paper look nice — centering the title, making the headings bold and so forth.</p>

<p>[INSERT IMAGE OF CSS AND HTML BEING ADDED TOGETHER TO PRODUCE SOME STYLED TEXT, SOMETHING LIKE I'VE SHOWN BELOW. ALSO INCLUDE HOUSE IMAGE THAT BUILDS ON THE LAST ONE, SHOWING THE HOUSE NOW DECORATED WITH PAIN AND NICE COLOURED TILES?] </p>

=The title of my story=
<p>It was a dark and stormy night. Somewhere, an owl hooted.</p>

<p>+</p>

<pre>CSS:

h1 { color: blue; }
p { color: red; }</pre>

<p>results in</p>

<h1 style="color: blue">The title of my story</h1>
<p style="color: red">It was a dark and stormy night. Somewhere, an owl hooted.</p>

</li>

<li><p>'''JavaScript''': This language is used to add dynamic functionality to your web page. This is actually another computer language called by HTML code to provide further functionality.  For example, Javascript could help you make a pop-up dialog box appear when you click on a paragraph to tell you how many letters it contains.  Going back to the paper, it could help you render your data as a graph or pie chart.</p></li>

<p>[INSERT IMAGE OF CSS AND HTML AND JAVASCRIPT BEING ADDED TOGETHER TO PRODUCE SOME STYLED TEXT WITH SOME FUNCTIONALITY, LIKE A POPUP WINDOW OVER THE TOP OF THE PARAGRAPH SHOWING HOW MANY CHARACTERS THE PARAGRAPH CONTAINS. ALSO INCLUDE HOUSE IMAGE THAT BUILDS ON THE LAST ONE, SHOWING THE DECORATED HOUSE WITH SOME COOL FUNCTIONALITY ADDED. HOW ABOUT A SATELLITE DISH ON THE ROOF, AND A WALL MOUNTED TV SEEN THROUGH THE WINDOW?] </p>

<h1 style="color: blue">The title of my story</h1>
<p style="color: red">It was a dark and stormy night. Somewhere, an owl hooted.</p>

<p>+</p>

<pre>JavaScript:

var paragraph = document.getElementsByTagName('p')[0];
paragraph.onclick = function() {
  alert("The length of this paragraph is " + paragraph.innerHTML.length + " characters.");
}</pre>

<p>results in</p>

<h1 style="color: blue">The title of my story</h1>
<p style="color: red" onclick="alert("The length of this paragraph is " + this.innerHTML.length + " characters.");">It was a dark and stormy night. Somewhere, an owl hooted.</p>

</li>
</ul>

We will expand on these in the next article and get you started with some coding!

Read [[concepts/internet and web/the web standards model|The web standards model]] for more details on the why and what of web standards.


==The tools of the trade==

Now we'll look at the actual tools you'll be using to build web sites and put them online for others to look at. In this course, you'll be writing a lot of code, and testing it out in web browsers. Before you start, you should at least have the following installed:

One or more modern browsers, to test your code in: 
* [http://www.google.com/chrome Chrome]
* [http://www.mozilla.org/en-US/firefox/new/ Firefox]
* [http://windows.microsoft.com/ie Internet Explorer] 
* [http://www.opera.com Opera]
* [http://www.apple.com/safari/ Safari]

A decent text editor, to write your code in. Reasonable free options include:
* [http://bluefish.openoffice.nl/index.html Bluefish] for Linux.
* [http://notepad-plus-plus.org/ Notepad++]
* [http://foicica.com/textadept/ TextAdept]
* [http://www.barebones.com/products/TextWrangler/ Text Wrangler] for Mac
* [http://www.microsoft.com/visualstudio/eng/products/visual-studio-express-for-web Visual Studio Express] for Windows


Go ahead, download and install these now. We'll wait right here.
{{Notes_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}