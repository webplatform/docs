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
|Description=The following examples use the '''uniqueID''' property within an HTC to assign a unique identifier to an element.

This example assigns a '''uniqueID''' to an element from within a behavior. Every time the [[dom/Window/setTimeout|'''setTimeout''']] method is invoked, the behavior-defined tick() function is called. The '''uniqueID''' attaches the element to the tick() function defined in the behavior's namespace.
|Code=&lt;PUBLIC:METHOD NAME{{=}}"tick" /&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/CustomTags/CustomFlying.htm
}}{{Single Example
|Description=This example uses the '''uniqueID''' property to show how the browser can autogenerate a unique ID for an element inserted into the document by a behavior.
|Code=&lt;PUBLIC:ATTACH EVENT{{=}}"onload" FOR{{=}}"window" ONEVENT{{=}}"init()" /&gt;
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
}}
}}
{{Notes_Section
|Notes====Remarks===
When you apply this property to the [[dom/Document|'''Document''']] object, the client automatically generates a new ID that you can assign to an element's [[html/attributes/id|'''id''']] property.
A new ID is generated and assigned to the element the first time the property is retrieved. Every subsequent access to the property on the same element returns the same ID.
'''Note'''  The unique ID generated is not guaranteed to be the same every time the document is loaded.
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