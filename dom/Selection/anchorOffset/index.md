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
|Description=The following example shows the anchorOffset value of a selection when you release the mouse button.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
&lt;!-- this example shows the character offset from anchor node of your selection--&gt;
    &lt;title&gt;AnchorOffset Example&lt;/title&gt;        
    &lt;script type{{=}}"text/javascript"&gt;         
      function getAnchorOffset() {
        if (window.getSelection) {                      //only work if supported
           var selection {{=}} window.getSelection ();      //get the selection object     
           var anchorOffsetProp {{=}} selection.anchorOffset;   //get the offset
           alert ( "Anchor Offset: \n" + anchorOffsetProp.toString());                                 
           }
      }                
    &lt;/script&gt;
  &lt;/head&gt;
&lt;body&gt;
&lt;div onmouseup{{=}}"getAnchorOffset()"&gt;    &lt;!-- call this function when the mouse button is released --&gt;
      &lt;p&gt;
        Select some text with your mouse within this field.
        When &lt;strong&gt;the left &lt;em&gt;button&lt;/em&gt; is released&lt;/strong&gt;, a dialog pops up with the anchor offset.
      &lt;/p&gt;  
      &lt;p&gt;
        The nested tags &lt;strong&gt;here and &lt;em&gt;there&lt;/em&gt; can&lt;/strong&gt; demonstrate different offsets as well.
      &lt;/p&gt;
    &lt;/div&gt;
  &lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The value that is returned by '''anchorOffset''' usually refers to a character position within the text portion of the element.
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