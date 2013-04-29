{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
|Editorial notes=The click event refers to the type of event that is triggered for an element when it is clicked.
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/Element
|Interface=dom/objects/MouseEvent
|Target=dom/Element
|Default_action=
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''event''' object to gain information about the origin of the click. In addition, it cancels the default action to prevent navigation of [[html/elements/a|'''anchor''']] elements, unless the SHIFT key is pressed. Normally a Shift+Click opens the target of a link in a new window; however, the script replaces the current document by setting the [[dom/location|'''location''']] of the '''window''' object.
|Code=&lt;script type{{=}}"text/javascript"&gt;
/* This code cancels the event. If the click occurs in an anchor
   and the SHIFT key is down, the document is navigated. */
function clickIt()  
{
    var e {{=}} window.event.srcElement
    txtName.value {{=}} e.tagName;
    txtType.value {{=}} e.type;
    if ((e.tagName {{=}}{{=}} "A") &amp;&amp; 
        (window.event.shiftKey)) {
        window.location.href {{=}} e.href;
    }
    
    window.event.returnValue {{=}} false; 
}
&lt;/script&gt;
&lt;body onclick{{=}}"clickIt()"&gt;
&lt;p&gt;To follow a link, click while pressing the SHIFT key.&lt;/p&gt;
&lt;a href{{=}}"about:blank"&gt;Click Here&lt;/a&gt;
&lt;textarea name{{=}}"txtName"&gt;&lt;/textarea&gt; &lt;textarea name{{=}}"txtType"&gt;&lt;/textarea&gt;
&lt;/body&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onclickEX.htm
}}{{Single Example
|Language=HTML
|Description=This example shows how to bind the '''onclick''' event to grouped controls.
|Code=&lt;head&gt;
&lt;script type{{=}}"text/javascript"&gt;
function CookieGroup() 
{
txtOutput.value {{=}} window.event.srcElement.value;
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;!-- Controls are grouped by giving them the same NAME but unique IDs. --&gt;
&lt;p&gt;Grouped Radio Buttons&lt;br&gt;
&lt;input type{{=}}"radio" 
    name{{=}}"rdoTest" 
    id{{=}}"Cookies" 
    value{{=}}"accept_cookies" 
    checked 
    onclick{{=}}"CookieGroup()"&gt;&lt;br&gt;
&lt;input type{{=}}"radio" 
    name{{=}}"rdoTest" 
    id{{=}}"NoCookies" 
    value{{=}}"refuse_cookies" 
    onclick{{=}}"CookieGroup()"&gt;&lt;br&gt;
&lt;/p&gt;
&lt;p&gt;Ungrouped Radio Button&lt;br&gt;
&lt;input type{{=}}"radio" 
    name{{=}}"rdoTest1" 
    value{{=}}"chocolate-chip_cookies" 
    onclick{{=}}"CookieGroup()"&gt;&lt;br&gt;
&lt;/p&gt;
&lt;p&gt;Value of control on which the onclick event has fired&lt;br&gt;
&lt;textarea name{{=}}"txtOutput" style{{=}}"width: 250px"&gt;&lt;/textarea&gt; &lt;/p&gt;
&lt;/body&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onclickEX1.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
If the user clicks the left mouse button, the '''onclick''' event for an object occurs only if the mouse pointer is over the object and an [[dom/events/mousedown|'''onmousedown''']] and an [[dom/events/mouseup|'''onmouseup''']] event occur in that order. For example, if the user clicks the mouse on the object but moves the mouse pointer away from the object before releasing, no '''onclick''' event occurs.
The '''onclick''' event changes the value of a control in a group. This change initiates the event for the group, not for the individual control. For example, if the user clicks a radio button or check box in a group, the '''onclick''' event occurs after the [[dom/events/beforeupdate|'''onbeforeupdate''']] and [[dom/events/afterupdate|'''onafterupdate''']] events for the control group.
If the user clicks an object that can receive the input focus but does not already have the focus, the [[dom/events/focus|'''onfocus''']] event occurs for that object before the '''onclick''' event. If the user double-clicks the left mouse button in a control, an [[dom/events/dblclick|'''ondblclick''']] event occurs immediately after the '''onclick''' event.
Although the '''onclick''' event is available on a large number of HTML elements, if a document is to be accessible to keyboard users, you should restrict its use to the [[html/elements/a|'''a''']], '''input''', '''area''', and '''button''' elements. These elements automatically allow keyboard access through the TAB key, making documents that use the elements accessible to keyboard users. For more information, please see the section on writing accessible Dynamic HTML.
Initiates any action associated with the object. For example, if the user clicks an [[html/elements/a|'''a''']] object, the client loads the document specified by the [[html/attributes/href|'''href''']] property. To cancel the default behavior, set the [[dom/properties/returnValue|'''returnValue''']] property of the '''event''' object to FALSE.
To invoke this event, do one of the following:
*Click the object.
*Invoke the [[dom/methods/click|'''click''']] method.
*Press the ENTER key in a form.
*Press the access key for a control.
*Select an item in a combo box or list box by clicking the left mouse button or by pressing the arrow keys and then pressing the ENTER key.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 18.2.3


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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>abbr</code>
*<code>[[html/elements/acronym|acronym]]</code>
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
*<code>map</code>
*<code>marquee</code>
*<code>menu</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>noBR</code>
*<code>object</code>
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
*<code>[[svg/elements/svg|SVGSVGElement]]</code>
*<code>[[dom/methods/click|click]]</code>
*<code>[[dom/events/msgesturetap|onmsgesturetap]]</code>
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}