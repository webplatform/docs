{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/objects/Event
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
|Description=This example shows how to prevent a context menu from appearing by canceling the '''oncontextmenu''' event handler.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/oncontextmenu.htm
|Code=
&lt;span style{{=}}"width: 300px; background-color: blue; color: white;" 
    oncontextmenu{{=}}"return false"&gt;
The context menu never displays when you right-click in this box. &lt;/span&gt;
}}
{{Single_Example
|Description=Although '''area''' elements inherit the '''oncontextmenu''' event by way of the object hierarchy, they do not respond to right-click events in Internet Explorer. However, it is possible to imitate the desired behavior by using the [[dom/events/focus|'''onfocus''']] and [[dom/events/blur|'''onblur''']] events to determine the currently selected region and trigger the appropriate action in the context menu handler of the '''img''' itself. Although it isn't used by Internet Explorer, retain the '''oncontextmenu''' event attribute on the '''area''' elements for a fully cross-client implementation.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/oncontextmenuEX1.htm
|Code=
&lt;script type{{=}}"text/javascript"&gt;
var selectedArea {{=}} null;
function activate(e,f) {
    selectedArea {{=}} f ? e : null;
}
function menu(e) { 
    if (selectedArea)
        alert('right-click: ' + selectedArea.id); 
    else {
        // cross-client case
        if (e.tagName {{=}}{{=}} 'AREA')
            alert('right-click: ' + e.id); 
        else
            alert('right-click: ' + e.tagName);
    }
    return false; 
}
&lt;/script&gt;
&lt;map id{{=}}"Map0"&gt;
&lt;area id{{=}}"Area1" onfocus{{=}}"activate(this,true)" onblur{{=}}"activate(this,false)" 
    oncontextmenu{{=}}"return menu(this)" shape{{=}}"rect" coords{{=}}"100, 50, 200, 150" href{{=}}"..."/&gt;
&lt;/map&gt;
&lt;img src{{=}}"..." oncontextmenu{{=}}"return menu(this)" usemap{{=}}"#Map0" /&gt;  
}}}}
{{Notes_Section
|Notes=
===Remarks===
Opens the context menu. To cancel the default behavior, set the [[dom/properties/returnValue|'''returnValue''']] property of the '''event''' object to '''false'''.
To invoke this event, do one of the following:
*Right-click the object.

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
*<code>marquee</code>
*<code>menu</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>noBR</code>
*<code>ol</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>rt</code>
*<code>ruby</code>
*<code>s</code>
*<code>samp</code>
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
*<code>window</code>
*<code>xmp</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}