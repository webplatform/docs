{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Adds all the children of the specified node to the selection. Previous selection is lost.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=parentNode
|Data type=DOM Node
|Description=The object that receives the new selection. 
|Optional=No
}}
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
}}{{Single Example
|Language=JavaScript
|Code=var footer {{=}} document.getElementById("footer");
window.getSelection().selectAllChildren(footer);
/* Everything inside the footer is now selected */
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Selection.selectAllChildren Selection.selectAllChildren]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975180(v=vs.85).aspx selectAllChildren Method]
|HTML5Rocks_link=
}}