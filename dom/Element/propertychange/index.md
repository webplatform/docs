{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary,  spec, and compat
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Interface=dom/Element
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example demonstrates how to use the '''onpropertychange''' event to determine the name and value of an updated property.
|Code=&lt;html&gt;
&lt;head&gt;
&lt;script type{{=}}"text/javascript"&gt;
function changeProp()
{
    oProp.value {{=}} sText.value;
}
function changeCSSProp()
{
    if(oSelect.selectedIndex{{=}}{{=}}0) oStyleProp.style.color{{=}} "white";
    else oStyleProp.style.color {{=}} "black";
    oStyleProp.style.backgroundColor {{=}} oSelect.value;
}
function Results(){
    sSrc.innerText {{=}} event.srcElement.id;
    sProperty.innerText {{=}} event.propertyName;
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div style{{=}}"background: #eeeeee; padding: 10px;"&gt;
	Click the button below to change its 'Value' property to the string specified 
	in the text box.&lt;br&gt;&lt;br&gt;
  &lt;input type{{=}}"text" style{{=}}"width: 250px" id{{=}}"sText" value{{=}}"Enter Some Text"&gt;
	&amp;nbsp;
  &lt;input type{{=}}"button" id{{=}}"oProp" onclick{{=}}"changeProp()" value{{=}}"Change property" onpropertychange{{=}}"Results();"&gt;
  &lt;p&gt;Click the button below to change its 'backgroundColor' Cascading Style Sheet 
	(CSS) property to the color specified in the drop-down list box.&lt;br&gt;
  &lt;select name{{=}}"oSelect" style{{=}}"width: 150px"&gt;
	    &lt;option value{{=}}"black" style{{=}}"color: black"&gt;Black&lt;/option&gt;
	    &lt;option value{{=}}"blue" style{{=}}"color: blue"&gt;Blue&lt;/option&gt;
	    &lt;option value{{=}}"green" style{{=}}"color: green"&gt;Green&lt;/option&gt;
	    &lt;option value{{=}}"red" style{{=}}"color: red"&gt;Red&lt;/option&gt;
  &lt;/select&gt;&amp;nbsp;
  &lt;input type{{=}}"button" id{{=}}"oStyleProp" onclick{{=}}"changeCSSProp()" value{{=}}"Change property" onpropertychange{{=}}"Results();"&gt;&lt;/p&gt;
  &lt;br&gt;&lt;br&gt;
  &lt;div style{{=}}"border: 1px solid #cccccc; width: 100%; padding: 10px; background: white;"&gt;
    &lt;b&gt;Source object:&lt;/b&gt; &lt;span id{{=}}"sSrc" style{{=}}"color: red;"&gt;&lt;/span&gt;&lt;br&gt;
    &lt;b&gt;Property Name:&lt;/b&gt; &lt;span id{{=}}"sProperty" style{{=}}"color: red;"&gt;&lt;/span&gt;
  &lt;/div&gt;
&lt;/div&gt;
&lt;br&gt;
&lt;br&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onpropertychangeEX.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''onpropertychange''' event fires when properties of an object, expando, or style sub-object change. To retrieve the name of the changed property, use the '''TransitionEvent''' object's [[dom/TransitionEvent/propertyName|'''propertyName''']] property. This property returns a read-only string of the name of the property that has changed. In the case of Cascading Style Sheets (CSS) properties, the property name is prefixed with <code>style</code>. For example, if the CSS property [[css/cssom/properties/pixelLeft|'''pixelLeft''']] is altered, the value of <code>window.event.propertyName</code> is '''style.left'''. By contrast, if the non-CSS property [[html/attributes/name (frames)|'''name''']] is altered, the value of <code>window.event.propertyName</code> is '''name'''.
When the '''onpropertychange''' event fires, the '''srcElement''' property of the '''event''' object is set to the object whose property has changed.
'''Note'''  Changing the [[dom/HTMLElement/innerText|'''innerText''']] or [[dom/HTMLElement/innerHTML|'''innerHTML''']] of child elements will not cause the '''onpropertychange''' event to fire for the parent element.
Sends notification when a property changes.
To invoke this event, do one of the following:
*Cause a property to change value.

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