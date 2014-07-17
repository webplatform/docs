{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/Selection
|Read_only=No
|Example_object_name=selObj
|Return_value_name=result
|Javascript_data_type=Boolean
|Return_value_description=
false - The selection is not collapsed.

true - The selection is collapsed or empty.

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses '''isCollapsed''' to see whether a selection is empty or not. If the selection is not empty, the selected text is displayed.
|Code=&lt;!DOCTYPE html&gt;

&lt;html&gt;
  &lt;head&gt;
     
     
    &lt;!-- This example shows the character offset from anchor node of your selection. --&gt;
    &lt;title&gt;isCollapsed Example&lt;/title&gt;        
    &lt;script type{{=}}"text/javascript"&gt;         
      function testCollapsed () {
        if (window.getSelection) {      
          var oSel {{=}} window.getSelection();
          var oDisplayBox {{=}} document.getElementById('displayBox');
          
          if (oSel.isCollapsed) {
            oDisplayBox.innerHTML {{=}} "&lt;p&gt;Nothing is selected!&lt;/p&gt;";
          }
          else {
            oDisplayBox.innerHTML {{=}} "&lt;p&gt;The text of the selection:\n" + oSel.toString() + "&lt;/p&gt;";
          }
        }            
      }        
    &lt;/script&gt;
  &lt;/head&gt;

  &lt;body&gt;
    &lt;p&gt;
      Click the button below to get the text content. 
      Use the mouse to select some text within this field. 
      Then, click the button again to see if the selection is collapsed.
    &lt;/p&gt;  
    &lt;input type{{=}}"button" value{{=}}"Is it collapsed" onclick{{=}}"testCollapsed()" /&gt;   
    &lt;div id{{=}}"displayBox"&gt;&lt;/div&gt;
  &lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
A collapsed selection has its start and end points set to the same value, which renders it empty.
Even a collapsed selection may have a rangeCount greater than 0. selObj.getRangeAt(0) may return a range that is also collapsed.
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Selection.isCollapsed Selection.isCollapsed]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974692(v=vs.85).aspx isCollapsed Property]
|HTML5Rocks_link=
}}