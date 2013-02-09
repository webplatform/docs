{{Page_Title|color}}
{{Flags}}
{{Summary_Section|This page explains the different mechanisms available in HTML and CSS to specify colors.}}
{{Basic Page}}
{{Page_Title|color}}
{{Flags}}
{{Summary_Section|This page explains the different mechanisms available in HTML and CSS to specify colors.}}
{{Basic Page}}
==Basic HTML Color keywords==

The [http://www.w3.org/TR/REC-html40/types.html#h-6.5 HTML 4.01 spec] defines 16 color keywords. These colors can always be rendered properly, regardless of the color resolution of the user's display card. As an example, you can specify pure red text in CSS with the following

<syntaxHighlight>color: red; /* color rendered pure red */</syntaxHighlight>

[[Image:named_system_colors.png]]

The [http://www.w3.org/TR/CSS2/syndata.html#color-units Cascading Style Sheets, Level 2 Revision 1 (CSS2.1)] specification includes "orange" (#FFA500) for a total of 17 color keywords.

==Extended Color keywords==

In addition to the colors listed above, most browsers support an extended list of color keywords. The links below point to tables of colors sorted in various ways. The named colors do not represent the full color spectrum; therefore, for best results, use RGB or HSL color values. The basic and extended color keywords are defined in the [http://www.w3.org/TR/css3-color/#svg-color CSS Color Module Level 3 Extended Color Keywords] section.

*[[css/color/colors by name|Colors by Name]]
*[[css/color/colors by hue|Colors by Hue]]
*[[css/color/colors by lightness|Colors by Lightness]]
*[[css/color/colors by saturation|Colors by Saturation]]

===Hexadecimal and RGB Notation===

An RGB color value can be specified in two ways:

* A '#' immediately, followed by a triad of two-digit hexadecimal numbers specifying the intensity of the three component color channels: red, green, and blue, respectively.

<syntaxHighlight>color: #FF0000 /* text rendered pure red because the red channel is set to its highest value, FF.*/</syntaxHighlight>

Note that most browsers support abbreviated syntax for hex colors where both numbers are the same, in each channel. So for example, the above color could be written <code>#F00</code>. However, it is safest to use the full color definition.

* The RGB() function, which contains three values delimited by commas specifying the intensity of the three component color channels: red, green, and blue, respectively. The above red color can be specified by either of the following:

<syntaxHighlight>color: rgb(255,0,0) /* text rendered pure red because the red channel is set to its highest integer value, 255.*/
color: rgb(100%,0%,0%) /* text rendered pure red because the red channel is set to its highest percentage value, 100%.*/</syntaxHighlight>

Why 255? modern computers use 256-bit color, which means they can display around 16.7 million different colors (256 x 256 x 256; hexadecimal numbers have 16 different values, 0-9 and then a-f — 16 x 16 = 255). And since computers count from 0, not 1, the value range is 0-255, not 1-256.

==RGBA Notation==

In modern browsers (Opera, Firefox, Chrome, Safari, and Internet Explorer 9+), a counterpart to the RGB color model is supported — RGBA — which can also accept an "alpha" value specifying the opacity of a color. The format of an RGBA value is the same as RGB, with the addition of a numerical value between 0 (completely transparent and therefore invisible) and 1 (completely opaque).

<syntaxHighlight>color: rgba(255,0,0,0.5) /* text rendered semi-transparent red */
color: rgba(100%,0%,0%,0.5) /* text rendered semi-transparent red */</syntaxHighlight>

==HSL and HSLA notation==

Modern browsers (Opera, Firefox, Chrome, Safari, and Internet Explorer 9+) also support an <acronym title="Hue Saturation Lightness">HSL</acronym> color model, which is also a function taking three values:

* The hue takes a degree value in the range of 0-360, representing how far round a standard colour wheel the color sits. The table below gives you an idea of how this works.

{{{!}} class="wikitable"
{{!}}-
!Degree
!Name
!Color
{{!}}-
{{!}}0°
{{!}}red
{{!}}[[Image:FF0000.png]]
{{!}}-
{{!}}60
{{!}}yellow
{{!}}[[Image:FFFF00.png]]
{{!}}-
{{!}}120
{{!}}lime
{{!}}[[Image:00FF00.png]]
{{!}}-
{{!}}180
{{!}}cyan
{{!}}[[Image:00FFFF.png]]
{{!}}-
{{!}}240
{{!}}blue
{{!}}[[Image:0000FF.png]]
{{!}}-
{{!}}300
{{!}}magenta
{{!}}[[Image:FF00FF.png]]
{{!}}-
{{!}}360
{{!}}red
{{!}}[[Image:FF0000.png]]
{{!}}}

* Saturation is represented as a percentage, where <code>100%</code> is full color saturation and <code>0%</code> percent is a shade of gray.
* Lightness is also represented as a percentage, where <code>50%</code> percent is normal, <code>0%</code> is pure black, and <code>100%</code> is pure white.

HSL also has a corresponding function that accepts an alpha channel value — HSLA <code>hsla()</code> alpha counterpart that allows you to specify opacity by using a numerical value between 1 and 0.

<syntaxHighlight>color: hsl(0, 100%, 50%) /* red */
color: hsla(0, 100%, 50%, 0.5) /* semi-transparent red */
 
color: hsl(120, 100%, 50%) /* lime green */ 
color: hsl(120, 100%, 20%) /* dark green */ 
color: hsl(120, 100%, 80%) /* light green */ 
color: hsl(120, 75%, 75%)  /* pastel green */ </syntaxHighlight>

==System Colors==

It is also possible to specify system colors, so you can specify for example that you want your text to be the same color as your highlighted text; these are only supported on Windows. Unlike the named colors, system colors have no numeric RGB equivalent because the exact color is not known until the Web page is viewed on the user's system. In this way, system colors are user-defined because users can choose their own system color scheme from the Windows Control Panel. The following table demonstrates appropriate text and background colors, as they would appear on a Windows Vista system with default colors.

[[Image:named_system_colors.png]]

Note that the system color names have been deprecated in the http://www.w3.org/TR/css3-color/ CSS Color Module Level 3] recommendation, and since they are Windows-only, so it is advisable to not use them.

For a complete list of system colors, see [[css/color/user-defined system colors|User-Defined System Colors]].

{{Standardization_Status|}}
{{API_Name}}

==currentColor==

* You can use the <code>currentColor</code> value to set a color to the computed value of the element's <code>color</code> propety. for example, the background color of the div in the following example will be red, the same color as the <code>color</code> of it's parent element.

&lt;article style="color:red"&gt;
  &lt;p&gt;This is a sample article&lt;/p&gt;
  
  &lt;div style="background-color:currentColor"&gt;
    &lt;p&gt;This is some kind of highlight box.&lt;/p&gt;
  &lt;/div&gt;
&lt;/article&gt;

==transparent keyword==

Note that the [http://www.w3.org/TR/css3-color/ CSS Color Module Level 3] spec defines a keyword <code>transparent</code>, which is very useful for overriding previously set colors when required. It is equivalent to rgba(0,0,0,0), which is completely transparent black.

This value used to only be defined as an override value for the [[css/properties/background|background]] and [[css/properties/border|border property]], until it was defined as a true value in CSS3. <code>transparent</code> is supported on all properties in al modern browsers including IE9+.

==Opacity property==

You can set the opacity of an entire element using the [[css/properties/opacity|opacity property]].

{{See_Also_Section
|Topic_clusters=Visual Effects
}}




{{Notes_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Notes_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}