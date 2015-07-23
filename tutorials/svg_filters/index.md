{{Page_Title|SVG filters}}
{{Flags
|State=Not Ready
|Editorial notes=Stub
|Checked_Out=No
|High-level issues=Stub
}}
{{Byline}}
{{Summary_Section|CSS custom filters go way beyond the image-processing capabilities of CSS's pre-defined filter effects, allowing you to bend, fold, spindle, and mutilate otherwise flat web content.}}
{{Tutorial
|Content=
==Filters: a review==

<!--
* built-in CSS filter effects
* SVG filters, arguably "custom"
* custom CSS filters rely on GLSL
-->

==Custom filter terminology==

<!--
* GLSL            == Graphics Language Shading Language
* shader          == external GLSL program
* vertex shader   == manipulates mesh
* fragment shader == manipulates pixels along mesh surface
* uniforms        == global parameters
* attributes      == per-vertex parameters
* varyings        == per-vertex parameters passed to fragment shader (e.g. for lighting effects);
* tesselation     == how big is your mesh?
* vertices
* "textures"?
* uvs?
-->

==Vertex filters==

<!--
built-in attributes:

attribute vec4 a_position       ;
attribute vec2 a_texCoord       ; ???
attribute vec2 a_meshCoord      ;
attribute vec3 a_triangleCoord  ;

built-in uniforms:

uniform mat4 u_projectionMatrix ;
uniform vec2 u_textureSize      ; ???
uniform vec4 u_meshBox          ;
uniform vec2 u_tileSize         ;
uniform vec2 u_meshSize         ; ???

built-in varyings:

varying vec2 v_texCoord         ;


precision mediump float         ;

attribute vec4 a_position       ;
uniform mat4 u_projectionMatrix ;

no-op:

void main() {
    gl_Position = u_projectionMatrix * a_position;
}


-->

==Fragment filters==

<!--
no-op:

precision mediump float;

void main() {

    float r = 1.0;
    float g = 1.0;
    float b = 1.0;
    float a = 1.0;

    css_ColorMatrix = mat4( r, 0.0, 0.0, 0.0,
                      0.0, g, 0.0, 0.0,
                      0.0, 0.0, b, 0.0,
                      0.0, 0.0, 0.0, a );
}

-->

==custom() function syntax==

<!--
url(.vs)
mix( url(.fs) blend composite),
rows columns,
uniform_name value,
etc.
-->

==Coding the custom vertex filter==

<!--
-->

==Coding the custom fragment filter==

<!--
* css_ColorMatrix
* css_MixColor
-->

...
}}
{{Notes_Section}}
{{See_Also_Section
|Topic_clusters=Filters
|External_links=
* [http://www.w3.org/TR/filter-effects/ Filter Effects 1.0]
* [http://www.adobe.com/devnet/html5/articles/css-shaders.html Introducing CSS shaders: Cinematic effects for the web]
* [http://aerotwist.com/presentations/custom-filters/ WebGL &amp; Custom Filters]
}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}