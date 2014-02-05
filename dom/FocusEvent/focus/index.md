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
|Event_applies_to=dom/FocusEvent
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Interface=dom/FocusEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''onfocus''' event to make '''INPUT_text''' and '''label''' objects more accessible. When the '''INPUT_text''' object has focus, the '''onfocus''' event fires and the [[css/properties/background-color|'''backgroundColor''']], [[css/properties/font-size|'''fontSize''']], and [[css/properties/font-weight|'''fontWeight''']] properties are changed to give the control more prominence.
|Code=...
&lt;style type{{=}}"text/css"&gt;
.normal {
	background-color: white;
	color: black;
	font-weight: normal;
	font-size: 8pt;
	font-family: Arial;
}
.accessible {
	background-color: silver;
	font-weight: bold;
	font-size: 10pt;
}
&lt;/style&gt;
&lt;script type{{=}}"text/javascript"&gt;
function fnSetStyle(){
   event.srcElement.className{{=}}"accessible";
   var oWorkLabel{{=}}eval(event.srcElement.id + "_label");
   oWorkLabel.className{{=}}"accessible";
}
&lt;/script&gt;
&lt;label for{{=}}"oInput" class{{=}}"normal" id{{=}}"oInput_label"&gt;Enter some text&lt;/label&gt;
&lt;input type{{=}}"text" class{{=}}"normal" onfocus{{=}}"fnSetStyle()" id{{=}}"oInput"&gt; 
...
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onfocusEX.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
'''Note'''  Using the [[dom/HTMLElement/setActive|'''setActive''']] method has no effect on document focus. Using the [[dom/FocusEvent/focus|'''focus''']] method on an individual element causes the element to gain focus and become the active element.
When one object loses activation and another object becomes the [[dom/Document/activeElement|'''activeElement''']], the '''onfocus''' event fires on the object becoming the '''activeElement''' only after the [[dom/FocusEvent/blur|'''onblur''']] event fires on the object losing activation. Use the focus events to determine when to prepare an object to receive input from the user.
Elements cannot receive focus until the document is finished loading.
For Microsoft Internet Explorer 5.5 and later, focus on a [[dom/Document|Document]], and the '''active element''' of a '''document''' can be managed separately. The synchronous events '''onactivate''' and '''ondeactivate''' provide better control for managing activation changes.
As of Microsoft Internet Explorer 5, browser elements retain focus within the current  history when the user returns to a page. To avoid firing the '''onfocus''' event unintentionally for an element when the document loads, invoke the '''focus''' method on another element.
As of Internet Explorer 5, you can force elements that do not implicitly receive focus to receive focus by adding them to the document tabbing order using the [[html/attributes/tabIndex|'''TABINDEX''']] attribute.
Sets focus to an object.
To invoke this event, do one of the following:
*Click an object.
*Use keyboard navigation.
*Invoke the [[dom/FocusEvent/focus|'''focus''']] method.
*Invoke the [[dom/HTMLElement/setActive|'''setActive''']] method.

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
*'''HTMLDocumentEvents4'''
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