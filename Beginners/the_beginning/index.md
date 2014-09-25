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
{{:Beginners/Submenu}}

==Who is this course for?==

Our beginner's guide is written for complete beginners to the world of web site code, who don't know what to learn first, and just need a single point that will lead them in the right direction with confidence. This series of articles guides you through all the real basics of web development, so you can get up to speed relatively quickly, learning just enough to not feel lost and overwhelmed, and get comfortable with the area in general.

This particular course's approach is different from most online introductory web development courses because it tries to give you important background information that most web development courses avoid because they're not actually necessary for you to start developing for the Web. However, we think that you should know the basics of how the Web works if you're going to be a web developer.

Also, this course is for front-end web developers. That means we teach you how to create web pages with languages like HTML, CSS, and JavaScript (which we'll explain later). This course is not for back-end web developers, which are developers that host web servers (which we'll also explain later).

If any term is hard to understand, refer to the [[Beginners/glossary|glossary for beginners]].

== What is the Internet and the Web, and how does they work? ==

The Internet is a global network of networks of computers that connects computers from all around the world to each other. The World Wide Web is a web of information connected to each other by links and the Internet. The links point to other websites and the Internet is used to get there. Most computers in the network merely consume information from other places (also know as '''clients'''), whereas others can consume information from other places and send information to other computers that ask for it ('''servers''').

[INCLUDE A NICE SIMPLE IMAGE OF A SERVER SURROUNDED BY CLIENT MACHINES, AND SOME ARROWS AND CAPTIONS TO INDICATE CLIENTS REQUESTING A WEB PAGE, AND THE SERVER SENDING THE WEB PAGE TO THE CLIENTS TO DISPLAY?]

The main components which the Web depends on are:

