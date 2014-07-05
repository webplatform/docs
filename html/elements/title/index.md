{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Add compatibility.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Defines the <code>title</code> of the current document.}}
{{Markup_Element
|DOM_interface=dom/HTMLTitleElement
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
}}
}}
{{Notes_Section
|Usage=You can only have one title element on your page. This tag is mandatory. If you omit it the document will not validate as HTML
|Notes=* defines a title in the browser toolbar
* provides a title for the page when it is added to favorites
* displays a title for the page in search-engine results

It can only contain text and any contained tags are not interpreted.

There are rare cases where the title is allowed to be omitted. This is the case when a higher-level protocol provides title information, like the subject line of an e-mail.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/global.html#h-7.4.2
|Status=Recommendation
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/document-metadata.html#the-title-element
|Status=Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=HTML
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}