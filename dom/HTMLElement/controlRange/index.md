{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example demonstrates how to use the [[dom/traversal/methods/createRange (selection)|'''createRange''']] method to retrieve the '''controlRange''' collection.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/collections/controlrange.htm
|Code=
...
function fnChangeFontFamily    (){
  if (document.selection.type {{=}}{{=}} "Control"){ 
    var oControlRange {{=}} document.selection.createRange();
    for (i {{=}} 0; i &lt; oControlRange.length; i++)
      if (oControlRange(i).tagName !{{=}} "IMG")
       oControlRange(i).style.fontFamily{{=}}event.srcElement.style.fontFamily;
  }
}
...
&lt;!-- Text Font-Family Controls  --&gt;
&lt;SPAN  onclick{{=}}"fnChangeFontFamily();"&gt;
    &lt;DIV STYLE{{=}}"height: 25px; cursor:hand; font-family:times; 
        font-size:14pt; font-weight:normal; color:white"&gt;Times&lt;/DIV&gt;
    &lt;DIV STYLE{{=}}"height: 25px; cursor:hand; font-family:arial;   
        font-size:14pt; font-weight:normal; color:white"&gt;Arial&lt;/DIV&gt;
    &lt;DIV STYLE{{=}}"height: 25px; cursor:hand; font-family:georgia; 
        font-size:14pt; font-weight:normal; color:white"&gt;Georgia&lt;/DIV&gt;
    &lt;DIV STYLE{{=}}"height: 25px; cursor:hand; font-family:verdana; 
        font-size:14pt; font-weight:normal; color:white"&gt;Verdana&lt;/DIV&gt;
&lt;/SPAN&gt;&lt;BR/&gt;
...
}}}}
{{Notes_Section
|Notes=
===Remarks===
Instead of using the collection's [[dom/traversal/methods/item (controlRange)|'''item''']] method, you can use an index to directly access an element in the collection. For example, the element returned from the collection represented by <code>oColl(0)</code> is the same as the element returned by <code>oColl.item(0)</code>.
The '''controlRange''' collection is available as of Microsoft Internet Explorer 5.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Reference</code>
*<code>[[dom/traversal/methods/createControlRange|createControlRange]]</code>
*<code>[[dom/traversal/methods/createRange (selection)|createRange]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}