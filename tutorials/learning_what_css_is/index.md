{{Page_Title|What is CSS?}}
{{Flags
|Checked_Out=No
}}
{{Byline}}
{{Summary_Section|The article introduces you to Cascading Style Sheets, or CSS, defining what they are, and what they are used for on the Web.}}
{{Tutorial
|Content=This tutorial explains what CSS is. You create a simple document that you will work with on the following pages.
 
== About CSS ==
 
Cascading Style Sheets (CSS) is a language for specifying how documents are presented to users. A ''document'' is a collection of information that is structured using a ''markup language''.

===Examples===

* A web page like the one you are reading is a document. The information that you see in a web page is usually structured using the markup language HTML (HyperText Markup Language).
* Dialogs, also called modal windows, of an application are often documents. Such dialogs may also be structured using a markup language, like XUL. This is often the case in Mozilla applications, but is not the common case.
  
In this tutorial, boxes captioned '''More details''' like the one below contain optional information. If you are in a hurry to progress with the tutorial then you could skip these boxes, perhaps returning to read them later. Otherwise read them when you come to them, and perhaps follow the links to learn more.
  
===More details===

A document is not the same as a file. It might or might not be stored in a file.
 
For example, the document that you are reading now is not stored in a file. When your web browser requests this page, the server queries a database and generates the document, gathering parts of the document from many files. However, in this tutorial you will work with documents that are stored in files.

For more information about documents and markup languages, see other parts of this web site—for example:

<table>
  <tr>
    <td style="width: 10%;">[[HTML]]</td> <td>for web pages</td>
  </tr>
  <tr>
    <td style="width: 10%;">[[XML]]</td> <td>for structured documents in general</td>
  </tr>
  <tr>
    <td style="width: 10%;">[[SVG]]</td> <td>for graphics</td>
  </tr>
  <tr>
    <td style="width: 10%;">[[XUL]]</td> <td>for user interfaces in Mozilla</td>
  </tr>
</table>

In Part II of this tutorial you will see examples of these markup languages.

''Presenting'' a document to a user means converting it into a form that humans can make use of. Browsers, such as Opera, Firefox, or Internet Explorer, are designed to present documents visually — for example, on a computer screen, projector or printer.

CSS is not just for browsers, and not just for visual presentation. In formal CSS terminology, the program that presents a document to a user is called a ''user agent'' (UA). A browser is just one kind of UA. However, in Part I of this tutorial you will only work with CSS in a browser.
 
For some formal definitions of terminology relating to CSS, see [[Definitions]] in the CSS Specification.

=== Action: Creating a document ===
 
# Create a new directory and open a text editor
# Copy and paste the HTML shown below. Save the file using the name <code>doc1.html</code>

<syntaxhighlight lang="html5"><!DOCTYPE html>
 <html>
   <head>
   <meta charset="UTF-8">
   <title>Sample document</title>
   <link rel="stylesheet" href="style1.css">
   </head>
   <body>
     <p>
       <strong>C</strong>ascading
       <strong>S</strong>tyle
       <strong>S</strong>heets
     </p>
   </body>
 </html></syntaxhighlight>

# In your browser, open a new tab or a new window, and open the file there.

You should see the text with the initial letters bold, like this:

'''C'''ascading '''S'''tyle '''S'''heets

What you see in your browser might not look exactly the same as this, because of settings in your browser and in this wiki. If there are some differences in the font, spacing and colors that you see, they are not important.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=CSS
|Chrome_supported=Yes
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=CSS
|Android_supported=Yes
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Lynx
|Version=all
|Note=Lynx does not support CSS very well
}}
}}
{{See_Also_Section
|External_links=* [http://www.google.com Google]
* [http://www.mozilla.org Mozilla]
* [http://www.opera.com Opera]
|Manual_sections====Contributions===
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|HTML5Rocks_link=
}}