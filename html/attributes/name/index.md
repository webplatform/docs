{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info

|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to set the '''NAME''' attribute on a dynamically created [[html/elements/a|'''A''']] element.
|Code=var oAnchor {{=}} document.createElement("&lt;A NAME{{=}}'AnchorName'&gt;&lt;/A&gt;");
}}{{Single Example
|Description=The following example shows how to set the '''NAME''' attribute on a dynamically created [[html/elements/a|'''A''']] element.  This example assumes that ppvDocument is a valid '''IHTMLDocument2''' interface pointer, and ppvElement is a valid '''IHTMLElement''' interface pointer.
|Code=ppvDocument-&gt;createElement(CComBSTR("&lt;A NAME{{=}}'AnchorName'&gt;&lt;/A&gt;"), &amp;ppvElement)
}}{{Single Example
|Description=The following example shows how to set the '''NAME'''  dynamically on objects (option buttons) created with the [[dom/methods/createElement|'''createElement''']] method.
|Code=var inp {{=}} document.createElement('input');
	inp.setAttribute('type',  'radio');
	inp.setAttribute('name',  'Q'+count);
	inp.setAttribute('value', answers[i]);
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/Dyn_Name_Sample.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
When you submit a '''form''', use the '''name''' property to bind the value of the control.
The name is not the value that is displayed for the '''input type{{=}}button''', '''input type{{=}}reset''', and '''input type{{=}}submit''' input types. The internally stored value is  submitted with the form, not the displayed value.
When you submit a '''form''', use the '''name''' property to bind the value of the control. The name is not the value displayed for the '''input type{{=}}button''', '''input type{{=}}reset''', and '''input type{{=}}submit''' input types. The internally stored value is submitted with the '''form''', not the displayed value.
Microsoft JScript allows you to change the name at run time. This does not cause the name in the programming model to change in the collection of elements, but it does change the name that you use for submitting elements.
Windows Internet Explorer 8 and later. In IE8 Standards mode, dynamically setting the '''name''' attribute on an '''input type{{=}}radio''' button correctly applies that button to the same named group. For more information about IE8 mode, see Defining Document Compatibility.
In Internet Explorer 8 and later versions, you can set the '''NAME''' attribute at run time on elements that are dynamically created with the [[dom/methods/createElement|'''createElement''']] method. To create an element with a '''NAME''' attribute in earlier versions of Windows Internet Explorer, include the attribute and its value when you use the '''createElement''' method.
In Microsoft Internet Explorer 6 and later versions, this property applies to the [[dom/attributes|'''attribute''']] object.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 17.3
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
*<code>applet</code>
*<code>[[dom/attributes|attribute]]</code>
*<code>button</code>
*<code>embed</code>
*<code>form</code>
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
*<code>link</code>
*<code>map</code>
*<code>object</code>
*<code>rt</code>
*<code>ruby</code>
*<code>select</code>
*<code>textArea</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}