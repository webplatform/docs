{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Deletion Candidate: It's deprecated, http://www.w3.org/TR/html5/obsolete.html#non-conforming-features
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Deprecated}}
{{API_Name}}
{{Summary_Section|(Obsolete) A special-purpose single-line text input field}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=
|CSS_display=
|Content=This element was created to provide a single-line text-input control to allow any characters for entering a query string. The query string was supposed to be sent to the server identified by the base URL and return a list of pages matching this query. 

== History ==

On June 1992, Dan Connolly would [http://1997.webhistory.org/www.lists/www-talk.1992/0080.html prefer] a different [[HTML/Elements/a|anchor]] type instead of isindex.

On November 1992, [http://lists.w3.org/Archives/Public/www-talk/1992NovDec/thread.html#31 indexes as links rather than documents] started by Dan Connolly who is pushing the idea that indexes are more links than documents. In this thread, different type of solutions are proposed. The question of forms for making queries is [http://lists.w3.org/Archives/Public/www-talk/1992NovDec/0039.html mentioned] in reference to Dynatext browser: "The browser displays toggle buttons, text
fields etc. The user fills in the fields, clicks OK, and the
query results come up in the table of contents window."

A thread about [http://lists.w3.org/Archives/Public/www-talk/1992NovDec/thread.html#42 isindex] in November 1992, Kevin Hoadley [http://lists.w3.org/Archives/Public/www-talk/1992NovDec/0042.html questioned]  the need for an isindex element and proposed to drop it. He proposed to have instead an [[HTML/Elements/input|input]] element (idea [http://lists.w3.org/Archives/Public/www-talk/1992NovDec/0053.html supported] by Steve Putz). Tim Berners-Lee [http://lists.w3.org/Archives/Public/www-talk/1992NovDec/0044.html explains] the purpose of isindex resulting in aggregated search results. Kevin [http://lists.w3.org/Archives/Public/www-talk/1992NovDec/0048.html replies] that he doesn't like the boolean nature of isindex and would prefer a system where everything is searchable and proposes to extend the current WWW Framework with a specific httpd configuration and defined that some URIs mapping create search queries.

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=This example uses the '''ISINDEX''' element to replace the default prompt.
|Code=&lt;ISINDEX PROMPT{{=}}"Enter a keyword to search for in the index"&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
In HTML 4, this element is deprecated; '''INPUT''' is recommended for use instead. The [[dom/properties/tagName|'''tagName''']] property for '''isIndex''' returns '''input'''.
The '''ISINDEX''' element belongs in the '''body''' of the document.
This element is treated as an '''input''' object inside a '''form''' object.
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
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}