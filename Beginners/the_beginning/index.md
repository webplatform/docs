{{Page_Title|Part 1: The beginning}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|The very first part of our beginner's material gives you some important background on how everything works, and gets you set up and ready to go with web site building.}}
{{Basic Page}}
==Who is this course for?==

Our beginner's guide is written for complete beginners to the world of web site code, who don't know what to learn first, and just need a single point that will lead them in the right direction with confidence. This series of articles guides you through all the real basics of web development, so you can get up to speed relatively quickly, learning just enough to not feel lost and overwhelmed, and get comfortable with the area in general.

If you are already experienced in web development, then we would recommend that you start on the [[Main_Page|WPD main page]].

==What is the web, and how does it work?==

The Web is a global network of computers on which content can be stored, and accessed at will by anyone with a connection to that network (basically, anyone with an internet service and a computer of some kind that can connect to that service). Most computers in the network merely consume information from other places (also know as '''clients'''), whereas others can consume information from other places '''and''' send information to other computers that ask for it ('''servers'''.)

[INCLUDE A NICE SIMPLE IMAGE OF A SERVER SURROUNDED BY CLIENT MACHINES, AND SOME ARROWS AND CAPTIONS TO INDICATE CLIENTS REQUESTING A WEB PAGE, AND THE SERVER SENDING THE WEB PAGE TO THE CLIENTS TO DISPLAY?]
  
The technology that the Web runs on top of has its roots in an old US military project from the 1960s called ARPANET, but the Web really came into existance when Tim Berners-Lee, generally credited as being the creator of the Web, created a document management system in the early 90s in which you could put links between documents and add other features besides. It also included a central computer (known as a server) for serving the documents to other computers in the network, and a program for displaying the documents to the system's users (which was in effect the world's first Web browser — called WorldWideWeb).

Find more about the web's history and origins in [[the_history_of_the_web|The history of the Web]]

The main components of the Web are as follows:

# A web server: This is a computer where web sites are stored, ready for delivery to those who want to look at them
# Client computers: Users of these computers can use a web browser to '''request''' a web site from a server, at which point it will be sent (a '''response''') to the user's computer and displayed inside the web browser. 
# A web browser: As indicated above, this is a program installed on your computer that accesses and displays web sites for you, allowing you to interact with the Web.
# A means of transporting data around the Web: this is generally referred to as a '''transmission protocol''', a system that handles transporting data around the Web.
# A DNS (Domain Name Server): this is basically like an address book for the Web. The real locations that web sites live at, on web servers, are represented by complicated strings of numbers called '''IP addresses'''. Domain Name Servers associate these addresses with domain names, so they are easier to handle for humans. So for example, the IP address of google.co.uk is 173.194.66.94 — try typing it in and you'll see we're right — but google.co.uk is far easier to remember!
# Web standards: these are the different types of code that web developers use to create web sites. When a web site is requested from a server by a web browser, the data that is sent back to the web browser will consist of a series of files containing various information such as the text you want to show on the web page, the styles that text should have, etc. This is then read by the web browser, which assembles the files into a complete web page. 

[INSERT IMAGE OF TOWN AND CITY CONNECTED BY ROAD, WITH DELIVERY VAN GOING ALONG ROAD TOWARDS TOWN] 

Let's look at an analogy, to make this easier. Imagine the Web as being like a series of towns and cities connected by roads. One town (the client computer) wants to get a supply of chocolate (web site) from the awesome chocolatier in the city. So the town's mayor (web browser) writes a letter (web request) to send to the chocolatier in the city. The town's mayor has the address of the chocolatier (domain name), but is not sure how to actually get there, so she gives it to the postman, and he takes it there (this is basically what the Domain Name Server does when it is given a domain name). The city is happy to give the town some of its chocolate supply from the chocolatier, so it sends a delivery van full over right away (the code files, written using web standards), travelling by the main road (the transmission protocol). Once it gets to the town, the mayor distributes the chocolate to all her townsfolk (displays the web page), and everyone is happy (users are easy to please).

This may sound complicated, but most of this is done transparently, without you having to worry about it. As a beginning web developer, the only part you have to worry about is the Web standards.

Read [how_does_the_internet_work|How does the Internet work?] for more information.

