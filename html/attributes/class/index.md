{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies one or more classes for an element, usually used to point to a class in a style sheet.}}
{{Markup_Attribute
|Applies_to=dom/HTMLElement
|Property_applies_to=dom/HTMLElement
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the class attribute to apply one or more styles to an HTML element.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;title&gt;&lt;/title&gt;
    &lt;style type{{=}}"text/css"&gt;
        p {font-size: 24pt;}
        .redText {color: red;}
        .blueText {color: blue;}
        .italicText {font-style: italic;}
    &lt;/style&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;p&gt;
        Large text, no class specified, one implied.
    &lt;/p&gt;
    &lt;p class{{=}}"redText"&gt;
        Large text, .redText class specified.
    &lt;/p&gt;
    &lt;p class{{=}}"blueText italicText"&gt;
        Large text, .blueText and .italicText classes specified.
    &lt;/p&gt;
  &lt;/body&gt;
&lt;/html&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The property is equal to NULL if the attribute is not explicitly assigned.
When multiple styles are specified for an element, a conflict could develop if two or more styles define the same attribute differently. In this case, you can resolve the conflict by applying styles to the element in the following order, according to the Cascading Style Sheets (CSS) selector used to define the style:
#Element
#Class attribute
#ID attribute
#Inline styles

When two or more selectors pertain to an element, a style defined later takes precedence over a style defined earlier. For more information, see Introduction to Cascading Style Sheets.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML]
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/
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