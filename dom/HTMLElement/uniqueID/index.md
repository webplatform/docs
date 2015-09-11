---
title: uniqueID
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/CustomTags/CustomFlying.htm'
notes:
  - 'summary, clean-up MSDN import'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLElement/uniqueID

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var result = element.uniqueID;
element.uniqueID = value;
```

## <span>Examples</span>

The following examples use the **uniqueID** property within an HTC to assign a unique identifier to an element.

This example assigns a **uniqueID** to an element from within a behavior. Every time the [**setTimeout**](/dom/Window/setTimeout) method is invoked, the behavior-defined tick() function is called. The **uniqueID** attaches the element to the tick() function defined in the behavior's namespace.

``` html
<PUBLIC:METHOD NAME="tick" />
<PUBLIC:METHOD NAME="startFly" />
<PUBLIC:PROPERTY NAME="from" />
<PUBLIC:PROPERTY NAME="fromX" />
<PUBLIC:PROPERTY NAME="fromY" />
<PUBLIC:PROPERTY NAME="delay" />
:
<SCRIPT LANGUAGE="jscript">
var currCount;
var flyCount;
var flying;
var msecs;
var oTop, oLeft;

msecs = 50;
flyCount = 20;
flying = false;

runtimeStyle.position = "relative";
runtimeStyle.visibility = "hidden";

window.attachEvent("onload", onload);

function onload()
{
  // delay commences from the window.onLoad event
  if (delay != "none")
  {
     window.setTimeout(uniqueID+".tick()", delay);
  }
}

function tick()
{
   if (flying == false)
   {
      startFly();
   }
   else
   {
      doFly();
   }
}
:
</SCRIPT>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/CustomTags/CustomFlying.htm)

This example uses the **uniqueID** property to show how the browser can autogenerate a unique ID for an element inserted into the document by a behavior.

``` html
<PUBLIC:ATTACH EVENT="onload" FOR="window" ONEVENT="init()" />
<SCRIPT LANGUAGE="JScript">

function init()
{
   // Specifying an ID=document.uniqueID ensures that a unique identifier
   // will be assigned to the element being inserted into the document by
   // the behavior.
   newTextAreaID = element.document.uniqueID;
   element.document.body.insertAdjacentHTML ("beforeEnd",
    "<P><TEXTAREA STYLE='height: 200 ;"+
    "width: 350' ID= " + newTextAreaID + "></TEXTAREA></P>");
}
</SCRIPT>
```

## <span>Notes</span>

### <span>Remarks</span>

When you apply this property to the [**Document**](/dom/Document) object, the client automatically generates a new ID that you can assign to an element's [**id**](/html/attributes/id) property. A new ID is generated and assigned to the element the first time the property is retrieved. Every subsequent access to the property on the same element returns the same ID. **Note**  The unique ID generated is not guaranteed to be the same every time the document is loaded.

### <span>Syntax</span>