{{Page_Title|Part 4: Structuring our content with HTML}}
{{Flags
|State=Not Ready
|Editorial notes=Quoting David Hertz original proposal:

* Add more example in the body section:
** high level page structure - header, footer, navigation, main content, sidebar
** header - include title, logo, search form
** footer - include license notice, accessibility statement, contact details?
** navigation - include 5 items, do horizontal nav as it is better for learning
** main content - have this as the main recipe details; use it as an opportunity to demonstrate some good typography
** sidebar - have this as an image gallery of images from the recipe
|Checked_Out=No
}}
{{Summary_Section|Next we will dive into Hypertext Markup Language (HTML), structuring our content. This document shows an example HTML file with notes on each components that will help you learn their use.}}
{{Basic Page}}
{{:Beginners/Submenu}}

== An HTML Document with Details About Each Component ==

Ever wondered the meaning of the building blocks of a webpage? Here’s a breakdown of the main components.

=== An Example Document in a Web Browser ===

[[File:Beginners_example_html_file.png|upright|A web browser window with Hello world in red]]

=== An Example Document Code ===

You can copy and paste this code in a new file (e.g. <tt>index.html</tt>) and open it directly in a web browser — no web server needed!

You should see only a white page with a big "Hello world" written in red like the image above.

<syntaxHighlight lang="html5">
<!DOCTYPE html><!-- This tag is an HTML Comment -->
<!-- ^ The DOCTYPE tag tells the browser what version 
       of HTML it's dealing with; there are others and  
       we want to make sure that there's no confusion. -->
<html lang="en"><!-- We open with the html tag; the  
       language part is optional. 

       While some say it's for text encoding
       purposes (i.e. unexpected characters), it is not for that. It's for
       accessibility adaptive technology to know which language it should
       adapt to while reading.

       As for the text encoding, see below at "meta charset" -->
 <head><!-- Required part of every HTML document, this is  
       where we add internal information (i.e. metadata) about  
       the current HTML page -->
   <meta charset="utf-8"><!-- This is a way, in HTML, to  
                              tell the browser that we are writing text in UTF-8  
                              so we can write Greek, Russian, English, French 
                              and many others in one page.

                              This is one of the two way to handle which set of letters
                              to display the text. The web server handles this, but the
                              meta charset is also helpful.
                              
                              In essence those two make sure the content doesn't look 
                              like gobbledy gook when someone in Korea opens your document
                              in a browser that defaults to Korean -->
   <title>Example Page</title><!-- REQUIRED. This is what gets  
                                   displayed on the web browser tab or window -->
	<link rel="stylesheet" href="style1.css" type="text/css" media="screen">
        <!-- ^ Will call another file, called "style1.css" that   
               is right beside the current document. Why this    
               syntax? The "type" is similar to the previous meta charset,    
               it specifies the web browser to read the file as CSS. While    
               we, humans, think that ".css" is telling, computers doesn’t    
               need extension (this is an old story), but instead use what    
               we call headers to tell what type of file it is.

               The media attribute in the link tag tells us to WHEN to apply    
               the stylesheet. This is what we commonly refer to as a media query.
               The first use of media queries was to deal with how a webpage
               would look like once printed (back in 200x) but now it's much more complete
               to help us target screen resolutions and other aspects like screen orientation.  -->
<style>h1 { color: red; }  /* This is a CSS comment. Inside an HTML document that has
                              an embedded CSS part inside <style> tags, we use CSS comments. */
</style><!-- ^ Instead of using a link tag, we can also add
               CSS directly in a document -->
 </head><!-- Closing the head. -->
 <body>
   <h1>Hello world</h1><!-- Because of the previous style tag, if you look at this
                            webpage in a browser, the Hello world should be red -->
 </body>
</html>
</syntaxHighlight>
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