{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=strAttributeName|Data type=BSTR|Description='''String''' that specifies an attribute name.|Optional=}}
{{Method Parameter|Name=lFlags|Data type=Integer|Description='''Integer''' that specifies whether to use a case-sensitive search to locate the attribute. Can be one of the following values:|Optional=}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Boolean

Boolean

{| class="wikitable"
|-
!Return value
!Description
|-
|true
|The attribute was successfully removed.
|-
|false
|The attribute was not removed.
|}
 


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 8 and later. IE8 Standards mode enables several enhancements to the [[dom/methods/setAttribute|'''setAttribute''']], [[dom/methods/getAttribute|'''getAttribute''']], and '''removeAttribute''' methods that are not available when pages are displayed in earlier document modes:
*The ''strAttributeName'' parameter requires the name of the desired content attribute and not the Document Object Model (DOM) attribute. 

For example, in IE8 mode, this method no longer requires ''strAttributeName'' to be <code>"className"</code> when setting, getting, or removing a [[dom/properties/className|'''CLASS''']] attribute. Earlier versions of Windows Internet Explorer and Internet Explorer 8 in compatibility mode still require ''strAttributeName'' to specify the corresponding DOM property name.
*The ''strAttributeName'' parameter is not case sensitive. As a result, the ''lFlags'' parameter is no longer supported and should not be used.
*The methods support event handlers. For example, the following code example defines an event handler to call a function called SomeFunction when the body of the page is loaded.
<div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>document.body.setAttribute('onload', 'SomeFunction()');</code></pre>
</div>

'''removeAttribute''' always returns S_OK as an HRESULT value.  Check the ''pfSuccess'' parameter to determine if the attribute is successfully removed.
If your pages are displayed in IE5 (Quirks) mode or IE7 Standards mode, be careful when spelling attribute names. If two or more attributes have the same name—differing only in capitalization—and ''lFlags'' is set to <code>0</code>, this method removes only the last attribute to be created with this name. All other attributes of the same name are ignored.
The ''strAttributeName'' parameter requires the name of the desired content attribute and not the DOM attribute.
The ''strAttributeName'' parameter is not case sensitive. As a result, the ''lFlags'' parameter is no longer supported and should not be used.
The methods support event handlers. For example, the following code example defines an event handler to call a function called SomeFunction when the body of the page is loaded.
 <code>document.body.setAttribute('onload', 'SomeFunction()');</code>
'''removeAttribute''' always returns S_OK as an HRESULT value.  Check the ''pfSuccess'' parameter to determine if the attribute is successfully removed.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>address</code>
*<code>applet</code>
*<code>area</code>
*<code>b</code>
*<code>base</code>
*<code>baseFont</code>
*<code>bgSound</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
*<code>br</code>
*<code>button</code>
*<code>caption</code>
*<code>center</code>
*<code>cite</code>
*<code>code</code>
*<code>col</code>
*<code>colGroup</code>
*<code>comment</code>
*<code>custom</code>
*<code>dd</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>dt</code>
*<code>em</code>
*<code>embed</code>
*<code>fieldSet</code>
*<code>font</code>
*<code>form</code>
*<code>frame</code>
*<code>frameSet</code>
*<code>head</code>
*<code>hn</code>
*<code>hr</code>
*<code>html</code>
*<code>i</code>
*<code>iframe</code>
*<code>img</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}hidden</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}text</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>link</code>
*<code>listing</code>
*<code>map</code>
*<code>marquee</code>
*<code>menu</code>
*<code>meta</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>noBR</code>
*<code>object</code>
*<code>ol</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>s</code>
*<code>samp</code>
*<code>script</code>
*<code>select</code>
*<code>small</code>
*<code>span</code>
*<code>strike</code>
*<code>strong</code>
*<code>[[css/cssom/style|style]]</code>
*<code>sub</code>
*<code>sup</code>
*<code>[[html/elements/table|table]]</code>
*<code>tBody</code>
*<code>td</code>
*<code>textArea</code>
*<code>tFoot</code>
*<code>th</code>
*<code>tHead</code>
*<code>title</code>
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>wbr</code>
*<code>xmp</code>
*<code>Reference</code>
*<code>[[dom/methods/getAttribute|getAttribute]]</code>
*<code>[[dom/methods/setAttribute|setAttribute]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}