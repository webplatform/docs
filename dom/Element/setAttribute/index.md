{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=strAttributeName|Data type=BSTR|Description='''String''' that specifies the name of the attribute.|Optional=}}
{{Method Parameter|Name=AttributeValue|Data type=VARIANT|Description=Variant that specifies the string, number, or Boolean to assign to the attribute.|Optional=}}
{{Method Parameter|Name=lFlags|Data type=Integer|Description='''Integer''' that specifies whether to use a case-sensitive search to locate the attribute. Can be one of the following values:|Optional=}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 8 and later. IE8 Standards mode enables several enhancements to the '''setAttribute''', [[dom/methods/getAttribute|'''getAttribute''']], and [[dom/methods/removeAttribute|'''removeAttribute''']] methods that are not available when pages are displayed in earlier document modes.
*The ''strAttributeName'' parameter requires the name of the desired content attribute and not the Document Object Model (DOM) attribute. 

For example, in IE8 mode, this method no longer requires ''strAttributeName'' to be <code>"className"</code> when setting, getting, or removing a [[dom/properties/className|'''CLASS''']] attribute. Earlier versions of Windows Internet Explorer and Internet Explorer 8 in compatibility mode still require ''strAttributeName'' to specify the corresponding DOM property name.
*The ''strAttributeName'' parameter is not case sensitive. As a result, the ''lFlags'' parameter is no longer supported and should not be used.
*The methods support event handlers. For example, the following code example defines an event handler to call a function called SomeFunction when the body of the page is loaded.
<div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>document.body.setAttribute('onload', 'SomeFunction()');</code></pre>
</div>

If the specified attribute is not already present, the '''setAttribute''' method adds the attribute to the object and sets the value.
If your pages are displayed in IE5 (Quirks) mode or IE7 Standards mode, be careful when spelling attribute names. If you set ''lFlags'' to <code>1</code> and the ''strAttributeName'' parameter does not have the same uppercase and lowercase letters as the attribute, a new attribute is created for the object. If two or more attributes have the same name, differing only in case, and ''lFlags'' is set to <code>0</code>, this method assigns values only to the first attribute created with this name. All other attributes of the same name are ignored.
Internet Explorer 8 and later. When pages are displayed in IE8 mode, the ''AttributeValue'' parameter only supports string values. Non-string values are not automatically converted to string values. For best results, formally convert values to strings before using them as parameter values. For example, do not attempt to pass an object directly to the ''AttributeValue'' parameter; call the object's '''toString''' method instead.
Use either '''VariantClear''' or '''SysFreeString''' with '''setAttribute''' to clear a '''Variant'''. '''VariantClear''' will set a variant to VT_EMPTY, but will not free its allocated memory.
The ''strAttributeName'' parameter requires the name of the desired content attribute.
The ''strAttributeName'' parameter is not case sensitive. As a result, the ''lFlags'' parameter is no longer supported and should not be used.
The ''AttributeValue'' parameter only supports string values. Non-string values are not automatically converted to string values. For best results, formally convert values to strings before using them as parameter values. For example, do not attempt to pass an object directly to the ''AttributeValue'' parameter; call the object's '''toString''' method instead.
The methods support event handlers. For example, the following code example defines an event handler to call a function called SomeFunction when the body of the document is loaded.
 <code>document.body.setAttribute('onload', 'SomeFunction()');</code>
[[dom/methods/removeAttribute|'''removeAttribute''']] always returns S_OK as an HRESULT value.  Check the ''pfSuccess'' parameter to determine if the attribute is successfully removed.
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
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
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
*<code>[[dom/userProfile|userProfile]]</code>
*<code>var</code>
*<code>wbr</code>
*<code>xmp</code>
*<code>Reference</code>
*<code>[[dom/methods/getAttribute|getAttribute]]</code>
*<code>[[dom/methods/removeAttribute|removeAttribute]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}