* '''Web Clients''': Computers that get information from web servers. The most common form of web clients are web browsers which have a good user interface and do not require technical information to use. Browsers make the web open 
* '''Web Servers''': Computers that serve information to web clients.
* '''DNS''': Stands for "Domain Name System."A set of servers communicating together databases of Internet’s way to refer to another computer into human words. DNS turns a domain name like "en.wikipedia.org" and turns it into an IP address "208.80.154.224:80" where the server is located.
* '''Hypertext''': The text of the web, what web servers give to web clients. The text of the web includes many things and has changed over time, but there are two important aspects to the text of the web we shall mention below. You can read a Wikipedia article on hypertext [http://en.wikipedia.org/wiki/Hypertext here].
* '''Hyperlink''': A link that refers to another set of hypertext. If this link refers to a different domain name, the web client will need to use DNS to find the right IP address of the server.
* '''HTTP''': Stands for HyperText Transfer Protocol. The protocol of how web requests from clients and information from web servers should be written so they understand each other.

[INSERT IMAGE OF TOWN AND CITY CONNECTED BY ROAD, WITH DELIVERY VAN GOING ALONG ROAD TOWARDS TOWN. I'D LIKE IT TO EXPRESS SOMETHING LIKE THE FOLLOWING]

Imagine the Web as being like a series of towns and cities connected by roads. One town (the client, a regular web user) wants to get a supply of chocolate (website) from the awesome chocolate maker in the city, so the town's mayor (web browser) writes a letter (web request written in HTTP) to send to the chocolate maker in the city. The town's mayor has the name of the business of the chocolate maker (domain name), but doesn't actually know the address, so they gives it to the postman, and the postman takes it there (DNS uses the domain name and sends the request to the right IP address using the Internet). The chocolate maker is happy to give the town some of its chocolate supply, so it sends a delivery van full over right away (the hypertext of the website, web response packaged in HTTP), travelling by the main road (the Internet). Once it gets to the town, the mayor distributes the chocolate to all her townsfolk (displays the web page), and everyone is happy.

Read [[concepts/internet and web/how does the internet work|How does the Internet work?]] for more information.

This may sound complicated, but most of this is done transparently, without you having to worry about it. As a beginning web developer, the part you have to worry about is the making of the actual chocolate: That is, the website's content. You don't need to worry about the packaging that is HTTP because web servers deal with that. You just need to make the chocolate because you're the chocolate maker, not the delivery van driver. Have fun!

==What are websites made of?==

Remember that in our story, the mayor sent a letter to the chocolate maker and they sent back chocolate. However, web clients and web servers send pieces of text to each other and for the World Wide Web to work, they need to be able to read that text. Because of that, there's an organization called the World Wide Web Consortium, or W3C, that decides how the Web should work with official Web standards. All web clients and web servers are expected to adhere to these standards and also be able to communicate from older web clients and servers somehow. They define how hypertext on the web should be sent with [http://www.w3.org/Protocols/rfc2616/rfc2616.html the HTTP specification].

They also decide how the webpage should be displayed with languages called HTML (which stands for HyperText Markup Language), CSS (which stands for Cascading Style Sheets), and JavaScript. These are the languages you'll be using to structure web pages as a front-end web developer. Websites are made of these languages and used by the web browser to display a webpage. There are specifications for these languages, too, but they're not as straightforward to read as the HTTP specification. That's why we have introductory web development courses like these!

Read [[concepts/internet and web/the web standards model|The web standards model]] for more details on the why and what of web standards.

Just to get you introduced to these languages, we've added descriptions and examples of them below. Enjoy!

==What are the languages of the Web like?==

<p>'''HyperText Markup Language (HTML)''': This language is used to outline the content of your webpage. It gives your webpage a title and content like regular text, styled text such as bold or italics, paragraphs, lists, tables, and more. It also gives your webpages links to other webpages. HTML is made of elements specified by tags like <code>&lt;div&gt;</code> and <code>&lt;p&gt;</code> and these elements have attributes that can change the elements and be used by CSS or JavaScript. A webpage can be simply HTML, but such a webpage would be rather simple, so the languages of CSS and JavaScript are used.</p>

<p>[INSERT IMAGE OF HTML ELEMENTS AND WHAT THEY CREATE ON THE RENDERED PAGE, SOMETHING LIKE I'VE SHOWN BELOW. ALSO INCLUDE HOUSE OR WALL JUST SHOWING THE BARE ROOF AND BRICKWORK] </p>

The following snippet of HTML code:

<pre>&lt;h1&gt;The title of my story&lt;/h1&gt;
&lt;p id = "thisIsAnAttribute"&gt;It was a dark and stormy night.
Somewhere, an owl hooted.&lt;/p&gt;</pre>

results in the following:

<div style="border: 2px solid black;">
<h1>The title of my story</h1>
<p>It was a dark and stormy night. Somewhere, an owl hooted.</p>
</div>

<p>'''Cascading Style Sheets (CSS)''': This language is used to style and position the HTML content. It gives your webpage a clean look and more professionalism and a better user interface along with it: It centers your elements, it gives them background, it gives them color, it puts them into place, and it makes them how they should be. CSS has selectors which select elements to be manipulated by CSS and properties which give the elements all of the things that CSS provides. CSS must be accompanied by HTML to work whatsoever.</p>

<p>[INSERT IMAGE OF CSS AND HTML BEING ADDED TOGETHER TO PRODUCE SOME STYLED TEXT, SOMETHING LIKE I'VE SHOWN BELOW. ALSO INCLUDE HOUSE IMAGE THAT BUILDS ON THE LAST ONE, SHOWING THE HOUSE NOW DECORATED WITH PAIN AND NICE COLOURED TILES?] </p>

The application of the following CSS code to our above snippet:

<pre>h1 {
    color: blue;
}
p {
    color: red;
}</pre>

results in the following:

<div style="border: 2px solid black;">
<h1 style="color: blue">The title of my story</h1>
<p style="color: red">It was a dark and stormy night. Somewhere, an owl hooted.</p>
</div>

<p>'''JavaScript''': This language is used to add dynamic functionality to your web page. It provides the majority of the interactions in webpages, aside from simple things like certain elements such as textboxes that are from HTML. JavaScript leads to things happening to the webpage when things are clicked or a key is pressed. JavaScript is a scripting language that is <i>very</i> powerful and actually makes webpages a bit dangerous, so be careful with it! Even though JavaScript was originally for the Web, JavaScript is actually used in lots of things other than it, but this course will focus on its application to the Web.</p>

<p>[INSERT IMAGE OF CSS AND HTML AND JAVASCRIPT BEING ADDED TOGETHER TO PRODUCE SOME STYLED TEXT WITH SOME FUNCTIONALITY, LIKE A POPUP WINDOW OVER THE TOP OF THE PARAGRAPH SHOWING HOW MANY CHARACTERS THE PARAGRAPH CONTAINS. ALSO INCLUDE HOUSE IMAGE THAT BUILDS ON THE LAST ONE, SHOWING THE DECORATED HOUSE WITH SOME COOL FUNCTIONALITY ADDED. HOW ABOUT A SATELLITE DISH ON THE ROOF, AND A WALL MOUNTED TV SEEN THROUGH THE WINDOW?]</p>

The application of the following JavaScript code to our above snippet:

<pre>var paragraph = document.getElementsById("thisIsAnAttribute");
paragraph.onclick = function() {
  alert("The length of this paragraph is " + paragraph.innerHTML.length + " characters.");
}</pre>

results in the following (click the paragraph!):

<div style="border: 2px solid black;">
<h1 style="color: blue">The title of my story</h1>
<p style="color: red" onclick='alert("The length of this paragraph is " + this.innerHTML.length + " characters.");'>It was a dark and stormy night. Somewhere, an owl hooted.</p>
</div>

We will expand on these languages in this course and get you started coding in the next article!
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