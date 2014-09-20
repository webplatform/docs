{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=compatibility, clean-up of MSDN sections to fit WPD headers
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The click event is triggered for an element when it is activated by a mouse click or by another user action that normally has the same effect as a mouse click.}}
{{Event
|Event_applies_to=dom/MouseEvent
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Default_action=
|Content=
|Interface=dom/MouseEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''event''' object to gain information about the origin of the click. In addition, it cancels the default action to prevent navigation of [[html/elements/a|'''anchor''']] elements, unless the SHIFT key is pressed. Normally a Shift+Click opens the target of a link in a new window; however, the script replaces the current document by setting the [[dom/Location|'''location''']] of the '''window''' object.
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
|Usage=
|Notes====Remarks===
If the user clicks the left mouse button, the '''onclick''' event for an object occurs only if the mouse pointer is over the object and an [[dom/MouseEvent/mousedown|'''onmousedown''']] and an [[dom/MouseEvent/mouseup|'''onmouseup''']] event occur in that order. For example, if the user clicks the mouse on the object but moves the mouse pointer away from the object before releasing, no '''onclick''' event occurs.
The '''onclick''' event changes the value of a control in a group. This change initiates the event for the group, not for the individual control. For example, if the user clicks a radio button or check box in a group, the '''onclick''' event occurs after the [[dom/Event/beforeupdate|'''onbeforeupdate''']] and [[dom/Event/afterupdate|'''onafterupdate''']] events for the control group.
If the user clicks an object that can receive the input focus but does not already have the focus, the [[dom/HTMLElement/focus|'''onfocus''']] event occurs for that object before the '''onclick''' event. If the user double-clicks the left mouse button in a control, an [[dom/MouseEvent/dblclick|'''ondblclick''']] event occurs immediately after the '''onclick''' event.
Although the '''onclick''' event is available on a large number of HTML elements, if a document is to be accessible to keyboard users, you should restrict its use to the [[html/elements/a|'''a''']], '''input''', '''area''', and '''button''' elements. These elements automatically allow keyboard access through the TAB key, making documents that use the elements accessible to keyboard users. For more information, please see the section on writing accessible Dynamic HTML.
Initiates any action associated with the object. For example, if the user clicks an [[html/elements/a|'''a''']] object, the client loads the document specified by the [[html/attributes/href|'''href''']] property. To cancel the default behavior, set the [[dom/BeforeUnloadEvent/returnValue|'''returnValue''']] property to FALSE.
To invoke this event, do one of the following:
*Click the object.
*Invoke the [[dom/MouseEvent/click|'''click''']] method.
*Press the ENTER key in a form.
*Press the access key for a control.
*Select an item in a combo box or list box by clicking the left mouse button or by pressing the arrow keys and then pressing the ENTER key.

===Compatibility===
====Internet Explorer 8 & 9====
Internet Explorer 8 & 9 suffer from a bug where elements with a computed <code>[[css/properties/background-color|background-color]]</code> of <code>transparent</code> that are overlaid on top of other element(s) won't receive <code>click</code> events. Any '''click''' events will be fired at the underlying element(s) instead. See [http://jsfiddle.net/YUKma/show/ this live example] for a demonstration.

Known workarounds for this bug:
* For IE9 only:
** Set [[css/properties/background-color|<code>background-color</code>]]<code>: rgba(0,0,0,0)</code>
** Set [[css/properties/opacity|<code>opacity</code>]]<code>: 0</code> and an explicit <code>[[css/properties/background-color|background-color]]</code> other than <code>transparent</code>
* For IE8 and IE9
** Set [http://msdn.microsoft.com/en-us/library/ms532847(v=vs.85).aspx <code>filter</code>]<code>: alpha(opacity=0);</code> and an explicit <code>[[css/properties/background-color|background-color]]</code> other than <code>transparent</code>
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
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}