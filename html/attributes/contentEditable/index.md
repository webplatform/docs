{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info

|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets or retrieves the string that indicates whether the user can edit the content of the object.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=In the following example, setting the 
'''DIV''' elements to have 
<code>100%</code> [[css/properties/height|'''height''']] 
and [[css/properties/width|'''width''']] makes all content within 
the borders of the cells editable.
|Code=&lt;P&gt;Table 1 Editable&lt;/P&gt;&lt;BR/&gt;
&lt;TABLE BORDER{{=}}1 WIDTH{{=}}80%&gt;
&lt;THEAD&gt;
&lt;TR&gt;
&lt;TH&gt;&lt;DIV CONTENTEDITABLE STYLE{{=}}"height: 100%; width: 100%;"&gt;Heading 1 &lt;DIV&gt;&lt;/TH&gt;
&lt;TH&gt;&lt;DIV CONTENTEDITABLE STYLE{{=}}"height: 100%; width: 100%;"&gt;Heading 2 &lt;DIV&gt;&lt;/TH&gt;
&lt;/TR&gt;
&lt;/THEAD&gt;
&lt;TBODY&gt;
&lt;TR&gt;
&lt;TD&gt;&lt;DIV CONTENTEDITABLE STYLE{{=}}"height: 100%; width: 100%;"&gt;Row 1, Column 1 text.&lt;DIV&gt;&lt;/TD&gt;
&lt;TD&gt;&lt;DIV CONTENTEDITABLE STYLE{{=}}"height: 100%; width: 100%;"&gt;Row 1, Column 2 text.&lt;DIV&gt;&lt;/TD&gt;
&lt;/TR&gt;
&lt;TR&gt;
&lt;TD&gt;&lt;DIV CONTENTEDITABLE STYLE{{=}}"height: 100%; width: 100%;"&gt;Row 2, Column 1 text.&lt;DIV&gt;&lt;/TD&gt;
&lt;TD&gt;&lt;DIV CONTENTEDITABLE STYLE{{=}}"height: 100%; width: 100%;"&gt;Row 2, Column 2 text.&lt;DIV&gt;&lt;/TD&gt;
&lt;/TR&gt;
&lt;/TBODY&gt;
&lt;/TABLE&gt;
}}{{Single Example
|Description=The following example shows how to use the '''contentEditable''' property to control whether the user can edit the content of the object.
|Code=&lt;HEAD&gt;
&lt;SCRIPT&gt;
function chgSpan() {
    currentState {{=}} oSpan.isContentEditable;
    newState {{=}} !currentState;
    oSpan.contentEditable {{=}} newState;
    oCurrentValue.innerText {{=}} newState;
    newState{{=}}{{=}}false ? oBtn.innerText{{=}}"Enable Editing" :
        oBtn.innerText{{=}}"Disable Editing"
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY onload{{=}}"oCurrentValue.innerText {{=}} oSpan.isContentEditable;"&gt;
&lt;P&gt;Click the button to enable or disable SPAN content editing.&lt;/P&gt;
&lt;P&gt;
&lt;BUTTON ID{{=}}"oBtn" onclick{{=}}"chgSpan()"&gt;Enable Editing&lt;/BUTTON&gt;
&lt;/P&gt;
&lt;P&gt;&lt;SPAN ID{{=}}"oSpan"&gt;You can edit this text.&lt;/SPAN&gt;&lt;/P&gt;
SPAN can be edited: &lt;SPAN ID{{=}}"oCurrentValue"&gt;&lt;/SPAN&gt;
&lt;/BODY&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/contentEditableEX2.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Child elements do not inherit this attribute unless they have layout. Use the [[css/cssom/properties/hasLayout|'''hasLayout''']] property to determine if an object has layout.
If this attribute is applied to a '''BODY''' element, it has the same effect as setting the [[dom/properties/designMode|'''designMode''']] property of the [[dom/Document|'''Document''']] object.
Elements with the [[dom/properties/disabled (redundant)|'''disabled''']] attribute set to <code>false</code> do not respond to the '''contentEditable''' attribute.
If this attribute is applied to the [[html/elements/a|'''A''']] element, the default functionality of the '''A''' element will be lost while ''p'' is set to the value of <code>true</code>.
If this attribute is applied to the '''MARQUEE''' element, the default functionality of the '''MARQUEE''' element will be lost while ''p'' is set to the value of <code>true</code>.
Though the [[html/elements/table|'''TABLE''']], 
'''COL''', 
'''COLGROUP''', 
'''TBODY''', '''TD''', 
'''TFOOT''', '''TH''', 
'''THEAD''', and '''TR''' 
elements cannot be set as content editable directly, a content editable 
'''SPAN''', or  '''DIV''' 
element can be placed inside the individual table cells 
('''TD''' and '''TH''' 
elements).   See the example below.
'''Security Warning:  '''Users can change the contents of a document when the '''contentEditable''' property is set to TRUE. Using this property incorrectly can compromise the security of your application. Incorrect use of the '''contentEditable''' property might include not validating user input. If you do not validate user input, a malicious user can inject control characters or script that can harm your data. You should take routine precautions against displaying unvalidated user input. For more information, see Security Considerations: Dynamic HTML.
Windows Internet Explorer 8 and later. When a webpage is displayed in IE8 Standards mode, an object cannot receive focus when ''p'' is set to <code>false</code>. When pages are displayed in earlier document compatibility modes, objects can receive focus when ''p'' is <code>false</code>.
|Import_Notes====Syntax===
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=4.0+
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.0+
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=5.5+
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.0+
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.1+
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=3.0+
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0+
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0+
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15.0+
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=5.0+
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|External_links=* [http://demo.xpertdeveloper.com/contenteditable-attribute/ Contenteditable Demo]
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[html/elements/a|a]]</code>
*<code>abbr</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>address</code>
*<code>b</code>
*<code>bdo</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
*<code>button</code>
*<code>center</code>
*<code>cite</code>
*<code>code</code>
*<code>custom</code>
*<code>dd</code>
*<code>del</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>dt</code>
*<code>em</code>
*<code>fieldSet</code>
*<code>font</code>
*<code>form</code>
*<code>hn</code>
*<code>i</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}text</code>
*<code>ins</code>
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
*<code>q</code>
*<code>rt</code>
*<code>ruby</code>
*<code>s</code>
*<code>samp</code>
*<code>small</code>
*<code>span</code>
*<code>strike</code>
*<code>strong</code>
*<code>sub</code>
*<code>sup</code>
*<code>textArea</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>xmp</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}