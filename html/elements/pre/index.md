{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=HTML information must be modified. Add compatibility.
How is whitespace/escaping handled when a <code> tag is inside a <pre> tag?
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The pre tag defines preformatted text. Text in a pre element is displayed in a fixed-width font and preserves both spaces and line breaks.}}
{{Markup_Element
|DOM_interface=dom/HTMLPreElement
|Tag_omissions=Closing tag required
|CSS_display=block
|Content=Examples of content might include:
* e-mail
* computer code
* ASCII art
* program output

This element is used with the code element, the samp element, or the kbd element, and so on, according to the kind of content inside a pre element.


== Rendering in text/html ==

Unlike in XML mode, a text/html parser will strip the newline character if it appears after the opening <code>&lt;pre&gt;</code> tag, as an authoring convenience.


== Accessibility ==

The author should consider accessibility, when use the pre element. This is because, when speech synthesizers, braille displays, and the like is used, there is a possibility that preformatted text is destroyed. For example, for cases like ASCII art, it is likely that an alternative presentation, such as a textual description, would be more universally accessible to the readers of the document.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''PRE''' element to format text so that it renders exactly as it is typed.
|Code=&lt;pre&gt;
This text is formatted
   exactly
      as
         it
      is
   typed.
&lt;/pre&gt;
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=Example of pre-formatted computer code inside a &lt;code&gt; tag
|Code=<nowiki>
&lt;pre&gt;
  &lt;code&gt;
  process.run();
  &lt;/code&gt;
&lt;/pre&gt;
</nowiki>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=To cater for international users see: [http://www.w3.org/International/techniques/authoring-html#form-dir Managing text direction in form controls]
|Notes====Remarks===
Text within the '''PRE''' element is formatted. Spaces and carriage returns are preserved.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/grouping-content.html#the-pre-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/grouping-content.html#the-pre-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/text.html#edef-PRE
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>xmp</code>
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