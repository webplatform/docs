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
|Name=parentNode
|Data type=any
|Optional=No
}}
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
|Description=In this example, your selection is replaced by all the elements of the DIV.
|Code=&lt;!DOCTYPE html&gt;
&lt;head&gt;
    &lt;title&gt;Select all children example&lt;/title&gt;
    &lt;script&gt;
        function selectAllChildrenDemo () {
            var getNode {{=}} document.getElementById ("elementID");
            if (window.getSelection) {        // Internet Explorer 9
                var selection {{=}} window.getSelection ();
                selection.selectAllChildren (getNode);
            } else {                          // Workaround for Internet Explorer 8 &amp; earlier
                var oRange {{=}} document.body.createTextRange ();
                oRange.moveToElementText (getNode);
                oRange.select ();
            }
        }
    &lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;button onclick{{=}}"selectAllChildrenDemo ();"&gt;Select everything below&lt;/button&gt;
    &lt;div id{{=}}"elementID"&gt;The &lt;strong&gt;selectAllChildren&lt;/strong&gt; method replaces the current &lt;em&gt;selection&lt;/em&gt; with the all the &lt;strong&gt;contents&lt;/strong&gt; of the specified element (in this case a DIV).&lt;/div&gt;
&lt;/body&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
Raises a WRONG_DOCUMENT_ERR [[dom/DOMException|'''DOMException''']] if the ''parentNode'' is in another document.
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