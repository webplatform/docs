{{Page_Title|body}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Data Not Semantic, Unreviewed Import
|Content=Cleanup
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''body''' element (&lt;body&gt;) represents the main content of the document.}}
{{Markup_Element
|DOM_interface=dom/HTMLBodyElement
|Tag_omissions=Start and end are omissible in some cases
|CSS_display=block
|Content=You can access the <code><body></code> element from script through the document object.

The window object for the <code><body></code> element can host event handlers for the <code>onblur</code>, <code>onfocus</code>, <code>onload</code>, or <code>onunload</code> events.


=== HTML Event Handler Content Attributes ===

{{{!}} class="wikitable"
{{!}}-
!Event
!Description
{{!}}-
{{!}}<code>onafterprint</code> 
{{!}}User printed current document.
{{!}}-
{{!}}<code>onbeforeprint</code> 
{{!}}User requested printing of current document.
{{!}}-
{{!}}<code>onbeforeunload</code> 
{{!}}Document is about to be unloaded.
{{!}}-
{{!}}<code>onblur</code> 
{{!}}Document lost focus.
{{!}}-
{{!}}<code>onerror</code> 
{{!}}Document failed to load properly.
{{!}}-
{{!}}<code>onfocus</code> 
{{!}}Document received focus.
{{!}}-
{{!}}<code>onhashchange</code> 
{{!}}Fragment identifier part of the document’s current address changed.
{{!}}-
{{!}}<code>onload</code> 
{{!}}Document finished loading.
{{!}}-
{{!}}<code>onmessage</code> 
{{!}}Document received a message.
{{!}}-
{{!}}<code>onoffline</code> 
{{!}}Network connections failed.
{{!}}-
{{!}}<code>ononline</code> 
{{!}}Network connections returned.
{{!}}-
{{!}}<code>onpopstate</code> 
{{!}}User navigated session history.
{{!}}-
{{!}}<code>onredo</code> 
{{!}}User went forward in undo transaction history.
{{!}}-
{{!}}<code>onresize</code> 
{{!}}Document view was resized.
{{!}}-
{{!}}<code>onstorage</code> 
{{!}}Storage area changed.
{{!}}-
{{!}}<code>onundo</code> 
{{!}}User went backward in undo transaction history.
{{!}}-
{{!}}<code>onunload</code> 
{{!}}Document is going away.
{{!}}}

The following attributes are obsolete, and should not be used by authors: <code>alink</code>, <code>bgcolor</code>, <code>link</code>, <code>marginbottom</code>, <code>marginheight</code>, <code>marginleft</code>, <code>marginright</code>, <code>margintop</code>, <code>marginwidth</code>, <code>text</code>, <code>vlink</code>.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The <code><body></code> element follows the <code><head></code> element and is contained by the <code><html></code> element.
|Code=<syntaxhighlight lang="html5">
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>The HTML Document</title>
</head>
<body>
<p>The HTML content</p>
</body>
</html>
</syntaxhighlight>
|LiveURL=http://test.w3.org/html/examples/elements/body/body01.html
}}{{Single Example
|Language=JavaScript
|Description=This example exposes the <code><body></code> element in javascript.
|Code=<syntaxhighlight lang="javascript">var oBody = document.body;</syntaxhighlight>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/sections.html#the-body-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/sections.html#the-body-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/global.html#edef-BODY
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
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer (Windows)
|Version=8+
|Note=The value of the <code>background</code> attribute depends on the current document compatibility mode.
}}{{Compatibility Notes Row
|Browser=Internet Explorer (Windows)
|Version=6
|Note=When you use the <code>!DOCTYPE</code> declaration to specify standards-compliant mode, this object no longer represents the entire surface onto which a document's contents can be rendered. The object can obtain its size from its content, or you can set its size explicitly like a <code>div</code> object.
}}{{Compatibility Notes Row
|Browser=Internet Explorer (Windows)
|Version=6+
|Note=As of Microsoft Internet Explorer 6, when you use the <code>!DOCTYPE</code> declaration to specify standards-compliant mode, the <code><body></code> object can obtain its size from its content, or you can set its size explicitly—like a <code>div</code> object, for example. In standards-compliant mode, the <code><html></code> element represents the entire surface onto which a document's contents can be rendered. When the <code>!DOCTYPE</code> declaration does not specify standards-compliant mode, and with earlier versions of Windows Internet Explorer, the <code><body></code> object represents the entire surface onto which a document's contents can be rendered. The size of the <code><body></code> object cannot be changed and is equal to the size of the window. Margins you set on this object are rendered inside the border and scrollbars of the object.
}}
}}