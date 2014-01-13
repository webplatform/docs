{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Returns the first element that matches the provided selector.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=selectors
|Data type=String
|Description=A selector, or multiple selectors (separated by commas).
|Optional=No
}}
|Method_applies_to=dom/Element
|Example_object_name=element
|Return_value_name=element
|Javascript_data_type=DOM Node
|Return_value_description=A DOM element node, or null if the search cannot find an element that matches the selector string.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example illustrates how the selectors in the selector string
are scoped to the entire document. The variable <code>e</code>
contains the span even though the provided selector references
the P element, which is outside the scope of the starting DIV element.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
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
}}
}}
{{Notes_Section
|Notes=The document search order is depth-first. This method returns the first element found. To find all matching nodes, use [[css/selectors api/querySelectorAll|'''querySelectorAll''']].
The scope of the returned element node is limited to the descendants of the starting element node. If the starting element is [[dom/Document|Document]], the search returns nodes from the entire document.
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
Selectors are described in detail in Understanding CSS Selectors and [http://www.w3.org/TR/css3-selectors/ W3C Selectors].
Calling this method with an unknown selector (due to the browser not implementing it, or due to typo and such) may throw an exception.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Selectors API Level 1
|URL=http://www.w3.org/TR/selectors-api
|Status=Proposed Recommendation
|Relevant_changes=Section 6.1
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.5
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=16
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=9
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=10
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=5.0
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Any
|Version=Any
|Note=The returned elements will only match selector strings that the running browser supports. Look at any individual selector for compatibility information. Some advanced selector may cause the call to throw an exception, due to syntax errors.
}}
}}
{{See_Also_Section
|Topic_clusters=Selectors
|Manual_sections====Related pages (MSDN)===
*[[dom/Document|Document]]
*[[html/elements/a|a]]
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
*[[html/elements/table|table]]
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
*[[css/selectors api/querySelectorAll|querySelectorAll]]
*<code>Other Resources</code>
*[[http://go.microsoft.com/fwlink/p/?linkid{{=}}203783 W3C Selectors API]]
*[[http://go.microsoft.com/fwlink/p/?linkid{{=}}203764 W3C Selectors]]
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}