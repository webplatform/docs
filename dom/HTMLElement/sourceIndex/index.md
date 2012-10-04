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
|Description=This example uses the '''sourceIndex''' property to identify the previous and next elements in the [[dom/properties/all|'''all''']] collection.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/sourceIndex.htm
|Code=
&lt;SCRIPT&gt;
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
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>abbr</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>address</code>
*<code>applet</code>
*<code>area</code>
*<code>article</code>
*<code>aside</code>
*<code>b</code>
*<code>bdo</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
*<code>br</code>
*<code>button</code>
*<code>caption</code>
*<code>center</code>
*<code>cite</code>
*<code>code</code>
*<code>col</code>
*<code>colGroup</code>
*<code>custom</code>
*<code>dd</code>
*<code>del</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>dt</code>
*<code>em</code>
*<code>embed</code>
*<code>fieldSet</code>
*<code>figcaption</code>
*<code>figure</code>
*<code>font</code>
*<code>footer</code>
*<code>form</code>
*<code>frame</code>
*<code>frameSet</code>
*<code>head</code>
*<code>header</code>
*<code>hgroup</code>
*<code>hn</code>
*<code>hr</code>
*<code>html</code>
*<code>i</code>
*<code>iframe</code>
*<code>img</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}hidden</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}text</code>
*<code>ins</code>
*<code>isIndex</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>listing</code>
*<code>map</code>
*<code>mark</code>
*<code>marquee</code>
*<code>menu</code>
*<code>nav</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>noBR</code>
*<code>object</code>
*<code>ol</code>
*<code>optGroup</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>q</code>
*<code>rt</code>
*<code>ruby</code>
*<code>s</code>
*<code>samp</code>
*<code>section</code>
*<code>select</code>
*<code>small</code>
*<code>span</code>
*<code>strike</code>
*<code>strong</code>
*<code>sub</code>
*<code>sup</code>
*<code>[[html/elements/table|table]]</code>
*<code>tBody</code>
*<code>td</code>
*<code>textArea</code>
*<code>tFoot</code>
*<code>th</code>
*<code>tHead</code>
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>xmp</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}