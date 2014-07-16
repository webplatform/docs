{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns the element or node that contains the start of the selection.}}
{{API_Object_Property
|Property_applies_to=dom/Selection
|Read_only=No
|Example_object_name=selObj
|Return_value_name=node
|Javascript_data_type=DOM Node
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example shows the text that you select, and all the text contained in the anchorNode element.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
&lt;!-- this example shows the text you selected, and all the text within the anchor node--&gt;
    &lt;title&gt;AnchorNode Example&lt;/title&gt;        
    &lt;script type{{=}}"text/javascript"&gt;         
      function getAnchorNode() {
        if (window.getSelection) {                      //only work if supported
           var selection {{=}} window.getSelection ();      //get the selection object     
           var anchorNodeProp {{=}} selection.anchorNode;   //get the node object        
           alert ( "Selected text: \n" + selection.toString() + "\nText related to the node: \n" + anchorNodeProp.toString());                                 
           }
      }                
    &lt;/script&gt;
  &lt;/head&gt;
&lt;body&gt;
&lt;div onmouseup{{=}}"getAnchorNode()"&gt;                       &lt;!-- call this function when the mouse button is released --&gt;
      &lt;p&gt;
        Select some text with your mouse within this field.
        When the left button is released, a dialog pops up with the anchor node.
      &lt;/p&gt;  
      &lt;p&gt;
        This is some more text to try as well.
      &lt;/p&gt;
    &lt;/div&gt;
  &lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
Returns null if not successful. This is not supported by Windows Internet Explorer 8 or earlier versions. AnchorNode returns the value of the [[dom/Range/startContainer|'''startContainer''']] attribute of the first '''Range ''' object in the list. See [[dom/Selection/focusNode|'''focusNode''']] to find the node that contains the end of a selection.

A user may make a selection from left to right (in document order) or right to left (reverse of document order). The anchor is where the user began the selection. This can be visualized by holding the Shift key and pressing the arrow keys on your keyboard. The selection's anchor does not move, but the selection's focus, the other end of the selection, does move.
|Import_Notes====Syntax===
startNode=selObj.anchorNode;
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Selection.anchorNode Selection.anchorNode]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974688(v=vs.85).aspx anchorNode Property]
|HTML5Rocks_link=
}}