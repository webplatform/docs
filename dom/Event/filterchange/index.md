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
|Description=This example uses the '''onfilterchange''' event to trigger a filter effect. When the document loads, the block of text is erased using a checkerboard-down Transition. Once the checkerboard Transition is complete, the image is made visible using a box-in Transition.
|Code=&lt;HTML&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/filters.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}