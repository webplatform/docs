{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=start|Data type=Integer|Description=The offset into the text field for the start of the selection.|Optional=}}
{{Method Parameter|Name=end|Data type=Integer|Description=The offset into the text field for the end  of the selection.|Optional=}}
|Method_applies_to=dom/HTMLInputElement
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
|Description=The following code  example shows how to set  a test  selection's start and end positions.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}9" /&gt; &lt;!--Force IE9 mode --&gt;
&lt;title&gt;Example of setSelectionRange()&lt;/title&gt;
    &lt;script&gt;
        function SelectSomeText () {
            var input {{=}} document.getElementById ("Textbox");
                input.setSelectionRange (4,13);          
        }
    &lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;p&gt;&lt;input type{{=}}"text" id{{=}}"Textbox" size{{=}}"40" value{{=}}"The text selection appears here"/&gt;&lt;/p&gt;
    &lt;p&gt;&lt;button onclick{{=}}"SelectSomeText ()"&gt;See selection&lt;/button&gt;&lt;/p&gt;
    
&lt;/body&gt;
&lt;/html&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
If you set a parameter  to  more  than the length of the text field, the parameter points  to  the end of the text field. If the ''end'' parameter is less than or equal to the ''start'' paramenter, the start and end positions of the selection are set to the ''end'' value. The selection is then an insertion point or caret.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 7.6.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>input type{{=}}text</code>
*<code>textArea</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}