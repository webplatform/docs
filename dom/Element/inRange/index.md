---
title: inRange
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs summary, specs, and compat'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/inrange.htm'
uri: dom/Element/inRange

---
# inRange

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/Element](/dom/Element)*

## Syntax

``` {.js}
var object = object.inRange(/* see parameter list */);
```

## Parameters

### Range

 Data-typeÂ
:   any

[**TextRange**](/dom/TextRange) object that might be contained.

## Return Value

Returns an object of type DOM Node.

Boolean

**Boolean** that returns one of the following possible values.

Return value
:   Description
true
:   Range is contained within or is equal to the TextRange object on which the method is called.
false
:   Range is not contained within the TextRange object on which the method is called.

Â

## Examples

The following example shows how to use the **inRange** method to show that two [**TextRange**](/dom/TextRange) objects are equal.

    <html>
    <script type="text/javascript">
    window.onload=fnCheck;
    function fnCheck(){
        var oRng1 = document.body.createTextRange();
        var oRng2 = oRng1.duplicate();
        var bInside = oRng1.inRange(oRng2); // returns true;
    }
    </script>

    <body>
        <div id=div1>
        Content for division 1.
        </div>
        <div id=div2>
        Content for division 2.
        </div>
    </body>
    </html>

The following example shows how to use the **inRange** method to show that two contained ranges are not equal.

    <html>
    <script type="text/javascript">
    window.onload=fnCheck;
    function fnCheck(){
         var oRng1 = document.body.createTextRange(); // create a text range
           var oRng2 = oRng1.duplicate();       // create a duplicate range base on oRng1

        oRng1.moveToElementText(document.getElementById("div1"));
        oRng2.moveToElementText(document.getElementById("div2"));
        var bInside = oRng1.inRange(oRng2); // returns false;
    }
    </script>

    <body>
        <div id="div1">
        Content for division 1.
        </div>
        <div ID="div2">
        Content for division 2.
        </div>
    </body>
    </html>

The following example shows how to use the **inRange** method to show that a text range exists within another text range.

    <html>
    <script type="text/javascript">
    window.onload=fnCheck;
    function fnCheck(){
        var oRng1 = document.body.createTextRange();
        var oRng3 = oRng1.duplicate();
        oRng3.findText('division 1');
        var bInside = oRng1.inRange(oRng3); // returns true;
    }
    </script>
    <body>
        <div id="div1">
        Content for division 1.
        </div>
        <div ID="div2">
        Content for division 2.
        </div>
    </body>
    </html>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/inrange.htm)

## Notes

### Remarks

This feature might not be available on platforms other than Microsoft Win32.

### Syntax

### Standards information

There are no standards that apply here.

## See also

### Related pages (MSDN)

-   `TextRange`
-   `isEqual`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

