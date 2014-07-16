{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Collapses or sets the insertion point or caret at the end of a selection object.

If the content the selection is in is focused and editable, the caret will blink there.
}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Selection
|Example_object_name=selObj
|Javascript_data_type=Number
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following code example puts the caret or insertion point at the end of the selected text.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
   &lt;title&gt;Collapse to Start Example&lt;/title&gt;
    &lt;script&gt;
        function SelectAtEnd () {
            if (window.getSelection) {       
                var selection {{=}} window.getSelection ();
                selection.collapseToEnd ();
            }
        }
    &lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;p&gt;
    &lt;div contenteditable{{=}}"true" style{{=}}"width:300px;"&gt;
        Select some text from this paragraph, and then click the following button.
        When you click the button, the caret, or insertion point, is set to the end of your selection.
    &lt;/div&gt;
 &lt;/p&gt;  
 &lt;p&gt;&lt;input type{{=}}"button" name{{=}}"test" value{{=}}"Set caret" onclick{{=}}"SelectAtEnd ()" /&gt; &lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
Raises an INVALID_STATE [[dom/DOMException|'''DOMException''']] if there are no Ranges in the selection.
|Import_Notes====Syntax===
selObj.collapseToEnd()
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Selection.collapseToEnd Selection.collapseToEnd]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975174(v=vs.85).aspx collapseToEnd Method]
|HTML5Rocks_link=
}}