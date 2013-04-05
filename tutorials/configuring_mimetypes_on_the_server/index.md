{{Page_Title|Setting up Mime Types on your server}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=Yes
|Editorial notes=Initial creation. Will definitely need reviews
}}
{{Byline
|Name=Carlos Araya
|URL=http://rivendellweb.net/work
|Published=4/5/2013
}}
{{Summary_Section|How to set up media  or mime types for your your server and why you should always make sure they are set correctly.}}
{{Tutorial
|Content=After creating your content and setting up the proper content with text tracks and all the bells and whistles only to have your users report that it doesn't play for them.  You wreck your head for a few days and then discover that your server is not set up to properly handle the new video (or audio or any other type of content)  media types (also known as mime types.)

The media types help both servers and browsers to identify the kind of resource being asked for by the browser and served by the server. Take for example:

<pre>video/mp4</pre>

represents an MP4 (sub type) video (type)

while

<pre>application/font-woff</pre>

indicates a woff font (sub type) application (type). 

With the sheer number of formats, specifications and sub types (if you're really curious you can check the [[http://www.iana.org/assignments/media-types|IANA Media Type Registry]]j), it would be unrealistic to expect a server configuration to handle all the formats that we will use in our web sites and applications. 

Fortunately for our system administrators, most if not all, the available servers have a way for you to add new mime types to the server arsenal. The exact process will depend on the server you're using and some of the servers (Apache) have more than one way to add the media type(s). 

I have not listed all the possible servers. Only the ones I've directly worked with. If you have more servers to add, feel free to do so. 


==Apache HTTPD server - httpd.conf==

An administrator (with root access ideally) should edit the global configuration file (/etc/httpd.d/httpd.conf for example) and add the new types at the end of the media type listing, the lass line that starts with '''AddType'''.  The format is illustrated below. 

<pre>AddType video/ogg .ogv
AddType video/mp4 .mp4
AddType video/webm .webm</pre>


==Apache HTTPD server - .htaccess==

There may be times when you don't have access to edit the global configuration file or may want to make an exception by changing the global settings. In this instances Apache will allow you to create a special file (.htaccess) in the directory and add configuration directives that will apply only to that directory tree.

The sample below is a part of the [[https://raw.github.com/h5bp/html5-boilerplate/|HTML5 Boilerplate]]
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}