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
{{Topics|Event}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The example uses the '''srcElement''' property of the event object to determine which marquee has fired the '''onfinish''' event.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onfinishEX.htm
|Code=
&lt;body&gt;
&lt;label&gt;mqLooper1&lt;/label&gt;
&lt;marquee id{{=}}"mqLooper1" loop{{=}}"2" 
    onfinish{{=}}"alert(event.srcElement.id + ' finished looping.')"&gt; 
this marquee loops twice &lt;/marquee&gt; 
&lt;hr&gt;
&lt;label&gt;mqLooper2&lt;/label&gt;
&lt;marquee id{{=}}"mqLooper2" loop{{=}}"5" 
onfinish{{=}}"alert(event.srcElement.id + ' finished looping.')"&gt; 
this marquee loops five times &lt;/marquee&gt;
&lt;/body&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
A value greater than 1 and less than infinity must be set on the [[html/attributes/loop|'''LOOP''']] attribute for this event to fire.
Marquee ceases to loop.
To invoke this event, do one of the following:
*Specify a value for the [[html/attributes/loop|'''LOOP''']] attribute of the '''marquee''' object.

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
*<code>marquee</code>
*<code>Reference</code>
*<code>[[html/attributes/loop|loop]]</code>
*<code>[[dom/events/start|onstart]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}