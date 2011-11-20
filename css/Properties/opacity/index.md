<div style='float: right;background: white;border:1px dashed black;padding: 1ex;margin-left: 1ex;'>

* [[CSS/Properties|List of Properties]]
** [[CSS/Properties#Color|Color]]
*** [[CSS/Properties/color|color]]
*** [[CSS/Properties/opacity|opacity]]

</div>

= opacity =

The opacity property specifies the opacity of an element.

== Description ==
<table class="filehistory" width="400"><tr><th width="100">Values
     </th><td><alphavalue> | inherit
     </td></tr>
     <tr><th width="100">Initial value
     </th><td>1
     </td></tr>
     <tr><th width="100">Applies to
     </th><td>All elements
     </td></tr>
     <tr><th width="100">Inherited
     </th><td>No
     </td></tr>
</table>


== Values ==
*<code id="alphavalue"><alphavalue></code><br />Syntactically a <number>. The uniform opacity setting to be applied across an entire object. Any values outside the range 0.0 (fully transparent) to 1.0 (fully opaque) will be clamped to this range.


*<code>inherit</code><br />Takes the same specified value as the property for the element's parent.


== Example ==
=== Example A ===
[style.css]
  body {
    color: #fff;
    background-color: #666;
  }
  h1{
    background-color: red;
  }
  #op{
    '''opacity: 1.0;'''
  }
  #tr{
    '''opacity: 0.4;'''
  }

[index.html]
<pre>
  <body>
    <h1 id="op">CSS color property example(fully opaque)</h1>
    <h1 id="tr">CSS color property example(transparent)</h1>
  </body>
</pre>

[[File:Css3_colors_opacity_001.png]]

== CSS Reference ==
CSS Color defines the opacity property in [http://www.w3.org/TR/css3-color/#transparency 3.2. Transparency: the ‘opacity’ property].

[[Category:CSS]]