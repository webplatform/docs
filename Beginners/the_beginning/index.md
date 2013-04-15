{{Page_Title|Part 1: The beginning}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|The very first part of our beginner's material gives you some important background on how everything works, and gets you set up and ready to go with web site building.}}
{{Basic Page}}
==Who is this course for?==

The whole of this web site is intended to provide vital information that web developers need to do their job, whether that's teaching new skills, or providing reference material to look up data to help with tasks they are already familiar with. But that's existing developers: the trouble is that most of the material on WebPlatform.org is not for complete beginners to the world of web site code, who don't know what to learn first, and just need a single point that will lead them in the right direction with confidence.

Our beginner's guide was written specifically for this purpose. This series of articles guides you through all the real basics of web development, so you can get up to speed relatively quickly, learning just enough to not feel lost and overwhelmed, and get comfortable with the area in general. Then, after you've gone through this first set of articles, you can then use it as a subject roadmap, going through and learning more about each individual subject to fill in the gaps.

If you are already experienced in web development, then we would recommend that you start on the [[Main_Page|WPD main page]].

==What is the web, and how does it work?==

The Web is a global network of computers on which content can be stored, and accessed at will by anyone with a connection to that network (basically, anyone with an internet service and a computer of some kind that can connect to that service). Most computers in the network merely consume information from other places, whereas others can consume information from other places '''and''' send information to other computers that ask for it.
  
The technology that the Web runs on top of has its roots in an old US military project from the 1960s called ARPANET. This technology was built upon to create the Internet, which first existed as we know it in the late 70s. But there were a few more pieces missing, and these were filled in by Tim Berners-Lee, generally credited as being the creator of the Web, in the late 80s. Berners-Lee, then a research scientist at the CERN laboratories in Switzerland, created a document management system in which you could put links between documents and add other features besides. It also included a central computer (known as a server) for serving the documents to other computers in the network, and a program for displaying the documents to the system's users (which was in effect the world's first Web browser — called WorldWideWeb).

Find more about the web's history and origins in [[the_history_of_the_web|The history of the Web]]

The main components of the Web are as follows:

# A web server: this is a computer where web sites are stored, ready for delivery to those who want to look at them
# Client computers: these are computers with an available internet connection and a web browser installed upon them. Users of these computers can use a web browser to '''request''' a web site from a server, at which point it will be sent (a '''response''') to the user's computer and displayed inside the web browser. 
# A web browser: As indicated above, this is a program installed on your computer that accesses and displays web sites for you, allowing you to interact with the Web.
# A means of transporting data around the Web: this is generally referred to as a '''transmission protocol''', a system that handles transporting data around the Web.
# A Domain Name Server: this is basically like an address book for the Web. The real locations that web sites live at, on web servers, are represented by complicated strings of numbers called '''IP addresses'''. Domain Name Servers associate these addresses with domain names, so they are easier to handle for humans. So for example, the IP address of google.co.uk is 173.194.66.94 — try typing it in and you'll see we're right — but google.co.uk is far easier to remember!
# Web standards: these are the different types of code that web developers use to create web sites. When a web site is requested from a server by a web browser, the data that is sent back to the web browser will consist of a series of files containing various information such as the text you want to show on the web page, the styles that text should have, etc. This is then read by the web browser, which assembles the files into a complete web page. 

[INSERT IMAGE OF TOWN AND CITY CONNECTED BY ROAD, WITH DELIVERY VAN GOING ALONG ROAD TOWARDS TOWN] 

Let's look at an analogy, to make this easier. Imagine the Web as being like a series of towns and cities connected by roads. One town (the client computer) wants to get a supply of chocolate (web site) from the awesome chocolatier in the city. So the town's mayor (web browser) writes a letter (web request) to send to the chocolatier in the city. The town's mayor has the address of the chocolatier (domain name), but is not sure how to actually get there, so she gives it to the postman, and he takes it there (this is basically what the Domain Name Server does when it is given a domain name). The city is happy to give the town some of its chocolate supply from the chocolatier, so it sends a delivery van full over right away (the code files, written using web standards), travelling by the main road (the transmission protocol). Once it gets to the town, the mayor distributes the chocolate to all her townsfolk (displays the web page), and everyone is happy (users are easy to please).

Read [how_does_the_internet_work|How does the Internet work?] for more information.

==Why is the web such a good thing?==

The Web is a wonderful thing for you to learn more about, not only in terms of using it for information, communication, entertainment, etc. but also in terms of developing new content and services for others to use. Here are just a few reasons:

# The Web is free to use, and develop, in terms of both monetary cost and freedom. Yes, some web sites charge for viewing content, some governments try to limit the content their countries view and broadcast, some software you can use to write web site code might cost money to buy, and Wifi providers tend to charge for their services. But the underlying technologies that the web is built on are free for anyone to use and contribute to. But it is possible to access the web for free, and publish your own content on the Web without spending any money, or for minimal costs.
# Web code is quite easy to learn in comparison to other programming environments, so it is easy to get started as a web developer.
# No one company controls the Web, and the development of web technologies, so it is unlikely that the web will die out as a result of a single company's financial or political issues.
# The web is pretty popular. Billions of people use the web, so on publishing a web site you have an instant global market.
# The web community is very passionate and friendly, and they like giving away ideas and code for free. It is easy to get help if you are stuck, meet like-minded people to discuss ideas with, and find code to help speed up your work and learn from.
# The web is designed with universal access in mind - to be accessible by as wide an audience as possible, regardless of circumstances, any disabilities they may have, etc.

