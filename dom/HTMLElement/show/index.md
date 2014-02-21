{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=any
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=any
|Optional=No
}}{{Method Parameter
|Name=w
|Data type=any
|Optional=No
}}{{Method Parameter
|Name=h
|Data type=any
|Optional=No
}}{{Method Parameter
|Name=pElement
|Data type=VARIANT
|Optional=No
}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to use the '''show''' method to create and display a pop-up window.
|Code=&lt;html&gt;
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
}}
}}
{{Notes_Section
|Notes====Remarks===
A '''popup''' object is set to the same zoom level as the parent window.
Windows Internet Explorer 8. Pop-up windows zoom by default; this behavior cannot be changed.
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.
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