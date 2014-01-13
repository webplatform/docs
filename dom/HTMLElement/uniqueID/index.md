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
|Description=The following examples use the '''uniqueID''' property within an HTC to assign a unique identifier to an element.

This example assigns a '''uniqueID''' to an element from within a behavior. Every time the [[dom/methods/setTimeout|'''setTimeout''']] method is invoked, the behavior-defined tick() function is called. The '''uniqueID''' attaches the element to the tick() function defined in the behavior's namespace.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/CustomTags/CustomFlying.htm
|Code=
&lt;PUBLIC:METHOD NAME{{=}}"tick" /&gt;
&lt;PUBLIC:METHOD NAME{{=}}"startFly" /&gt;
&lt;PUBLIC:PROPERTY NAME{{=}}"from" /&gt;
&lt;PUBLIC:PROPERTY NAME{{=}}"fromX" /&gt;
&lt;PUBLIC:PROPERTY NAME{{=}}"fromY" /&gt;
&lt;PUBLIC:PROPERTY NAME{{=}}"delay" /&gt;
:
&lt;SCRIPT LANGUAGE{{=}}"jscript"&gt;
var currCount;
var flyCount;
var flying;
var msecs;
var oTop, oLeft;

msecs {{=}} 50;
flyCount {{=}} 20;
flying {{=}} false;

runtimeStyle.position {{=}} "relative";
runtimeStyle.visibility {{=}} "hidden";

window.attachEvent("onload", onload);

function onload()
{
  // delay commences from the window.onLoad event
  if (delay !{{=}} "none")
  {
     window.setTimeout(uniqueID+".tick()", delay);
  }
}

function tick()
{
   if (flying {{=}}{{=}} false)
   {
      startFly();
   }
   else
   {
      doFly();
   }
}
:
&lt;/SCRIPT&gt;
}}
{{Single_Example
|Description=This example uses the '''uniqueID''' property to show how the browser can autogenerate a unique ID for an element inserted into the document by a behavior.
|LiveURL=
|Code=
&lt;PUBLIC:ATTACH EVENT{{=}}"onload" FOR{{=}}"window" ONEVENT{{=}}"init()" /&gt;
&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;

function init()
{
   // Specifying an ID{{=}}document.uniqueID ensures that a unique identifier
   // will be assigned to the element being inserted into the document by
   // the behavior.
   newTextAreaID {{=}} element.document.uniqueID;
   element.document.body.insertAdjacentHTML ("beforeEnd",
    "&lt;P&gt;&lt;TEXTAREA STYLE{{=}}'height: 200 ;"+
    "width: 350' ID{{=}} " + newTextAreaID + "&gt;&lt;/TEXTAREA&gt;&lt;/P&gt;");
}
&lt;/SCRIPT&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
When you apply this property to the [[dom/Document|'''Document''']] object, the client automatically generates a new ID that you can assign to an element's [[html/attributes/id|'''id''']] property.
A new ID is generated and assigned to the element the first time the property is retrieved. Every subsequent access to the property on the same element returns the same ID.
'''Note'''  The unique ID generated is not guaranteed to be the same every time the document is loaded.
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
*<code>b</code>
*<code>base</code>
*<code>baseFont</code>
*<code>bgSound</code>
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
*<code>comment</code>
*<code>dd</code>
*<code>del</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>[[dom/Document|Document]]</code>
*<code>dt</code>
*<code>em</code>
*<code>embed</code>
*<code>fieldSet</code>
*<code>font</code>
*<code>form</code>
*<code>frame</code>
*<code>frameSet</code>
*<code>head</code>
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
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>link</code>
*<code>listing</code>
*<code>map</code>
*<code>marquee</code>
*<code>menu</code>
*<code>noBR</code>
*<code>object</code>
*<code>ol</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>q</code>
*<code>s</code>
*<code>samp</code>
*<code>script</code>
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
*<code>title</code>
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>xmp</code>
*<code>Conceptual</code>
*<code>Introduction to DHTML Behaviors</code>
*<code>Using HTML Components to Implement DHTML Behaviors in Script</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}