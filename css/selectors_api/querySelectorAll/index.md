{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Element
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

'''IHTMLDOMChildrenCollection'''

A collection of DOM
element nodes. The collection may be empty.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
This method differs from the [[css/selectors api/querySelector|'''querySelector''']]
method by returning a collection of DOM element nodes that
match the selector string, rather than only the first element found.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}142050 Selectors API Level 1], Section 6.1


===Parameters===
;''v'' [in]:Type: '''<b>BSTR'''</b>The selector string.
;''pel'' [out, retval]:Type: '''<b>IHTMLDOMChildrenCollection'''</b>A collection of DOMelement nodes. The collection may be empty.
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>[[html/elements/a|a]]</code>
*<code>address</code>
*<code>b</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
*<code>button</code>
*<code>caption</code>
*<code>center</code>
*<code>cite</code>
*<code>code</code>
*<code>col</code>
*<code>colGroup</code>
*<code>dd</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>dt</code>
*<code>em</code>
*<code>fieldSet</code>
*<code>form</code>
*<code>hn</code>
*<code>html</code>
*<code>i</code>
*<code>img</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}text</code>
*<code>isIndex</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>listing</code>
*<code>marquee</code>
*<code>menu</code>
*<code>noBR</code>
*<code>ol</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>s</code>
*<code>samp</code>
*<code>small</code>
*<code>span</code>
*<code>strike</code>
*<code>strong</code>
*<code>sub</code>
*<code>sup</code>
*<code>[[html/elements/table|table]]</code>
*<code>tBody</code>
*<code>td</code>
*<code>textArea</code>
*<code>tFoot</code>
*<code>th</code>
*<code>tHead</code>
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>xmp</code>
*<code>Reference</code>
*<code>[[css/selectors api/querySelector|querySelector]]</code>
*<code>IElementSelector</code>
*<code>Other Resources</code>
*<code>[http://go.microsoft.com/fwlink/p/?linkid{{=}}203783 W3C Selectors API]</code>
*<code>[http://go.microsoft.com/fwlink/p/?linkid{{=}}203764 W3C Selectors]</code>
|Topic_clusters=Selectors
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}