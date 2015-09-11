---
title: reference
tags:
  - WebGL
uri: webgl/reference

---
## <span>Specification</span>

Khronos publishes the [WebGL Specification](http://www.khronos.org/registry/webgl/specs/latest/) and the [WebGL quick reference card](http://www.khronos.org/files/webgl/webgl-reference-card-1_0.pdf).

## <span>WebGL Context</span>

A webgl context can be obtained by calling the getContext function on a [Canvas Element](/canvas)

### <span>Syntax</span>

``` js
var gl = canvas.getContext('webgl', attributes) || canvas.getContext('experimental-webgll', attributes)
```

### <span>Arguments</span>

1.  DOMString: 'webgl' or 'experimental-webgl'
2.  Object: WebGLContextAttributes

### <span>Return Value</span>

A context object or null.

### <span>WebGLContextAttributes</span>

-   boolean alpha: default true
-   boolean depth: default true
-   boolean stencil: default false
-   boolean antialias: default true
-   boolean premultipliedAlpha: default true
-   boolean preserveDrawingBuffer: default false
