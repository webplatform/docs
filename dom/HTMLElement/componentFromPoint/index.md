---
title: componentFromPoint
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, examples best practices, compatibility, standards, clean-up of MSDN sections'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/componentFromPointEX1.htm'
uri: dom/HTMLElement/componentFromPoint

---
# componentFromPoint

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/HTMLElement](/dom/HTMLElement)*

## Syntax

``` {.js}
var object = object.componentFromPoint(x, y);
```

## Parameters

### x

 Data-typeÂ
:   any

 Â Specifies the client window coordinate of x.

### y

 Data-typeÂ
:   any

 Â Specifies the client window coordinate of y.

## Return Value

Returns an object of type DOM Node.

String

String

{

## Examples

This example uses the **componentFromPoint** method to determine which object the mouse pointer is hovering over.

    <HTML>
    <HEAD>
    <SCRIPT>
    /*When this function is activated, an alert pops up displays the component at the position of the pointer. */
    function ComponentSnapShot(){
       var sElem = "";
       sElem = document.body.componentFromPoint(
          event.clientX,
          event.clientY
       );
       if (sElem=="")
        alert("No component there!");
       else
        alert("Component: " + sElem);
    }
    function trackElement(){
       var sElem = "";
       sElem = document.body.componentFromPoint(
          event.clientX,
          event.clientY
       );
       window.status = "mousemove " + event.clientX + ", "
          + event.clientY +
          " The mouse pointer is hovering over: " + sElem;

    }
    </SCRIPT>
    </HEAD>
    <!-- There are several different events that can be used with componentFromPoint. Below are a few of them.
    Be carefull! Not all mouse events can be used with componentFromPoint.  -->
    <BODY onmousemove="trackElement()" onmousedown="ComponentSnapShot()" onkeydown="ComponentSnapShot()" oncontextmenu="ComponentSnapShot()">
    <TEXTAREA COLS=500 ROWS=500>
    This text forces scroll bars to appear in the window.
    </TEXTAREA>
    </BODY>
    </HTML>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/componentFromPointEX1.htm)

## Notes

### Remarks

The **componentFromPoint** method, available as of Microsoft Internet ExplorerÂ 5, is applicable to any object that can be given scroll bars through Cascading Style Sheets (CSS). The **componentFromPoint** method might not return the same object consistently when it is used with the [**onmouseover**](/dom/MouseEvent/mouseover) event. Because a user's mouse speed and entry point can vary, different components of an element can fire the **onmouseover** event. For example, when a user moves the cursor over a **textArea** object with scroll bars, the event might fire when the mouse enters the component border, the scroll bars, or the client region. After the event fires, the expected element might not be returned, unless the scroll bars were the point of entry for the mouse. In this case, the [**onmousemove**](/dom/MouseEvent/mousemove) event can be used to provide more consistent results. For the object's sizing handles to appear, [**designMode**](/dom/Document/designMode) must be **On**, and the object must be selected.

### Syntax

### Standards information

There are no standards that apply here.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

