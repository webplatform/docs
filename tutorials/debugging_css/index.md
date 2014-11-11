{{Page_Title|Debugging CSS}}
{{Flags
|State=In Progress
|Editorial notes=List utilities to help debug CSS.
|Checked_Out=Yes
|High-level issues=Stub
}}
{{Byline
|Name=Renoir Boulanger
|URL=https://renoirboulanger.com/
|Published=
}}
{{Summary_Section|This article lists utilities to help analyze situations where a CSS style we think should be applied is not.}}
{{Tutorial
|Next_page=
|Prev_page=
|Content===Content Needed==
This topic is in progress, we just ran out of time. If you have the time to write it up, please do. We’re all pitching in here at WPD. Thanks!

Methods for debugging CSS are essential, since CSS errors will not output any error message indicating the source of the issue at hand. 

==Avoiding problems in the first place==

===Cross browser Idiosyncrasies===
As mentioned in previous tutorials Web Browsers come with inbuilt CSS. This default CSS may differ between browsers and hence when viewing a site, unless the site CSS cancels out the browser's CSS there is a chance that the page is displayed differently across browsers, which most of ten than not it is undesirable.

This problem is avoided by normalizing the browser. This is done by using a set of CSS rules to cancel the web browser default CSS before applying custom CSS. There exist a couple of CSS normalizing files on the net freely available.



== CSS to debug CSS==

One of the things that could help in identifying a layout issue or perhaps some complex structure like a CSS based menu one would want to see what is really going on in terms of boxes.

<syntaxhighlight lang="css">*{
  outline:1px red solid; 
}</syntaxhighlight>

Using the above will display an outline around each element on the page indicating the structure, which could help in identifying where certain problems are.

== Isolate the issue==

If the problem is in a fully blown site with plenty of HTML/CSS, start commenting out the HTML and CSS rules and try to isolate the issue and perhaps even replicate it  and try to find the offending rules.

==WebBrowser tools==

At the time of writing Google Chrome/Mozilla Firefox and Internet Explorer come with inbuilt developer tools that could help with debugging. These tools allow to inspect elements and view the CSS applied on them. Furthermore one could disable rules, remove properties, add rules and add properties and view the changes in the browser.
}}
{{Notes_Section
|Usage=
|Notes=* Need to make summary
* Need to list more relevant and credible resources
|Import_Notes=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=
|External_links=* [http://24ways.org/2005/debugging-css-with-the-dom-inspector/  24 ways: Debugging CSS with the DOM inspector]
* [http://bigemployee.com/4-simple-techniques-to-quickly-debug-and-fix-your-css-code-in-almost-any-browser/ Debugging HTML and CSS with the developer tools]
|Manual_sections=* [http://www.w3.org/TR/CSS2/cascade.html#cascade CSS Level 2 : The cascade]
}}
{{Topics|CSS, Developer Tools, HTML, Inheritance}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}