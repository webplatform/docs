{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information. Add HTML information section. Complete Events section.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Cleanup, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''html''' element (&lt;html&gt;) represents the root of an HTML document. The &lt;html&gt; tag is the container for all other HTML elements; except for the &lt;!DOCTYPE&gt; tag.}}
{{Markup_Element
|DOM_interface=dom/HTMLHtmlElement
|Tag_omissions=
|CSS_display=
|Content=The '''html''' element is used to contain a complete HTML document.

<syntaxhighlight language="html5">
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>An Example Web Page</title>
  </head>
  <body>
    <h1>Hello World!</h1>
    <p>
      This is an example web page marked up using HTML.
    </p>
  </body>
</html>
</syntaxhighlight>


Internationalization topics related to the <code>html</code> element:
* [http://www.w3.org/International/techniques/authoring-html#textprocessing Declaring the overall language of a page]
* [http://www.w3.org/International/techniques/authoring-html#using Setting up a right-to-left page]
}}
{{Examples_Section
|Not_required=Yes
|Examples={{Single Example
|Language=HTML
|Description=
|Code=
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
When you use the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration to specify standards-compliant mode, this element represents the canvas—the entire surface onto which a document's contents can be rendered.  When you switch on standards-compliant mode, this element also becomes the positioning container for positioned elements that don't have a positioned parent. When the !DOCTYPE declaration does not specify standards-compliant mode,  the '''body''' object represents the entire surface onto which a document's contents can be rendered.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/semantics.html#the-html-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/semantics.html#the-html-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/global.html#edef-HTML
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=HTML
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
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}