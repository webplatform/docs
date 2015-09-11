---
title: getContext
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - "\nMove Candidate:   Probably should be under HTML5 canvas element. See HTML5 specification.\n\n"
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLCanvasElement
    href: /dom/HTMLCanvasElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLCanvasElement
tags:
  - API
  - Object
  - Methods
  - DOM
uri: canvas/methods/getContext

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/HTMLCanvasElement](/dom/HTMLCanvasElement)[dom/HTMLCanvasElement](/dom/HTMLCanvasElement)

## <span>Syntax</span>

``` js
var object = object.getContext(/* see parameter list */);
```

## <span>Parameters</span>

### <span>contextId</span>

 Data-type
:   any

 The identifier (ID) of the type of canvas to create.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

**ICanvasRenderingContext2D**

The context object.

## <span>Examples</span>

The following code example uses **getContext** to get a context to use to show a filled rectangle and filled text.

``` html
<!DOCTYPE html>
<head>
  <script type="text/javascript">
function draw()
{
  var canvas = document.getElementById("MyCanvas");
  if (canvas.getContext)
    {
    var ctx = canvas.getContext("2d");
    ctx.font = "italic 36px/2 Unknown Font, sans-serif";
    ctx.fillStyle = "blue";
    ctx.fillRect(0,0,canvas.width,canvas.height);
    ctx.fillStyle = "white";
    ctx.fillText ("Hello World",canvas.width/2,canvas.height*.8);
    }
}
</script>
</head>
<body onload="draw()" bgcolor="lightgray" >
      <div>
        <canvas id="MyCanvas" width="500" height="500" > </canvas>
      </div>
  </body>
</html>
```

## <span>Notes</span>

### <span>Remarks</span>

The **getContext** method returns null if the *contextId* value is not supported.

### <span>Syntax</span>

### <span>Standards information</span>

-   [The canvas element](http://go.microsoft.com/fwlink/p/?linkid=197017), Section 4.8.11

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `canvas`
