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
|Description=This example uses the className attribute to apply one or more styles to an HTML element.
|LiveURL=
|Code=
&lt;HEAD&gt;
    &lt;STYLE TYPE{{=}}"text/css"&gt;
        P {font-size: 24pt;}
        .redText {color: red;}
        .blueText {color: blue;}
        .italicText {font-style: italic;}
    &lt;/STYLE&gt;
&lt;/HEAD&gt;

&lt;BODY&gt;
    &lt;P&gt;
        Large text, no class specified, one implied.
    &lt;/P&gt;
    &lt;P CLASS{{=}}"redText"&gt;
        Large text, .redText class specified.
    &lt;/P&gt;
    &lt;P CLASS{{=}}"blueText italicText"&gt;
        Large text, .blueText and .italicText classes specified.
    &lt;/P&gt;
&lt;/BODY&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The property is equal to NULL if the attribute is not explicitly assigned.
When multiple styles are specified for an element, a conflict could develop if two or more styles define the same attribute differently. In this case, you can resolve the conflict by applying styles to the element in the following order, according to the Cascading Style Sheets (CSS) selector used to define the style:
#Element
#Class attribute
#ID attribute
#Inline styles

When two or more selectors pertain to an element, a style defined later takes precedence over a style defined earlier. For more information, see Introduction to Cascading Style Sheets.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML]


}}
{{See_Also_Section
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}