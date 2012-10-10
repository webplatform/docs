== Specification ==

Khronos publishes the [http://www.khronos.org/registry/webgl/specs/latest/ WebGL Specification] and the [http://www.khronos.org/files/webgl/webgl-reference-card-1_0.pdf WebGL quick reference card].

== WebGL Context ==

A webgl context can be obtained by calling the getContext function on a [[canvas|Canvas Element]]

=== Syntax ===
<syntaxhighlight lang="javascript">var gl = canvas.getContext('webgl', attributes)</syntaxhighlight>

=== Arguments ===

# DOMString: 'webgl' or 'experimental-webgl'
# Object: WebGLContextAttributes

=== Return Value ===

A context object or null.

=== WebGLContextAttributes ===

* boolean alpha: default true
* boolean depth: default true
* boolean stencil: default false
* boolean antialias: default true
* boolean premultipliedAlpha: default true
* boolean preserveDrawingBuffer: default false

[[Category:WebGL]]