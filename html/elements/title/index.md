{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Defines the <code>title</code> of the current document.}}
{{Markup_Element
|DOM_interface=dom/HTMLTitleElement
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''title''' element to specify a title for the document.
|Code=<!doctype html>
<html>
<head>
<title>WebPlatform.org - Your Web, documented</title>
</head>
</html>
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=This example uses the '''title''' element to provide the current page title as well as the category and the title of the website.
|Code=<!doctype html>
<html>
<head>
<title>title &bull; html &bull; WebPlatform.org</title>
</head>
</html>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=You can only have one title element per page. The content of this element is shown in the browser title bar, used for titles of favorites and bookmarks. It is usually also displayed as a title on search engine results pages.

It is read by screen readers as soon as the web page has finished loading and is the first information assistive technologies receive. It can be used to convey information immediately to users using such tools, like the success or error of a form submission.

Titles of sub pages should provide the most specific information on front (“front-loading”), for example a website might first provide the title of the current page, then the name of the category and the name of the complete website.
|Notes=It can only contain text and any contained tags are not interpreted.

There are rare cases where the title is allowed to be omitted. This is the case when a higher-level protocol provides title information, like the subject line of an e-mail.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related_Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/document-metadata.html#the-title-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/document-metadata.html#the-title-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/global.html#edef-TITLE
|Status=W3C Recommendation
|Relevant_changes=
}}
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