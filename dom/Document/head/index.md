{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs compat
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Gets the [[html/elements/head|head]] element of the document.}}
{{API_Object_Property
|Property_applies_to=dom/Document
|Read_only=Yes
|Example_object_name=document
|Return_value_name=headElement
|Javascript_data_type=DOM Node
|Return_value_description=The [[html/elements/head|head]] element of the document.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example displays the text (innerHTML) of the document's <code>head</code> element.
|Code=<!DOCTYPE HTML>
<html>
<head>
<title>New Document</title>
<meta name="Generator" content="Notepad">
<meta name="Author" content="Bob Palindrome">
<meta name="Keywords" content="document head">
<meta name="Description" content="head property example">
</head>

<body>
<nowiki>
<p onclick="alert(document.head.innerHTML)">Click me to see the contents of the &lt;head&gt; element</p>
</nowiki>
</body>
</html>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html5/dom.html#dom-document-head
|Status=Candidate Recommendation
|Relevant_changes=Section 3.1.1
}}{{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage
|Status=Living Standard
|Relevant_changes=Section 3.1.1
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}