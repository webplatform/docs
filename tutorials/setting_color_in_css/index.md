{{Flags}}
{{Summary_Section}}
{{Tutorial
|Content=
{{ CSSTutorialTOC() }}

 
{{previousPage("/en-US/docs/CSS/Getting_Started/Text_styles", "Text styles")}}This is the 8th section of the [[CSS Getting Started]] tutorial; it explains in details about how you can specify color in CSS. In your sample stylesheet, you introduce background colors.

 
== Information: Color ==
 
In this tutorial so far, you have used a limited number of named colors. CSS 2 supports 17 named colors in all. Some of the names might not be what you expect:

                                                  
{| border="1"
|-
| 
|black
| 
|gray
| 
|silver
| 
|white
| 
|-
|primaries
|red
| 
|lime
| 
|blue
| 
|-
|secondaries
|yellow
| 
|aqua
| 
|fuchsia
| 
|-
| 
|maroon
| 
|orange
| 
|olive
| 
|purple
| 
|green
| 
|navy
| 
|teal
| 
|}   
    Details 
Your browser might support many more named colors, like:

                
{| border="1"
|-
|dodgerblue
| 
|peachpuff
| 
|tan
| 
|firebrick
| 
|aquamarine
| 
|} 
For details of this extended list, see: [[SVG color keywords]] in the CSS 3 Color Module. Beware of using color names that your reader's browsers might not support.

  
For a larger palette, specify the red, green and blue components of the color you want by using a number sign (hash) and three ''hexadecimal'' digits in the range 0 – 9, a – f. The letters a – f represent the values 10 – 15:

                             
{| border="1"
|-
|black
| 
|<code>#000</code>
|-
|pure red
| 
|<code>#f00</code>
|-
|pure green
| 
|<code>#0f0</code>
|-
|pure blue
| 
|<code>#00f</code>
|-
|white
| 
|<code>#fff</code>
|} 
<br>
For the full palette, specify two hexadecimal digits for each component:

                             
{| border="1"
|-
|black
| 
|<code>#000000</code>
|-
|pure red
| 
|<code>#ff0000</code>
|-
|pure green
| 
|<code>#00ff00</code>
|-
|pure blue
| 
|<code>#0000ff</code>
|-
|white
| 
|<code>#ffffff</code>
|} 
You can usually get these six-digit hexadecimal codes from your graphics program or some other tool.

  
    Example 
With a little practice, you can adjust the three-digit colors manually for most purposes:

                                  
{| border="1"
|-
|Start with pure red:
| 
|<code>#f00</code>
|-
|To make it paler, add some green and blue:
| 
|<code>#f77</code>
|-
|To make it more orange, add a little extra green:
| 
|<code>#fa7</code>
|-
|To darken it, reduce all its components:
| 
|<code>#c74</code>
|-
|To reduce its saturation, make its components more equal:
| 
|<code>#c98</code>
|-
|If you make them exactly equal, you get gray:
| 
|<code>#ccc</code>
|} 
For a pastel shade like pale blue:

              
{| border="1"
|-
|Start with pure white:
| 
|<code>#fff</code>
|-
|Reduce the other components a little:
| 
|<code>#eef</code>
|}   
    More details 
You can also specify a color using decimal RGB values in the range 0 – 255, or percentages.

 
For example, this is maroon (dark red):

 
<pre>
rgb(128, 0, 0)

</pre>
 
For full details of how to specify colors, see: [[Colors]] in the CSS Specification.

 
For information on matching system colors like Menu and ThreeDFace, see: [[CSS2 System Colors]] in the CSS Specification.

  
=== Color properties ===
 
You have already used the {{ cssxref("color") }} property on text.

 
You can also use the {{ cssxref("background-color") }} property to change elements' backgrounds.

 
Backgrounds can be set to <code>transparent</code> to explicitly remove any color, revealing the parent element's background.

  
    Example 
The '''Example''' boxes in this tutorial use this pale yellow background:

 
<pre>
background-color: #fffff4;

</pre>
 
The '''More details''' boxes use this pale gray:

 
<pre>
background-color: #f4f4f4;

</pre>
   
== Action: Using color codes ==
 
# Edit your CSS file.
# Make the change shown here in bold, to give the initial letters a pale blue background. (The layout and comments in your file probably differ from the file shown here. Keep the layout and comments the way you prefer them.)
     <pre>
 /*** CSS Tutorial: Color page ***/
  
 /* page font */
 body {font: 16px "Comic Sans MS", cursive;}
  
 /* paragraphs */
 p {color: blue;}
 #first {font-style: italic;}
 
 /* initial letters */
 strong {
   color: red;
   background-color: #ddf;
   font: 200% serif;
   }
 
 .carrot {color: red;}
 .spinach {color: green;}
  </pre>
# Save the file and refresh your browser to see the result.
          
{| border="1"
|-
|'''C'''ascading '''S'''tyle '''S'''heets
|-
|'''C'''ascading '''S'''tyle '''S'''heets
|}  
}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Exercise question===
 
In your CSS file, change all the color names to 3-digit color codes without affecting the result (this cannot be done exactly, but you can get close. To do it exactly you need 6-digit codes, and you need to look up the CSS Specification or use a graphics tool to match the colors.)
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Color
|MSDN_link=
|HTML5Rocks_link=
}}