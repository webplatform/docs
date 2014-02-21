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
|Property_applies_to=dom/HTMLElement
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''sourceIndex''' property to identify the previous and next elements in the '''all''' collection (deprecated).
|Code=&lt;SCRIPT&gt;
function fnHandler(){
   // Retrieve the element that fired the event.
   var oElement{{=}}event.srcElement;
   var iIndex{{=}}oElement.sourceIndex;
   var sTagName{{=}}oElement.tagName;
   if(sTagName{{=}}{{=}}"!"){
      sTagName{{=}}"COMMENT";
   }
   oVal1.innerText{{=}}iIndex;
   oVal2.innerText{{=}}sTagName;
   if(iIndex-1&gt;0){
      sTagName{{=}}document.all[iIndex-1].tagName;
      if(sTagName{{=}}{{=}}"!"){
         sTagName{{=}}"COMMENT";
      }   
      oVal3.innerText{{=}}sTagName;
   }
   else{
      oVal3.innerText{{=}}"Cannot read.";
   }
   if(iIndex+1&lt;document.all.length){
      sTagName{{=}}document.all[iIndex+1].tagName;
      if(sTagName{{=}}{{=}}"!"){
         sTagName{{=}}"COMMENT";
      }   
      oVal4.innerText{{=}}sTagName;
   }
   else{
      oVal4.innerText{{=}}"Cannot read.";
   }
}
&lt;/SCRIPT&gt;

&lt;BODY onmousemove{{=}}"fnHandler()"&gt;
&lt;TABLE&gt;
&lt;TR&gt;&lt;TD&gt;Source Index:&lt;/TD&gt;&lt;TD ID{{=}}oVal1&gt;&lt;/TD&gt;&lt;/TR&gt;
&lt;TR&gt;&lt;TD&gt;Object Name:&lt;/TD&gt;&lt;TD ID{{=}}oVal2&gt;&lt;/TD&gt;&lt;/TR&gt;
&lt;TR&gt;&lt;TD&gt;Previous Object:&lt;/TD&gt;&lt;TD ID{{=}}oVal3&gt;&lt;/TD&gt;&lt;/TR&gt;
&lt;TR&gt;&lt;TD&gt;Next Object:&lt;/TD&gt;&lt;TD ID{{=}}oVal4&gt;&lt;/TD&gt;&lt;/TR&gt;
&lt;/TABLE&gt;
&lt;/BODY&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/sourceIndex.htm
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
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