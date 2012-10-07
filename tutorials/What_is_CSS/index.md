{{Flags}}
{{Summary_Section|This tutorial answers the question "what is CSS?".}}
{{Tutorial
|Content=== Information: What is CSS ==
 
Cascading Style Sheets (CSS) is a language for specifying how documents are presented to users.
 
A ''document'' is a collection of information that is structured using a ''markup language''. Examples include:

* A web page like the one you are reading is a document. The information that you see in a web page is usually structured using the markup language HTML (HyperText Markup Language).
* Dialogs, also called modal windows, of an application are often documents. Such dialogs may also be structured using a markup language, like XUL. This is often the case in Mozilla applications, but is not the common case.
  
In this tutorial, boxes captioned '''More details''' like the one below contain optional information. If you are in a hurry to progress with the tutorial then you could skip these boxes, perhaps returning to read them later. Otherwise read them when you come to them, and perhaps follow the links to learn more.

===More details===

A document is not the same as a file. It might or might not be stored in a file.
 
For example, the document that you are reading now is not stored in a file. When your web browser requests this page, the server queries a database and generates the document, gathering parts of the document from many files. However, in this tutorial you will work with documents that are stored in files.
 
For more information about documents and markup languages, see other parts of this web site—for example:

                    
{{{!}} border="1"
{{!}}-
{{!}}[[HTML]]
{{!}}for web pages
{{!}}-
{{!}}[[XML]]
{{!}}for structured documents in general
{{!}}-
{{!}}[[svg|SVG]]
{{!}}for graphics
{{!}}-
{{!}}[[XUL]]
{{!}}for user interfaces in Mozilla
{{!}}} 

In Part II of this tutorial you will see examples of these markup languages.

''Presenting'' a document to a user means converting it into a form that humans can make use of. Browsers, like Firefox, Chrome or Internet Explorer, are designed to present documents visually — for example, on a computer screen, projector or printer.

CSS is not just for browsers, and not just for visual presentation. In formal CSS terminology, the program that presents a document to a user is called a ''user agent'' (UA). A browser is just one kind of UA. However, in Part I of this tutorial you will only work with CSS in a browser.

For some formal definitions of terminology relating to CSS, see [[Definitions]] in the CSS Specification.
  
== Action: Creating a document ==
 
<ol> 
<li><p>Use your computer to create a new directory and a new text file there. The file will contain your document.</p></li>
<li><p>Copy and paste the HTML shown below. Save the file using the name <code>doc1.html</code></p>
<pre>&lt;!DOCTYPE html&gt;
 &lt;html&gt;
   &lt;head&gt;
   &lt;meta charset="UTF-8"&gt;
   &lt;title&gt;Sample document&lt;/title&gt;
   &lt;/head&gt;
 
   &lt;body&gt;
     &lt;p&gt;
       &lt;strong&gt;C&lt;/strong&gt;ascading
       &lt;strong&gt;S&lt;/strong&gt;tyle
       &lt;strong&gt;S&lt;/strong&gt;heets
     &lt;/p&gt;
   &lt;/body&gt;
 &lt;/html&gt;</pre></li>
<li><p>In your browser, open a new tab or a new window, and open the file there. You should see the text with the initial letters bold, like this:</p>

'''C'''ascading '''S'''tyle '''S'''heets

<p>What you see in your browser might not look exactly the same as this, because of settings in your browser and in this wiki. If there are some differences in the font, spacing and colors that you see, they are not important.</p>
</li>
</ol>
 
== What next? ==
 
Your document does not yet use CSS. In the next article you will use CSS to specify its style.
}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/What_is_CSS
|MSDN_link=
|HTML5Rocks_link=
}}