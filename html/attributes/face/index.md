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
|Description=This example sets the typeface family using the '''FACE''' attribute and the '''face''' property.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/face.htm
|Code=
&lt;FONT FACE{{=}}"Arial" ID{{=}}oFont&gt;
:
&lt;SCRIPT&gt;
    alert(oFont.face + "\n" + "When you click this, the font will change");
    oFont.face {{=}} 'Courier';
    alert(oFont.face + "\n" + "The font has changed.");
&lt;/SCRIPT&gt;
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 15.2.2 (Deprecated)


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>baseFont</code>
*<code>font</code>
*<code>[[css/properties/font-family|fontFamily]]</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}