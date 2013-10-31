{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/Event
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Event
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Topics|Events}}
{{Notes_Section
|Notes=
===Remarks===
Each document may have up to one active element.  Set the active element with the [[dom/methods/setActive|'''setActive''']] or [[dom/methods/focus|'''focus''']] methods.  Using the '''setActive''' method has no effect on document focus.  Using the '''focus''' method on an individual element causes the element to gain focus and become the active element.
Using the [[dom/methods/focus|'''focus''']] method on a document that does not have the focus moves the document to the front of the display. Additionally, the document's active element gains focus.
For a given display, only one element has focus at any given time.  Striking a key directly affects only the element with focus.  Events fired by that keystroke may be scripted to affect other documents and child elements.
With Microsoft Internet Explorer 5.5 and later, focus on a [[dom/document|'''document''']], and the [[dom/properties/activeElement|'''active element''']] of a '''document''' can be managed separately.  With Microsoft Internet Explorer 6 and later, use the '''onbeforeactivate''' event to cancel setting an element as active.  Canceling an element's '''onbeforeactivate''' event has three different behaviors, depending on the action which fired the event.
*When fired by a user clicking on the element, canceling will force the [[dom/methods/focus|'''focus''']] on the parent element and bubble up the chain until it hits a focusable element.
*When fired by a user tabbing through the document, canceling will force the [[dom/methods/focus|'''focus''']] on the next element in the taborder. Shift-tab will force the '''focus''' on the previous element in the taborder.
*When fired programmatically by the [[dom/methods/focus|'''focus''']] or the document.[[dom/methods/setActive|'''setActive''']] methods, canceling will have no effect.

'''Note'''  The '''onbeforeactivate''' event cannot be canceled when fired programmatically.
Change activation from the '''event'''.[[dom/properties/fromElement2|'''fromElement''']] to the '''event'''.'''srcElement'''.
To invoke this event, do one of the following:
*Click an element, other than the [[dom/properties/activeElement|'''active''']] element of the document.
*Use the keyboard to move focus from the active element to another element.
*Invoke the [[dom/methods/setActive|'''setActive''']] method on an element, when the element is not the active element.
*Invoke the [[dom/methods/focus|'''focus''']] method on an element, when the element is not the active element.

The ''pEvtObj'' parameter is required for the following interfaces:
*'''HTMLFrameSiteEvents2'''
*'''HTMLElementEvents'''
*'''HTMLElementEvents2'''
*'''HTMLLinkElementEvents'''
*'''HTMLLinkElementEvents2'''
*'''HTMLFormElementEvents'''
*'''HTMLFormElementEvents2'''
*'''HTMLImgEvents'''
*'''HTMLImgEvents2'''
*'''HTMLTextContainerEvents'''
*'''HTMLTextContainerEvents2'''
*'''HTMLAnchorEvents2'''
*'''HTMLLabelEvents'''
*'''HTMLLabelEvents2'''
*'''HTMLSelectElementEvents'''
*'''HTMLSelectElementEvents2'''
*'''HTMLInputTextElementEvents'''
*'''HTMLInputTextElementEvents2'''
*'''HTMLOptionButtonElementEvents'''
*'''HTMLOptionButtonElementEvents2'''
*'''HTMLButtonElementEvents'''
*'''HTMLButtonElementEvents2'''
*'''HTMLMarqueeElementEvents'''
*'''HTMLMarqueeElementEvents2'''
*'''HTMLControlElementEvents'''
*'''HTMLControlElementEvents2'''
*'''HTMLMapEvents'''
*'''HTMLMapEvents2'''
*'''HTMLAreaEvents'''
*'''HTMLAreaEvents2'''
*'''HTMLTableEvents'''
*'''HTMLTableEvents2'''
*'''HTMLScriptEvents'''
*'''HTMLScriptEvents2'''
*'''HTMLStyleElementEvents'''
*'''HTMLStyleElementEvents2'''
*'''HTMLInputFileElementEvents'''
*'''HTMLInputFileElementEvents2'''
*'''HTMLInputImageEvents'''
*'''HTMLInputImageEvents2'''
*'''HTMLDocumentEvents'''

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
*<code>input type{{=}}reset</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
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
*<code>xmp</code>
*<code>Reference</code>
*<code>[[dom/events/activate|onactivate]]</code>
*<code>[[dom/events/beforedeactivate|onbeforedeactivate]]</code>
*<code>[[dom/events/deactivate|ondeactivate]]</code>
*<code>[[dom/events/focusin|onfocusin]]</code>
*<code>[[dom/events/focusout|onfocusout]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}