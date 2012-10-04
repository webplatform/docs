{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/selection
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
|Description=In the following example, select the text and elements in the shaded section. When the mouse button is released, the selected items are deleted. Refresh the page to try again.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt;
    &lt;html&gt;
    &lt;head&gt;
    &lt;title&gt;Delete From Document&lt;/title&gt;        
        &lt;script type{{=}}"text/javascript"&gt;
        function deleteSelectedContent() {
        if (window.getSelection){                       //check for a selection
            var selection {{=}} window.getSelection();      //get a selection object
            selection.deleteFromDocument();             //remove content            
            }     
        }
        function refresh()                 
        {
          window.location.reload( false );              //reload our page
        }        
    &lt;/script&gt;
    &lt;/head&gt;
    &lt;body&gt;
    &lt;div onmouseup{{=}}"deleteSelectedContent ()" style{{=}}"background-color:#c0c0c0;"  &gt;
&lt;h1&gt;Now you see it&lt;/h1&gt;
&lt;p&gt;Select some text or elements on this page. When you release the mouse button, it will be gone. &lt;/p&gt;
&lt;h2&gt;H2 header&lt;/h2&gt;
&lt;p&gt;Some more sample text to &lt;strong&gt;delete&lt;/strong&gt;.&lt;/p&gt;
&lt;/div&gt;   
 &lt;input type{{=}}"button" value{{=}}"Refresh page" onclick{{=}}"refresh()"   /&gt;   
    &lt;/body&gt;
&lt;/html&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 7.6.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/HTMLSelection|HTMLSelection]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}