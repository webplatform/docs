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
|Description=This example uses the '''onchange''' event to retrieve the selected option of a '''select''' object.
|Code=&lt;body&gt;
&lt;form&gt;
  &lt;p&gt;Select a different option in the drop-down list box to trigger the onchange event.
  &lt;select name{{=}}"selTest" onchange{{=}}"alert('Index: ' + this.selectedIndex
     + '\nValue: ' + this.options[this.selectedIndex].value)"&gt;
  &lt;option value{{=}}"Books"&gt;Books&lt;/option&gt;
  &lt;option value{{=}}"Clothing"&gt;Clothing&lt;/option&gt;
  &lt;option value{{=}}"Housewares"&gt;Housewares&lt;/option&gt;
  &lt;/select&gt; &lt;/p&gt;
&lt;/form&gt;
&lt;/body&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onchangeEX.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
This event is fired when the contents are committed and not while the value is changing. For example, on a text box, this event is not fired while the user is typing, but rather when the user commits the change by leaving the text box that has focus. In addition, this event is executed before the code specified by [[dom/HTMLElement/blur|'''onblur''']] when the control is also losing the focus.
The '''onchange''' event does not fire when the selected option of the '''select''' object is changed programmatically.
Changed text selection is committed.
To invoke this event, do one of the following:
*Choose a different '''option''' in a '''select''' object using mouse or keyboard navigation.
*Alter text in the text area and then navigate out of the object.

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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}