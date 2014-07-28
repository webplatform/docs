{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary, examples best practices, compatibility, standards, clean-up of MSDN sections
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example demonstrates how to use the [[dom/Selection/createRange|'''createRange''']] method to retrieve the '''controlRange''' collection.
|Code=...
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/collections/controlrange.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Instead of using the collection's [[dom/HTMLCollection/item|'''item''']] method, you can use an index to directly access an element in the collection. For example, the element returned from the collection represented by <code>oColl(0)</code> is the same as the element returned by <code>oColl.item(0)</code>.
The '''controlRange''' collection is available as of Microsoft Internet Explorer 5.
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.
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