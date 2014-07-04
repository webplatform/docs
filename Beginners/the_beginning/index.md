{{Page_Title|Part 1: The beginning}}
{{Flags
|State=Almost Ready
|Editorial notes=Truncate content that is duplicate.

Refer to stash pages in http://docs.webplatform.org/wiki/TEST:beginners

Also, maybe get in touch with CommonCraft and ask to embed their video about the World Wide Web http://www.commoncraft.com/video/world-wide-web

* Explains what the Web is and how it works
* Describes what web standards are, and which web technologies you'll be learning about in this course
* Points you to the software you'll need to download in order to complete the rest of the course
|Checked_Out=No
}}
{{Summary_Section|The very first part of our beginner's material gives you some important background on how everything works, and gets you set up and ready to go with web site building.}}
{{Basic Page}}
{{Beginners submenu}}


==Who is this course for?==

Our beginner's guide is written for complete beginners to the world of web site code, who don't know what to learn first, and just need a single point that will lead them in the right direction with confidence. This series of articles guides you through all the real basics of web development, so you can get up to speed relatively quickly, learning just enough to not feel lost and overwhelmed, and get comfortable with the area in general.

If any term is hard to understand, keep a tab opened on the [[Beginners/glossary]].

== What is the web, and how does it work? ==

The Web is a global network of computers on which content can be stored, and accessed at will by anyone with a connection to that network (basically, anyone with an internet service and a computer of some kind that can connect to that service). Most computers in the network merely consume information from other places (also know as '''clients'''), whereas others can consume information from other places '''and''' send information to other computers that ask for it ('''servers'''.)

[INCLUDE A NICE SIMPLE IMAGE OF A SERVER SURROUNDED BY CLIENT MACHINES, AND SOME ARROWS AND CAPTIONS TO INDICATE CLIENTS REQUESTING A WEB PAGE, AND THE SERVER SENDING THE WEB PAGE TO THE CLIENTS TO DISPLAY?]
  
The technology that the Web runs on top of has its roots in an old US military project from the 1960s called ARPANET, but the Web really came into existance when [http://w3.org/People/#timbl Tim Berners-Lee], generally credited as being the creator of the Web, created a document management system in the early 90s in which you could put links between documents and add other features besides. It also included a central computer (known as a server) for serving the documents to other computers in the network, and a program for displaying the documents to the system's users (which was in effect the world's first Web browser — called WorldWideWeb).

Find more about the web's history and origins in [[concepts/internet and web/the history of the web|The history of the Web]]

The main components which allow us to access the Web are:

* '''Web Servers''': Computers who answers to requests made by the clients
* '''Client''': Software on a computer that makes requests to servers (i.e. a web browser)
* '''Hypertext''': A reference to something (an image, another document) somewhere else on the Internet. A text link is also know as an hyperlink.
* '''DNS''': A set of servers communicating together databases of Internet’s way to refer to another computer into human words
* '''The Internet''': A network of computers. The Web and Emails are two of many others.

'''NOTE''' All the common terms are described in [[Beginners/glossary]]

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
{{Notes_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}