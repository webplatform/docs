{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|HTML}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example causes the browser to reload the document every two seconds.
|LiveURL=
|Code=
&lt;meta http-equiv{{=}}"refresh" content{{=}}"2"&gt;
}}
{{Single_Example
|Description=This example sets the character set for the document.
|LiveURL=
|Code=
&lt;meta http-equiv{{=}}"Content-Type"
      content{{=}}"text/html; charset{{=}}utf-8"&gt;
}}
{{Single_Example
|Description=This example disables theme support for the document.
|LiveURL=
|Code=
&lt;meta http-equiv{{=}}"msthemecompatible" content{{=}}"no"&gt;
}}
{{Single_Example
|Description=This example tells Internet Explorer to display a webpage in IE9 mode, if possible.
|LiveURL=
|Code=
&lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}9"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
If the property is omitted, the [[html/attributes/name (meta object)|'''name''']] property should be used to identify the meta-information. The '''httpEquiv''' property is not case-sensitive.
Developers using the '''httpEquiv''' and '''content''' attributes to refresh documents from alternate URLs should treat the value of '''content''' as untrusted data.  For more information, please see Security Considerations: Dynamic HTML.

As of Windows Internet Explorer 8, the '''httpEquiv''' attribute also supports a value of <code>x-ua-compatible</code>, which allows developers to specify the document compatibility mode that Windows Internet Explorer should use to display a webpage.  To do this, set the '''content''' attribute to a '''String''' value containing a comma-delimited list of one or more of the following values.

{| class="wikitable"
|-
|'''Value'''
|'''Description'''
|-
|<code>IE{{=}}9</code>
|The webpage is displayed in IE9 Standards mode.
|-
|<code>IE{{=}}8</code>
|The webpage is displayed in IE8 Standards mode.
|-
|<code>IE{{=}}7</code>
|The webpage is displayed in IE7 Standards mode.
|-
|<code>IE{{=}}5</code>
|The webpage is displayed in IE5 (Quirks) mode.
|-
|<code>IE{{=}}EmulateIE9</code>
|If the webpage specifies a standards-based [[dom/properties/doctype|'''doctype''']] directive, the page is displayed in IE9 mode; otherwise, it is displayed in IE5 mode.
|-
|<code>IE{{=}}EmulateIE8</code>
|If the webpage specifies a standards-based [[dom/properties/doctype|'''doctype''']] directive, the page is displayed in IE8 mode; otherwise, it is displayed in IE5 mode.
|-
|<code>IE{{=}}EmulateIE7</code>
|If the webpage specifies a standards-based [[dom/properties/doctype|'''doctype''']] directive, the page is displayed in IE7 mode; otherwise, it is displayed in IE5 mode.
|-
|<code>IE{{=}}Edge</code>
|The webpage is displayed in the highest mode available to the version of Internet Explorer used to view the page. This option is generally intended for testing purposes.
|}
 
When the content attribute specifies multiple document modes, Internet Explorer displays the page in the highest mode supported by the browser. For more information, see Defining Document Compatibility.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 7.4.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Reference</code>
*<code>content</code>
*<code>meta</code>
*<code>Conceptual</code>
*<code>Defining Document Compatibility</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}