==What are web standards?==

Web standards are the technologies that we use to build web pages; there are a number of different ones, but in this short article series we will only really be talking about three:

* Hypertext Markup Language (HTML): This language is used to structure your data and give it meaning. For example, if you wanted to break your content into three paragraphs and a bulleted list. Consider an architectural analogy — if a web page were like a building, then HTML would be like the foundations, brickwork and roof. Having a solid structure is essential to both web pages and buildings.

[INSERT IMAGE OF HTML ELEMENTS AND WHAT THEY CREATE ON THE RENDERED PAGE, SOMETHING LIKE I'VE SHOWN BELOW. ALSO INCLUDE HOUSE OR WALL JUST SHOWING THE BARE ROOF AND BRICKWORK] 

<pre>HTML:
&lt;h1&gt;The title of my story&lt;/h1&gt;
&lt;p&gt;It was a dark and stormy night.
Somewhere, an owl hooted.&lt;/p&gt;
    |
    | renders as
    |
<div style="font-size: 30px">The title of my story</div>
<div>It was a dark and stormy night. Somewhere, and owl hooted.</div></pre>



* Cascading Style Sheets (CSS): This language is used to style your content and position it on the page. For example, if you wanted to  make the text of your paragraphs red, and move them all downwards by 2 centimeters. In our building analogy, CSS would be like the decorations using to make the building look nice — the plaster, paint, wallpaper, doorhandles and coving.

[INSERT IMAGE OF CSS AND HTML BEING ADDED TOGETHER TO PRODUCE SOME STYLED TEXT, SOMETHING LIKE I'VE SHOWN BELOW. ALSO INCLUDE HOUSE IMAGE THAT BUILDS ON THE LAST ONE, SHOWING THE HOUSE NOW DECORATED WITH PAIN AND NICE COLOURED TILES?] 

* JavaScript: This language is used to add dynamic functionality to your web page. So for example, if you wanted to make it so that when you click on each paragraph using the mouse, a pop-up dialog box appears, telling you how many letters each paragraph contains. In our building analogy, JavaScript would be like cool functionality you have inside the house, like the cooker, flatscreen TV, power shower, robot butler...

[INSERT IMAGE OF CSS AND HTML AND JAVASCRIPT BEING ADDED TOGETHER TO PRODUCE SOME STYLED TEXT WITH SOME FUNCTIONALITY, LIKE A POPUP WINDOW OVER THE TOP OF THE PARAGRAPH SHOWING HOW MANY CHARACTERS THE PARAGRAPH CONTAINS. ALSO INCLUDE HOUSE IMAGE THAT BUILDS ON THE LAST ONE, SHOWING THE DECORATED HOUSE WITH SOME COOL FUNCTIONALITY ADDED. HOW ABOUT A SATELLITE DISH ON THE ROOF, AND A WALL MOUNTED TV SEEN THROUGH THE WINDOW?] 

We will expand on these in the next article and get you started with some coding!

Read [the_web_standards_model|The web standards model] for more details on the why and what of web standards.


==The tools of the trade==

Now we'll look at the actual tools you'll be using to build web sites and put them online for others to look at. In this course, you'll be writing a lot of code, and testing it out in web browsers. Before you start, you should at least have the following installed:

* The newest browsers you are able to install, to test your code in. If you don't have them already, grab them from the homepages of [http://www.google.com/chrome Chrome], [http://www.mozilla.org/en-US/firefox/new/ Firefox], and [http://www.opera.com Opera]. If you are on Windows please make sure [http://windows.microsoft.com/en-GB/internet-explorer/products/ie/home Internet Explorer] is up-to-date; on Mac OS please make sure [http://www.apple.com/safari/ Safari] is up-to-date.
* A decent text editor, to write your code in. Reasonable free options are [http://foicica.com/textadept/ TextAdept], [http://notepad-plus-plus.org/ Notepad++], [http://www.microsoft.com/visualstudio/eng/products/visual-studio-express-for-web Visual Studio Express] for Windows, [http://www.barebones.com/products/TextWrangler/ Text Wrangler] for Mac, and [http://bluefish.openoffice.nl/index.html Bluefish] for Linux.

Download and install these now.
{{Notes_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}