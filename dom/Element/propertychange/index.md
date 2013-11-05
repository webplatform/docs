{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/Element
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Topics|Events}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example demonstrates how to use the '''onpropertychange''' event to determine the name and value of an updated property.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onpropertychangeEX.htm
|Code=
&lt;html&gt;
&lt;head&gt;
&lt;script type{{=}}"text/javascript"&gt;
function changeProp()
{
    oProp.value {{=}} sText.value;
}
function changeCSSProp()
{
    if(oSelect.selectedIndex{{=}}{{=}}0) oStyleProp.style.color{{=}} "white";
    else oStyleProp.style.color {{=}} "black";
    oStyleProp.style.backgroundColor {{=}} oSelect.value;
}
function Results(){
    sSrc.innerText {{=}} event.srcElement.id;
    sProperty.innerText {{=}} event.propertyName;
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div style{{=}}"background: #eeeeee; padding: 10px;"&gt;
	Click the button below to change its 'Value' property to the string specified 
	in the text box.&lt;br&gt;&lt;br&gt;
  &lt;input type{{=}}"text" style{{=}}"width: 250px" id{{=}}"sText" value{{=}}"Enter Some Text"&gt;
	&amp;nbsp;
  &lt;input type{{=}}"button" id{{=}}"oProp" onclick{{=}}"changeProp()" value{{=}}"Change property" onpropertychange{{=}}"Results();"&gt;
  &lt;p&gt;Click the button below to change its 'backgroundColor' Cascading Style Sheet 
	(CSS) property to the color specified in the drop-down list box.&lt;br&gt;
  &lt;select name{{=}}"oSelect" style{{=}}"width: 150px"&gt;
	    &lt;option value{{=}}"black" style{{=}}"color: black"&gt;Black&lt;/option&gt;
	    &lt;option value{{=}}"blue" style{{=}}"color: blue"&gt;Blue&lt;/option&gt;
	    &lt;option value{{=}}"green" style{{=}}"color: green"&gt;Green&lt;/option&gt;
	    &lt;option value{{=}}"red" style{{=}}"color: red"&gt;Red&lt;/option&gt;
  &lt;/select&gt;&amp;nbsp;
  &lt;input type{{=}}"button" id{{=}}"oStyleProp" onclick{{=}}"changeCSSProp()" value{{=}}"Change property" onpropertychange{{=}}"Results();"&gt;&lt;/p&gt;
  &lt;br&gt;&lt;br&gt;
  &lt;div style{{=}}"border: 1px solid #cccccc; width: 100%; padding: 10px; background: white;"&gt;
    &lt;b&gt;Source object:&lt;/b&gt; &lt;span id{{=}}"sSrc" style{{=}}"color: red;"&gt;&lt;/span&gt;&lt;br&gt;
    &lt;b&gt;Property Name:&lt;/b&gt; &lt;span id{{=}}"sProperty" style{{=}}"color: red;"&gt;&lt;/span&gt;
  &lt;/div&gt;
&lt;/div&gt;
&lt;br&gt;
&lt;br&gt;
&lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''onpropertychange''' event fires when properties of an object, [[dom/properties/expando|'''expando''']], or style sub-object change. To retrieve the name of the changed property, use the '''event''' object's [[dom/properties/propertyName2|'''propertyName''']] property. This property returns a read-only string of the name of the property that has changed. In the case of Cascading Style Sheets (CSS) properties, the property name is prefixed with <code>style</code>. For example, if the CSS property [[css/cssom/properties/pixelLeft|'''pixelLeft''']] is altered, the value of <code>window.event.propertyName</code> is '''style.left'''. By contrast, if the non-CSS property [[html/attributes/name (frames)|'''name''']] is altered, the value of <code>window.event.propertyName</code> is '''name'''.
When the '''onpropertychange''' event fires, the '''srcElement''' property of the '''event''' object is set to the object whose property has changed.
'''Note'''  Changing the [[dom/properties/innerText|'''innerText''']] or [[dom/properties/innerdom/innerHTML|'''innerHTML''']] of child elements will not cause the '''onpropertychange''' event to fire for the parent element.
Sends notification when a property changes.
To invoke this event, do one of the following:
*Cause a property to change value.

The ''pEvtObj'' parameter is required for the following interfaces:
*'''HTMLAnchorEvents2'''
*'''HTMLAreaEvents2'''
*'''HTMLButtonElementEvents2'''
*'''HTMLControlElementEvents2'''
*'''HTMLDocumentEvents2'''
*'''HTMLElementEvents2'''
*'''HTMLFormElementEvents2'''
*'''HTMLImgEvents2'''
*'''HTMLFrameSiteEvents2'''
*'''HTMLInputFileElementEvents2'''
*'''HTMLInputImageEvents2'''
*'''HTMLInputTextElementEvents2'''
*'''HTMLLabelEvents2'''
*'''HTMLLinkElementEvents2'''
*'''HTMLMapEvents2'''
*'''HTMLMarqueeElementEvents2'''
*'''HTMLObjectElementEvents2'''
*'''HTMLOptionButtonElementEvents2'''
*'''HTMLScriptEvents2'''
*'''HTMLSelectElementEvents2'''
*'''HTMLStyleElementEvents2'''
*'''HTMLTableEvents2'''
*'''HTMLTextContainerEvents2'''
*'''HTMLWindowEvents2'''

|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>address</code>
*<code>applet</code>
*<code>area</code>
*<code>b</code>
*<code>bdo</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
*<code>button</code>
*<code>caption</code>
*<code>center</code>
*<code>cite</code>
*<code>code</code>
*<code>comment</code>
*<code>custom</code>
*<code>dd</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>[[dom/document|document]]</code>
*<code>dt</code>
*<code>em</code>
*<code>embed</code>
*<code>fieldSet</code>
*<code>font</code>
*<code>form</code>
*<code>hn</code>
*<code>hr</code>
*<code>i</code>
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
*<code>listing</code>
*<code>map</code>
*<code>marquee</code>
*<code>menu</code>
*<code>noBR</code>
*<code>object</code>
*<code>ol</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>s</code>
*<code>samp</code>
*<code>script</code>
*<code>select</code>
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
*<code>[[dom/properties/propertyName2|propertyName]]</code>
*<code>srcElement</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}