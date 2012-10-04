{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLInputElement
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following code  example shows how to set a text selection's start and end positions.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;Selection Start and End example&lt;/title&gt;
    &lt;script&gt;
        function SelectSomeText () {
            var input {{=}} document.getElementById ("Textbox");
                input.selectionStart {{=}} 4;
                input.selectionEnd {{=}} 13;                
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
*<code>[[dom/HTMLInputElement|HTMLInputElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}