==What are web standards?==

To understand what web standards are, let's consider what standards are. If you think about it, there are a large number of standards all around us in the real world, which make life easier. Think about standards for plug sockets, screwdrivers, shoe and dress sizes, traffic lights, icons for maps/signage (such as toilets, hospital, airport), units of measurement, and paper sizes.

Now lets extend this idea to web standards. Web standards are a series of technologies that are defined in giant documents called specifications. These specifications are published by standards bodies (like the [http://www.w3.org/ W3C], which is kind of the web geek version of the [http://www.standardsuk.com/ BSI] or the [http://www.ansi.org/ ANSI]). These specifications are then taken by browser manufacturers (such as Mozilla, Google and Opera) and used to implement support for those technologies in their browsers. Because each browser uses the same specification to implement a standard, that technology should work in the same way across all browsers, and therefore A web site we create should work across all the different browsers you might use to browser the Web, whether it is on Windows PC, Mac, Linux PC, iPhone, Android phone, etc.

Web standards are good because they are developed via cooperation between many different companies in an open, public process. This means that the standards are likely to be created fairly, and not with the interests of a single company in mind. This means that a single company is not able to exert influence over the web in unfair ways by controlling technology implementations, and if one company goes bankrupt, there will be others to carry on the standards work. In addition, many contributors to a technology means that the end product is likely to be richer and better thought out.

Note: Not all technologies found on the web are web standards. Some technologies, such as Flash, are created by a single company and not defined in public specifications. Not being an open standard does not mean a technology is bad, but there are definitely advantages to the open process, as well as disadvantages.

Read [how_does_the_internet_work|How does the Internet work?] for more information.

==What web standards do we use to build the Web?==

There are a number of different technologies that can be used to build web pages; in this short article series we will only really be talking about three:

* Hypertext Markup Language (HTML): This language is used to structure your data and give it meaning. For example, if you wanted to break your content into three paragraphs and a bulleted list.
* Cascading Style Sheets (CSS): This language is used to style your content and position it on the page. For example, if you wanted to  make the text of your paragraphs red, and move them all downwards by 2 centimeters.
* JavaScript: This language is used to add dynamic functionality to your web page. So for example, if you wanted to make it so that when you click on each paragraph using the mouse, a pop-up dialog box appears, telling you how many letters each paragraph contains.

We will expand on these in the next article and get you started with some coding!

Read [the_web_standards_model|The web standards model] for more details on the why and what of web standards.


==The tools of the trade==

Now we'll look at the actual tools you'll be using to build web sites and put them online for others to look at. In this course, you'll be writing a lot of code, and testing it out in web browsers. Before you start, you should at least have the following installed:

* The newest browsers you are able to install, to test your code in. If you don't have them already, grab them from the homepages of [http://www.google.com/chrome Chrome], [http://www.mozilla.org/en-US/firefox/new/ Firefox], and [http://www.opera.com Opera]. If you are on Windows please make sure [http://windows.microsoft.com/en-GB/internet-explorer/products/ie/home Internet Explorer] is up-to-date; on Mac OS please make sure [http://www.apple.com/safari/ Safari] is up-to-date.
* A decent text editor, to write your code in. Reasonable free options are [http://foicica.com/textadept/ TextAdept], [http://notepad-plus-plus.org/ Notepad++], [http://www.microsoft.com/visualstudio/eng/products/visual-studio-express-for-web Visual Studio Express] for Windows, [http://www.barebones.com/products/TextWrangler/ Text Wrangler] for Mac, and [http://bluefish.openoffice.nl/index.html Bluefish] for Linux.
* An FTP program, such as [http://cyberduck.ch/ Cyberduck] (Mac, Windows) or [https://filezilla-project.org/ Filezilla] (Mac, Windows, Linux). File Transfer (FTP) is used to move your web site files over from your computer's hard disk drive to the web server where they will live when they are finished, and become a part of the web.

Download and install these for now; we'll cover them in more detail in later Parts of the article series.

==Web hosting and domain name==

When you want to get content up online, you'll need to buy some web hosting space, and a domain name. These are as follows:

# When you buy web hosting, you basically buy some space on a web server set up and run by a third part company (you could also run your own web server, but this is not for a beginner's course!) This is done by going to a web hosting company and choosing an option to purchase.
# When you buy a domain name, you basically buy an address for your web content to live at on the Web, so for example google.com, apple.com, etc. You can choose a domain name by going to a domain name registrar such as [http://godaddy.com/ GoDaddy] and following the instructions.

Note that most domain name purchases will come with free hosting, so you'll probably only need to make one purchase. For your early web experiments, you don't need anything very expensive or complicated. In fact, until you want to start putting content online, you can just test your web code files locally, on your own web browser installation.
{{Notes_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}