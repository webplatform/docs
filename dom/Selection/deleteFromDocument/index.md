{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Deletes the selected nodes from a document.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Selection
|Example_object_name=selObj
|Return_value_name=result
|Javascript_data_type=Number
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=In the following example, select the text and elements in the shaded section. When the mouse button is released, the selected items are deleted. Refresh the page to try again.
|Code=&lt;!DOCTYPE html&gt;
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
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
window.getSelection().deleteFromDocument();
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 7.6.1
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Selection.deleteFromDocument Selection.deleteFromDocument]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975176(v=vs.85).aspx deleteFromDocument Method]
|HTML5Rocks_link=
}}