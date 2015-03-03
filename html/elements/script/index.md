{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The script element enables dynamic script and data blocks to be included in documents. It can contain code/data directly or it can link to external sources. It is mainly used with JavaScript.}}
{{Markup_Element
|DOM_interface=dom/HTMLScriptElement
|Tag_omissions=
|CSS_display=
|Content====Standards information===
*[http://www.w3.org/TR/DOM-Level-2-HTML/html#ID-81598695 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5.
*[http://www.w3.org/TR/html401/interact/scripts.html#h-18.2.1 HTML 4.01 Specification], Section 18.2.1.
*[http://www.w3.org/TR/html5/scripting-1.html HTML 5 Specification], Section 4.3.

===Properties===
The '''script''' object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
!Used with inline scripts
{{!}}-
{{!}}[[html/attributes/src (script){{!}}'''src''']]
{{!}}Retrieves the URL to an external file that contains the source code or data.
{{!}}No
{{!}}-
{{!}}[[html/attributes/type (script element){{!}}'''type''']]
{{!}}Sets or retrieves the MIME type for the script. Required in HTML 4, defaults to <code>text/javascript</code> in HTML 5. For JavaScript, this should always be set to  <code>application/javascript</code> since [https://tools.ietf.org/html/rfc4329 RFC4329].
{{!}}Yes
{{!}}-
{{!}}[[html/attributes/charset{{!}}'''charset''']]
{{!}}Sets or retrieves the script's character encoding. You can't use the type attribute with this attribute.
{{!}}No
{{!}}-  
{{!}}[[html/attributes/language{{!}}'''language''']]
{{!}}Sets or retrieves the programming language for the associated scripting engine. Depracated, use type instead.
{{!}}Yes
{{!}}-  
{{!}}[[html/attributes/defer{{!}}'''defer''']]
{{!}}Specifies that script should be executed after the document has been parsed.
{{!}}No
{{!}}-
{{!}}[[html/attributes/async{{!}}'''async''']]
{{!}}Specifies that the script should be executed asynchronously, as soon as it becomes available.
{{!}}No
{{!}}-
{{!}}[[html/attributes/crossorigin{{!}}'''crossorigin''']]
{{!}}Sets or retrieves the whether or not script error information will be revealed from the script(This is used only when scripts are being loaded from different origins).
{{!}}No
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Loading an external script.
|Code=<nowiki><script src="http://example.com/Script/Url/here.js" type="application/javascript"></script></nowiki>
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=Writing an inline script.
|Code=<nowiki><script type="application/javascript">
  //Do stuff...
</script></nowiki>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=Code within the '''script''' block that is not contained within a function is executed immediately as the document is loaded.When the [[html/attributes/Type|'''Type''']] attribute is unset on the '''script''' object, then <code>text/javascript</code> is used. The order of the '''script''' objects in a document can also be important, especially if scripting event handlers are assigned to one or more elements in the document. Using <code lang="HTML">async="async"</code> didn't work in some older browser, instead <code lang="HTML">async="true"</code> was used.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/scripting-1.html#the-script-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/scripting-1.html#the-script-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/interact/scripts.html#edef-SCRIPT
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=HTML
|Manual_links=[[html/elements/noscript|<noscript> tag]]
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>XML Data Islands</code>
}}
{{Topics|HTML, JavaScript}}
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
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0(probably)
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=1.0
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=1.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=1.0
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1.0
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}