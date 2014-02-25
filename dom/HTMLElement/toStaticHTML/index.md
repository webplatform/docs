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
|Name=bstrHTML
|Data type=BSTR
|Description=An HTML fragment.
|Optional=No
}}{{Method Parameter
|Name=pbstrStaticHTML
|Data type=BSTR
|Description=An HTML fragment consisting of static elements only.
|Optional=No
}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

String

An HTML fragment consisting of static elements only.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following script demonstrates how '''toStaticHTML''' sanitizes script and dynamic HTML attributes. The result of the operation is: <code>&lt;span&gt;Click Me&lt;/span&gt;</code>.
|Code=&lt;script type{{=}}"text/javascript"&gt;
function sanitize() 
{
    var szInput {{=}} myDiv.innerHTML;
    var szStaticHTML {{=}} toStaticHTML(szInput);
    ResultComment {{=}} "\ntoStaticHTML sanitized the HTML fragment as follows:\n"
        + "Original Content:\n" + szInput + "\n"
        + "Static Content:\n" + szStaticHTML + "\n";
    myDiv.innerText {{=}} ResultComment;
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"sanitize()"&gt;
    &lt;div id{{=}}"myDiv"&gt;
    &lt;script&gt;function test() { alert("Testing, Testing, 123..."); }&lt;/script&gt;
    &lt;span onclick{{=}}"test()"&gt;Click Me&lt;/span&gt;
    &lt;/div&gt;
&lt;/body&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''toStaticHTML''' method can be used to remove event attributes and script from user input before it is displayed as HTML. Malicious HTML can be passed on a URL, in form parameters, or across domains by '''XDomainRequest''' or [[dom/Window/postMessage|'''postMessage''']]. Always validate user input before adding it as an HTML fragment to a webpage or storing it in a database.
'''Note'''   This method does not filter the attributes of the '''base''' element. This can cause potentially unwanted redirect requests for '''link''' and [[html/elements/a|'''anchor''']] elements injected into a webpage. For best results, only use '''toStaticHTML''' to modify elements in the body of a webpage.
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>window</code>
*<code>[[dom/HTMLElement/innerHTML|innerHTML]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}