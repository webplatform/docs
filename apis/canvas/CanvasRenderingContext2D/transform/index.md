---
title: 'transform'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://audiocommander.github.com/transformMatrixDemo'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: "Replaces the current transformation matrix with the result of multiplying the current transformation matrix with the matrix described by:\n"
tags:
  - API_Object_Methods
  - API
uri: apis/canvas/CanvasRenderingContext2D/transform

---
## Summary

Replaces the current transformation matrix with the result of multiplying the current transformation matrix with the matrix described by:

`a c e b d f 0 0 1`

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var object = object.transform(a, b, c, d, e, f);
```

## Parameters

### a

 Data-type
:   any

 The m1,1 value in the matrix.

### b

 Data-type
:   any

 The m1,2 value in the matrix.

### c

 Data-type
:   any

 The m2,1 value in the matrix.

### d

 Data-type
:   any

 The m2,2 value in the matrix.

### e

 Data-type
:   any

 The delta x (dx) value in the matrix.

### f

 Data-type
:   any

 The delta y (dy) value in the matrix.

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

This example shows visually how the transformation matrix works.

``` html
<html>
<head>
    <title>Transformation Matrix Demo</title>

<style>
#sliders {
    position: absolute;
    left: 0;
    top: 0;
}
#slA,#slB,#slC,#slD,#slE,#slF {
    display: block;
    position: relative;
    top: 1em;
    z-index: 100;
    margin-bottom: 2em;
}
</style>
</head>

<body>
<canvas id="canvas" width="800" height="600"></canvas>
<div id="sliders">
<div id="slA"><input type="range" id="sliderA" min="-100" max="100" value="100"></input>a:<span id="aValue">0</span></div>
<div id="slB"><input type="range" id="sliderB" min="-100" max="100" value="0">  </input>b:<span id="bValue">0</span></div>
<div id="slC"><input type="range" id="sliderC" min="-100" max="100" value="0">  </input>c:<span id="cValue">0</span></div>
<div id="slD"><input type="range" id="sliderD" min="-100" max="100" value="100"></input>d:<span id="dValue">0</span></div>
<div id="slE"><input type="range" id="sliderE" min="-100" max="100" value="0">  </input>e:<span id="eValue">0</span></div>
<div id="slF"><input type="range" id="sliderF" min="-100" max="100" value="0">  </input>f:<span id="fValue">0</span></div>
</div>

<script type="text/javascript">

var canvas = document.getElementById("canvas");
var ctx = canvas.getContext('2d');

// get the sliders
var sliderA = document.querySelector('#sliderA');
var sliderB = document.querySelector('#sliderB');
var sliderC = document.querySelector('#sliderC');
var sliderD = document.querySelector('#sliderD');
var sliderE = document.querySelector('#sliderE');
var sliderF = document.querySelector('#sliderF');

var a, b, c, d, e, f;

function mapSliderValue(v) {
    return v / 100;
}

function sliderDidChange() {
    // get values
    a = mapSliderValue(sliderA.value);
    b = mapSliderValue(sliderB.value);
    c = mapSliderValue(sliderC.value);
    d = mapSliderValue(sliderD.value);
    e = sliderE.value;
    f = sliderF.value;
    // show values
    document.querySelector('#aValue').innerText = a;
    document.querySelector('#bValue').innerText = b;
    document.querySelector('#cValue').innerText = c;
    document.querySelector('#dValue').innerText = d;
    document.querySelector('#eValue').innerText = e;
    document.querySelector('#fValue').innerText = f;
    // redraw
    draw();
}

function draw() {
    // save the current context
    ctx.save();
    // clear background
    ctx.fillStyle = "lightsteelblue";
    ctx.fillRect(0,0,canvas.width,canvas.height);
    // apply transform matrix
    ctx.setTransform(a, b, c, d, e, f);
    // draw transformed text
    ctx.fillStyle = "navy";
    ctx.fillText("Hello World!", 0, 0);
    // restore the context
    ctx.restore();
}

function setup() {
    ctx.font = "5em Arial";
    // set default values for tx & ty
    sliderE.min = 0;
    sliderE.max = canvas.width;
    sliderE.value = (canvas.width / 2) - (ctx.measureText("Hello World!").width / 2);
    sliderF.min = 0;
    sliderF.max = canvas.width;
    sliderF.value = canvas.height / 2;
    // add Event listeners
    sliderA.addEventListener("change",sliderDidChange,false);
    sliderB.addEventListener("change",sliderDidChange,false);
    sliderC.addEventListener("change",sliderDidChange,false);
    sliderD.addEventListener("change",sliderDidChange,false);
    sliderE.addEventListener("change",sliderDidChange,false);
    sliderF.addEventListener("change",sliderDidChange,false);
    sliderDidChange();
}

setup();

</script>

</body>
</html>
```

[View live example](http://audiocommander.github.com/transformMatrixDemo)

## Notes

The parameters of *transform* represent a matrix. This matrix is multiplied with the transformation matrix of the current context.

The arguments *a, b, c, d, e, f* are sometimes called *m11, m12, m21, m22, dx, dy* or *m11, m21, m12, m22, dx, dy*. Care should be taken in particular with the order of the second and third arguments (*b* and *c*) as their order varies from API to API; APIs sometimes use the notation *m12/m21* and sometimes *m21/m12* for those positions.

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
