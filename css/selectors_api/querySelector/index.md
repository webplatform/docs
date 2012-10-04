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

'''IHTMLElement'''

A DOM element node,
or null if the search cannot find
an element that matches the selector string.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example illustrates how the selectors in the selector string
are scoped to the entire document. The variable <code>e</code>
contains the span even though the provided selector references
the P element, which is outside the scope of the starting DIV element.
|LiveURL=
|Code=
&lt;html&gt;  
&lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}8"&gt;
&lt;!-- To limit the search to descendants of an element only, --&gt;
&lt;!-- call the selectors API on the specific element of interest. --&gt;
&lt;body&gt;   
    &lt;p&gt;    
        &lt;div id{{=}}"apple"&gt;     
        &lt;span&gt;Some are sauce, some are pie.&lt;/span&gt;    
        &lt;/div&gt;   
    &lt;/p&gt;   
&lt;script&gt;    
    var div {{=}} document.getElementById("apple");    
    var   e {{=}} div.querySelector("p span");    // 'e' will select the span.    
    var   f {{=}} div.querySelector("p div");     // 'f' will be null because the div is not a descendent of 'div'
&lt;/script&gt;  
&lt;/body&gt; 
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The document search order is depth-first. This method returns the first element found. To find all matching nodes, use [[css/selectors api/querySelectorAll|'''querySelectorAll''']].
The scope of the returned element node is limited to the descendants of the starting element node. If the starting element is [[dom/document|'''document''']], the search returns nodes from the entire document.
This method does not return the starting element node. For example, <code>div.querySelector("p div")</code> will never return the '''DIV''' element that it starts with.
The pseudo-class selectors
[[css/selectors/pseudo-classes/:hover|''':hover''']],
[[css/selectors/pseudo-classes/:focus|''':focus''']],  
and
[[css/selectors/pseudo-classes/:active|''':active''']] 
are supported. Selectors that contain 
[[css/selectors/pseudo-classes/:visited|''':visited''']] or 
[[css/selectors/pseudo-classes/:link|''':link''']] are ignored and no elements are returned.
You can search namespaced elements using a selector syntax based on prefix 
instead of the namespaceURI, for example "nsPrefix \: element", 
where "nsPrefix" is the prefix of a given element.
Selectors are described in detail in Understanding CSS Selectors and [http://go.microsoft.com/fwlink/p/?linkid{{=}}203764 W3C Selectors].
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}142050 Selectors API Level 1], Section 6.1


===Parameters===
;''v'' [in]:Type: '''<b>BSTR'''</b>The selector string.
;''pel'' [out, retval]:Type: '''<b>IHTMLElement'''</b>A DOM element node,or null if the search cannot findan element that matches the selector string.
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
*<code>[[css/selectors api/querySelectorAll|querySelectorAll]]</code>
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