{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=x|Data type=Integer|Description=|Optional=}}
{{Method Parameter|Name=y|Data type=Integer|Description=|Optional=}}
{{Method Parameter|Name=w|Data type=Integer|Description=|Optional=}}
{{Method Parameter|Name=h|Data type=Integer|Description=|Optional=}}
{{Method Parameter|Name=pElement|Data type=VARIANT|Description=|Optional=}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to use the '''show''' method to create and display a pop-up window.
|LiveURL=
|Code=
&lt;html&gt;
&lt;head&gt;
&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
var oPopup {{=}} window.createPopup();
function window_onload() {
    var oPopupBody {{=}} oPopup.document.body;
	oPopupBody.style.backgroundColor {{=}} "lightyellow";
	oPopupBody.style.border {{=}} "solid black 1px";    
    oPopupBody.innerHTML {{=}} "Display some &lt;B&gt;HTML&lt;/B&gt; here.";
    oPopup.show(100, 100, 200, 50, document.body);}
&lt;/SCRIPT&gt;
&lt;/head&gt;
&lt;body onload{{=}}"window_onload();"&gt;
&lt;/body&gt;
&lt;/html&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
A '''popup''' object is set to the same zoom level as the parent window.
Windows Internet Explorer 8. Pop-up windows zoom by default; this behavior cannot be changed. This only applies to pop-up windows created with [[dom/methods/createPopup|'''createPopup''']].
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>popup</code>
*<code>Reference</code>
*<code>[[dom/methods/createPopup|createPopup]]</code>
*<code>[[dom/methods/hide|hide]]</code>
*<code>[[dom/properties/document|document]]</code>
*<code>[[dom/properties/isOpen|isOpen]]</code>
*<code>Conceptual</code>
*<code>Using the Popup Object</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}