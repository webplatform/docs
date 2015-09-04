---
title: reference
tags:
  - WebGL
uri: webgl/reference

---
## Specification

Khronos publishes the [WebGL Specification](http://www.khronos.org/registry/webgl/specs/latest/) and the [WebGL quick reference card](http://www.khronos.org/files/webgl/webgl-reference-card-1_0.pdf).

## WebGL Context

A webgl context can be obtained by calling the getContext function on a [Canvas Element](/canvas)

### Syntax

``` {.js}
var gl = canvas.getContext('webgl', attributes) || canvas.getContext('experimental-webgll', attributes)
```

### Arguments

1.  DOMString: 'webgl' or 'experimental-webgl'
2.  Object: WebGLContextAttributes

### Return Value

A context object or null.

### WebGLContextAttributes

-   boolean alpha: default true
-   boolean depth: default true
-   boolean stencil: default false
-   boolean antialias: default true
-   boolean premultipliedAlpha: default true
-   boolean preserveDrawingBuffer: default false
