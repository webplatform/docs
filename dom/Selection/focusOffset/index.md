{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/selection
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example uses '''focusOffset''' to show the offset value for the end of a selection when you release the mouse button.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
&lt;!-- this example displays the character offset from anchor node of your selection--&gt;
    &lt;title&gt;Focus Offset Example&lt;/title&gt;        
    &lt;script type{{=}}"text/javascript"&gt;         
      function getfocusOffset() {
        if (window.getSelection) {                      //only works if supported
           var selection {{=}} window.getSelection ();      //get the selection object     
           var focusOffsetProp {{=}} selection.focusOffset;   //get the offset
           alert ( "Offset: \n" + focusOffsetProp.toString());                                 
           }
      }                
    &lt;/script&gt;
  &lt;/head&gt;
&lt;body&gt;
&lt;div onmouseup{{=}}"getfocusOffset()"&gt;    &lt;!-- call the function when the mouse button is released --&gt;
      &lt;p&gt;
        Use the mouse to select some text within this field.
        When &lt;strong&gt;the left &lt;em&gt;button&lt;/em&gt; is released&lt;/strong&gt;, a dialog box appears with the anchor offset.
      &lt;/p&gt;  
      &lt;p&gt;
        The nested tags &lt;strong&gt;here and &lt;em&gt;there&lt;/em&gt; can&lt;/strong&gt; demonstrate different offsets as well.
      &lt;/p&gt;
    &lt;/div&gt;
  &lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''focusOffset''' typically refers to a character position within the text portion of the [[dom/properties/focusNode|'''focusNode''']].
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 7.6.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/HTMLSelection|HTMLSelection]]</code>
*<code>Reference</code>
*<code>[[dom/properties/focusNode|focusNode]]</code>
*<code>[[dom/properties/anchorNode|anchorNode]]</code>
*<code>[[dom/properties/anchorOffset|anchorOffset]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}