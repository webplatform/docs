<div style='float: right;background: white;border:1px dashed black;padding: 1ex;margin-left: 1ex;'>

* [[CSS/Properties|List of Properties]]
** [[CSS/Properties#Color|Color]]
*** [[CSS/Properties/color|color]]
*** [[CSS/Properties/opacity|opacity]]

</div>

= color =

The color property describes the foreground color of an element's text content.

== Description ==

<table class="filehistory"><tr><th>Values
     </th><td><color value> | <color keyword> | currentColor | transparent | inherit
     </td></tr>
     <tr><th width="100">Initial value
     </th><td>Depends on user agent.<br />
[http://www.w3.org/TR/html5/rendering.html#fonts-and-colors HTML5] indicates that the initial value for the 'color' property is expected to be black, but users can easily change it in their user agent settings.
     </td></tr>
     <tr><th width="100">Applies to
     </th><td>All elements
     </td></tr>
     <tr><th width="100">Inherited
     </th><td>Yes
     </td></tr>
</table>

== Values ==
*<code><color value></code><br />The color can be specified as
** a [[CSS/Properties/color/RGB|hexadecimal RGB value]]: #faf or #ffaaff
** a [[CSS/Properties/color/RGB|RGB value]]: rgb(255, 160, 255) or rgb(100%, 62.5%, 100%)<br />Each value is from 0 to 255, or from 0% to 100%.
** a [[CSS/Properties/color/RGBA|RGBA value]]: rgba(255, 160, 255, 1) or rgb(100%, 62.5%, 100%, 1)<br />This variant includes an “alpha” component to allow specification of the opacity of a color. Values are in the range 0.0 (fully transparent) to 1.0 (fully opaque).
** a [[CSS/Properties/color/HSL|HSL value]]: hsl(0, 100%, 50%)<br />A triple (hue, saturation, lightness). hue is an angle in degrees. saturation and lightness are percentages (0-100%).
** a [[CSS/Properties/color/HSLA|HSLA value]]: hsl(0, 100%, 50%, 1)<br />This variant includes an “alpha” component to allow specification of the opacity of a color.  Values are in the range 0.0 (fully transparent) to 1.0 (fully opaque).

*<code><color keyword></code><br />One of the [[CSS/Properties/color/keywords|pre-defined color keywords]].

*<code>currentColor</code><br />Same as ‘inherit’.

*<code>transparent</code><br />Fully transparent. This keyword can be considered a shorthand for transparent black, rgba(0,0,0,0), which is its computed value.

*<code>inherit</code><br />Takes the same specified value as the property for the element's parent.

== Example ==
=== Example A ===
[style.css]
  body {
    '''color: #fff;'''
    background-color: #666;
  }

[index.html]
<pre>
  <body>
    <h1>CSS color property example</h1>
  </body>
</pre>

[[File:Csslist2_color.png]]


== Considerations ==

=== Separating foreground from background ===

In order to make it easier for users to see and hear content including separating foreground from background, [[http://www.w3.org/TR/2008/REC-WCAG20-20081211/ WCAG]] indicates the following:
* color is not used as the only visual means of conveying information, indicating an action, prompting a response, or distinguishing a visual element. [[http://www.w3.org/TR/2008/REC-WCAG20-20081211/#visual-audio-contrast-without-color Guideline 1.4.1]] (Level A)
* The visual presentation of text and images of text has a minimum contrast ratio of at least 4.5:1, with some exceptions. [[http://www.w3.org/TR/2008/REC-WCAG20-20081211/#visual-audio-contrast-contrast Contrast Minimum Guideline 1.4.3]] (Level AA)
* The visual presentation of text and images of text has an enhanced contrast ratio of at least 7:1 [[http://www.w3.org/TR/2008/REC-WCAG20-20081211/#visual-audio-contrast7 Guideline 1.4.6]] (Level AAA)

== CSS Reference ==

CSS defines the color property in [http://www.w3.org/TR/css3-color/ CSS Color], [http://www.w3.org/TR/css3-color/#foreground 3.1. Foreground color: the ‘color’ property].

== See also ==

* [http://www.w3.org/Style/CSS/Test/CSS3/Color/current/ css3-color conformance test suite]

[[Category:CSS]]