{{Page_Title|HTML Imports: #include for the web}}
{{Flags
|Checked_Out=No
}}
{{Byline
|Name=Eric Bidelman
|URL=http://www.html5rocks.com/profiles/#ericbidelman
|Published=11 November 2013
}}
{{Summary_Section|'''HTML Imports''', part of Web Components, is a way to include HTML documents in other HTML documents. An import can include CSS, JavaScript, or anything else an .html file can contain. }}
{{Tutorial
|Content===Why imports?==

Think about how you load different types of resources on the web. For JS, we have <code><script src></code>. For CSS, your go-to is probably <code><link rel="stylesheet"></code>. For images it's <code><img></code>. Video has <code><video></code>. Audio, <code><audio></code>... Get to the point! The majority of the web's content has a simple and declarative way to load itself. Not so for HTML. Here's your options:

#'''<iframe>''' - tried and true but heavy weight. An iframe's content lives entirely in a separate context than your page. While that's mostly a great feature, it creates additional challenges (shrink wrapping the size of the frame to its content is tough, insanely frustrating to script into/out of, nearly impossible to style).
#'''AJAX''' - [http://ericbidelman.tumblr.com/post/31140607367/mashups-using-cors-and-responsetype-document I love xhr.responseType="document"], but you're saying I need JS to load HTML? That doesn't seem right.
#'''CrazyHacks™''' - embedded in strings, hidden as comments (e.g., <code><script type="text/html"></code>). Yuck!

See the irony? The web's most basic content, HTML, requires the greatest amount of effort to work with. Fortunately, [http://w3c.github.io/webcomponents/explainer/ Web Components] are here to get us back on track.

}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/webcomponents/imports/
}}