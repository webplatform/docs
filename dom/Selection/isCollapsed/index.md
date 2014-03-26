{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/Selection
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses '''isCollapsed''' to see whether a selection is empty or not. If the selection is not empty, the selected text is displayed.
|Code=&lt;!DOCTYPE html&gt;

&lt;html&gt;
  &lt;head&gt;
    &lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}9" /&gt;  &lt;!-- Only works in Internet Explorer 9 --&gt;     
     
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