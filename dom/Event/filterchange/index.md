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
|Description=This example uses the '''onfilterchange''' event to trigger a filter effect. When the document loads, the block of text is erased using a checkerboard-down Transition. Once the checkerboard Transition is complete, the image is made visible using a box-in Transition.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/filters.htm
|Code=
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;TITLE&gt;Microsoft Cascading Style Sheet Controls Samples&lt;/TITLE&gt;
&lt;/HEAD&gt;
&lt;body&gt;
&lt;h2&gt;Some text filters out (checkerboard), and at its completion 
an image filters in (box-in).  Refresh repeats.&lt;/h2&gt;
&lt;Div ID{{=}}"TextRegion" STYLE{{=}}"Position: absolute; border: solid red; 
    background-color: lightblue; LEFT: 0; TOP: 100; WIDTH: 100%; 
    VISIBILITY: visible; FILTER: revealTrans(Transition {{=}} 11, 
    Duration {{=}} 1.25)"&gt;
Text that will filter upon document load.&lt;br&gt;
Text that will filter upon document load.&lt;br&gt;
Text that will filter upon document load.&lt;br&gt;
Text that will filter upon document load.&lt;br&gt;
Text that will filter upon document load.&lt;br&gt;
Text that will filter upon document load.&lt;br&gt;
Text that will filter upon document load.
&lt;/DIV&gt;
&lt;DIV ID{{=}}"ImageRegion" STYLE{{=}}"Position: absolute; border: solid red;
    LEFT: 0; TOP: 100; WIDTH: 30%; VISIBILITY: hidden; 
    FILTER: revealTrans(Transition {{=}} 0, Duration {{=}} 1.25)"&gt;
&lt;IMAGE id{{=}}image1 SRC{{=}}"/workshop/samples/author/graphics/dhtml/blupan.png"&gt;
&lt;/DIV&gt;
&lt;SCRIPT LANGUAGE{{=}}VBScript&gt;
Sub Window_onload
    Call TextRegion.filters.revealTrans.Apply ()
    Call ImageRegion.filters.revealTrans.Apply()
    Call Start
End Sub
Sub Start
   TextRegion.style.visibility {{=}} "hidden"
   ImageRegion.style.visibility {{=}} "visible"
   Call TextRegion.filters.revealTrans.Play()
End Sub
Sub TextRegion_onfilterchange
   if TextRegion.filters.revealTrans.Status {{=}} 0 then
      Call ImageRegion.filters.revealTrans.Play(1.5)
   End If
End Sub
&lt;/SCRIPT&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Signals that the filter on an object has changed state.
To invoke this event, do one of the following:
*Change the filter state.

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
*<code>abbr</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>address</code>
*<code>applet</code>
*<code>area</code>
*<code>b</code>
*<code>base</code>
*<code>baseFont</code>
*<code>bdo</code>
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
*<code>del</code>
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
*<code>ins</code>
*<code>isIndex</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>link</code>
*<code>listing</code>
*<code>map</code>
*<code>marquee</code>
*<code>menu</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>noBR</code>
*<code>noFrames</code>
*<code>noScript</code>
*<code>object</code>
*<code>ol</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>q</code>
*<code>rt</code>
*<code>ruby</code>
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
*<code>title</code>
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>wbr</code>
*<code>xml</code>
*<code>xmp</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}