{{Page_Title|Proxy-based browsers}}
{{Flags
|State=Not Ready
|Editorial notes=This is not a web development concept topic, and will attract vendor spam. Deletion candidate.
|Checked_Out=No
|High-level issues=Stub, Deletion Candidate
}}
{{API_Name}}
{{Summary_Section|This article will give an overview of proxy based browsers. Some solution transform web pages into compact formats. Some solution only provides data compression.}}
{{Concept_Page
|Content=== Purpose ==
Proxy Based web browsers reduce bandwidth usage by compressing resources of the rendered page on a proxy server (usually the browser vendors), before sending it to the client browser.

To make a request:
# The client requests a page from the Proxy Server.
# The proxy server requests the page from the origin server.
# The proxy server renders the page / runs javascript /compresses the page (the methods vary between implementations).
# The proxy server sends the client the rendered page.
# Client interaction with page is sent to the proxy server, who forwards it onto the origin server.

== Concerns ==
* Each implementation has different feature support.
* There may be concerns about trusting a third party service with browsing data.


== Implementations ==
* Opera Mini [http://www.opera.com/mobile/]
* Opera Desktop with Turbo [http://www.opera.com/browser/turbo/]
* Kindle Fire Silk
<blockquote>All of the browser subsystems are present on your Kindle Fire as well as on the AWS cloud computing platform.  Each time you load a web page, Silk makes a dynamic decision about which of these subsystems will run locally and which will execute remotely.</blockquote>
* Bolt [http://boltbrowser.com/]
* Skyfire [http://www.skyfire.com/]
* Nokia Xpress Browser [http://www.nokia.com/ie-en/apps/apps-by-nokia/xpressbrowser/]
* UC Browser [http://www.ucweb.com]
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|Mobile}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}