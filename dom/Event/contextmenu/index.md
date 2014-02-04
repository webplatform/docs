{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/Event
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Interface=dom/Event
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example shows how to prevent a context menu from appearing by canceling the '''oncontextmenu''' event handler.
|Code=&lt;span style{{=}}"width: 300px; background-color: blue; color: white;" 
    oncontextmenu{{=}}"return false"&gt;
The context menu never displays when you right-click in this box. &lt;/span&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/oncontextmenu.htm
}}{{Single Example
|Description=Although '''area''' elements inherit the '''oncontextmenu''' event by way of the object hierarchy, they do not respond to right-click events in Internet Explorer. However, it is possible to imitate the desired behavior by using the [[dom/HTLMElement/focus|'''onfocus''']] and [[dom/HTMLElement/blur|'''onblur''']] events to determine the currently selected region and trigger the appropriate action in the context menu handler of the '''img''' itself. Although it isn't used by Internet Explorer, retain the '''oncontextmenu''' event attribute on the '''area''' elements for a fully cross-client implementation.
|Code=&lt;script type{{=}}"text/javascript"&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/oncontextmenuEX1.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Opens the context menu. To cancel the default behavior, set the [[dom/BeforeUnloadEvent/returnValue|'''returnValue''']] property of the '''event''' object to '''false'''.
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
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.

===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}