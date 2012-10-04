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
|Description=This example uses the '''ALT''' attribute to indicate that the icon displayed denotes a read/write property.
|LiveURL=
|Code=
&lt;IMG SRC{{=}}"http://example.microsoft.com/rw.png" ALT{{=}}"Read/Write Property"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The text is used to replace the graphic for text-only browsers and to display in the window before the graphic has loaded. The text also acts as a ToolTip if the [[html/attributes/title|'''title''']] is not set when the user hovers the mouse over the graphic.
Alternate text should be provided whenever the graphic is not rendered. Alternate text is mandatory for Level 0 documents.
In Microsoft Internet Explorer 6, This property now applies to the '''object''' object.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 13.8


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>object</code>
*<code>applet</code>
*<code>area</code>
*<code>input</code>
*<code>input type{{=}}image</code>
*<code>img</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}