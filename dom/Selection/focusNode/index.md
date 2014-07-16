{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Retrieves the element or node that contains the end of a selection.}}
{{API_Object_Property
|Property_applies_to=dom/Selection
|Read_only=Yes
|Example_object_name=selObj
|Return_value_name=oNode
|Javascript_data_type=DOM Node
|Return_value_description=Returns the node in which the selection ends.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example shows the text content that is contained within the node (or tags) that is in focus when you click a section of text.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
&lt;!-- this example displays the character offset from anchor node of your selection--&gt;
    &lt;title&gt;focusNode Example&lt;/title&gt;        
    &lt;script type{{=}}"text/javascript"&gt;         
      function getfocusNode() {
        if (window.getSelection) {                      //only work if supported
           var selection {{=}} window.getSelection ();      //get the selection object     
           var focusNodeProp {{=}} selection.focusNode;     //get the node containing the end of selection 
           alert ( "Text of current node: \n" + focusNodeProp.toString() + "\nTag name: &lt;" + focusNodeProp.parentNode.tagName +"&gt;");                                                                                 
           }
      }                
    &lt;/script&gt;
  &lt;/head&gt;
&lt;body&gt;
&lt;div onmouseup{{=}}"getfocusNode()"&gt;    &lt;!-- call the function when the mouse button is released --&gt;
      &lt;p&gt;
        Select some text with your mouse within this field.
        When &lt;strong&gt;the left &lt;em&gt;button&lt;/em&gt; is released&lt;/strong&gt;, a dialog box appears with the focusNode.
      &lt;/p&gt;  
      &lt;p&gt;
        The nested tags &lt;strong&gt;here and &lt;em&gt;there&lt;/em&gt; can&lt;/strong&gt; demonstrate different focusNodes as well.
      &lt;/p&gt;
    &lt;/div&gt;
  &lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
Returns null if the selection does not exist. As a [[dom/Selection|'''Selection''']] object consists of a list of Range objects, focusNode returns the value of the [[dom/Range/endContainer|'''endContainer''']] attribute of the last Range object in the list.
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Selection.focusNode Selection.focusNode]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974690(v=vs.85).aspx focusNode Property]
|HTML5Rocks_link=
}}