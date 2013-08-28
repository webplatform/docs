{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The script element enables dynamic script and data blocks to be included in documents. It can contain code/data directly or it can link to external sources. It is mainly used with JavaScript.}}
{{Markup_Element
|DOM_interface=dom/HTMLScriptElement
|Content====Standards information===
*[http://www.w3.org/TR/DOM-Level-2-HTML/html#ID-81598695 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5.
*[http://www.w3.org/TR/html401/interact/scripts.html#h-18.2.1 HTML 4.01 Specification], Section 18.2.1.
*[http://www.w3.org/TR/html5/scripting-1.html HTML 5 Specification], Section 4.3.

===Members===
The '''script''' object has this type of member:
*[[#properties|Properties]]

====Properties====
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
{{!}}Sets or retrieves the MIME type for the script, the default is <code>text/javascript</code>. You can't use the charset attribute with this attribute.
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
{{!}}Sets or retrieves the whether or not the script will be loaded asynchronously and executed synchronously.
{{!}}No
{{!}}-
{{!}}[[html/attributes/async{{!}}'''aync''']]
{{!}}Sets or retrieves the whether or not the script will be loaded asynchronously and executed asynchronously.
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
|Code=&lt;script src=&quot;http://example.com/Script/Url/here.js&quot; type=&quot;application/Javascript&quot;&gt;&lt;/script&gt;
}}{{Single Example
|Language=HTML
|Description=Writing an inline script.
|Code=&lt;script type=&quot;application/Javascript&quot;&gt;
  //Do stuff...
&lt;/script&gt;
}}
}}
{{Notes_Section
|Notes=Code within the '''script''' block that is not contained within a function is executed immediately as the document is loaded.When the [[html/attributes/Type|'''Type''']] attribute is unset on the '''script''' object, then <code>text/javascript</code> is used. The order of the '''script''' objects in a document can also be important, especially if scripting event handlers are assigned to one or more elements in the document.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=[[html/elements/noscript|<noscript> tag]]
|Manual_sections====Related pages (MSDN)===
*<code>XML Data Islands</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}