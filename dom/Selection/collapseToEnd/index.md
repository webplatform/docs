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
|Parameters=
|Method_applies_to=dom/Selection
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}