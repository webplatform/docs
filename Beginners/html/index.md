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
== Topics ==
The '''[[Beginners]]''' section covers the various aspects of web development separated in 9 parts, you can browser through them using this list.

* [[Beginners/the_beginning|1. The beginning]]
* [[Beginners/crash_course|2. A crash course in web site code]]
* [[Beginners/planning|3. Planning]]
* '''[[Beginners/html|4. Structuring our content with HTML]]'''
* [[Beginners/css|5. Styling our content with CSS]]
* [[Beginners/programming|6. Programming fundamentals]]
* [[Beginners/javascript|7. JavaScript]]
* [[Beginners/advanced|8. Advanced topics]]
* [[Beginners/browser_testing|9. Browser testing]]
* [[Beginners/glossary|Glossary]]


== An HTML Document with details about each components ==

Ever wondered the utility of a web page, here are a few notes to help you understand their existence.

You can copy and paste this code in a new file (e.g. <tt>index.html</tt>) and open it in a web browser. You should see only a white page with a big "Hello world" written in red.

=== An example document in a web browser ===

[[File:Beginners_example_html_file.png|upright|A web browser window with Hello world in red]]

=== An example document code ===

<syntaxHighlight>
<!DOCTYPE html><!-- This tag is an HTML Comment -->
<!-- ^ The DOCTYPE tag tells the browser what version 
       of HTML it is dealing with; there are others and  
       we want to make sure there is no confusion. -->
<html lang="en"><!-- this is how we open every document; the  
       language part is optional, but makes sure your document  
       doesn't look like gobbledy gook when someone in Korea  
       opens your document in a browser that defaults to Korean -->
 <head><!-- required part of every HTML document, this is  
       where we add internal information (i.e. meta) about  
       the current HTML page -->
   <meta charset="utf-8"><!-- This is a way, in HTML, to  
                              tell the browser that we are writing text in UTF-8  
                              so we can write Greek, Russian, English, French  
                              and many others in one page -->
   <title>Example Page</title><!-- REQUIRED, This is what gets  
                                   displayed on the web browser tab -->
	<link rel="stylesheet" href="style1.css" type="text/css" media="screen">
        <!-- ^ Will call another file, called "style1.css" that   
               is right beside the current document. Why this    
               syntax? The "type" is similar to the previous meta charset,    
               it specifies the web browser to read the file as CSS. While    
               we, humans, think that ".css" is telling, computers doesn’t    
               need extension (this is an old story), but instead use what    
               we call headers to tell what type of file it is.

               The media attribute in the link tag tells us to WHEN to apply    
               the stylesheet. This is what we commonly refer to as a MediaQuery.
               The first use of media queries was mostly used to deal with how a web page
               would look like once printed (back in 200x) but now its much more complete
               to help us target screen resolution and other aspects.  -->
<style>h1 { color: red; }  /* This is a CSS comment. Inside an HTML document that has
                              an embedded CSS document that you we are using until   
                              we close the style tag */
</style><!-- ^ Instead of using a link tag, we can also add
               CSS directly in a document -->
 </head><!-- Closing the head, now the real deal. 
             Note that whatever is in the head, can  
             potentially block. When you will want to learn about  
             performance, you’ll remember that note. -->
 <body>
   <h1>Hello world</h1><!-- Because of the previous style tag, if you look at this
                            web page in a browser, the Hello world should be red -->
 </body>
</html>
</syntaxHighlight>
{{Notes_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}