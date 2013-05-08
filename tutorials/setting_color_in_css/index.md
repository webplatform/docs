{{Page_Title|Setting color in CSS}}
{{Flags
|Checked_Out=No
}}
{{Byline}}
{{Summary_Section|This article explains in detail the different ways you can specify [[css/units/color|color]] in CSS.}}
{{Tutorial
|Content=== Information: Color ==
 
In this tutorial so far, you have used a limited number of named colors. CSS 2 supports 17 named colors in all. Some of the names might not be what you expect:

{{{!}} border="1"
{{!}}-
{{!}} 
{{!}}<p style="color:black;">black</p>
{{!}} 
{{!}}<p style="color:gray;">gray</p>
{{!}} 
{{!}}<p style="color:silver;">silver</p>
{{!}} 
{{!}}<p style="color:white;background-color:black;">white</p>
{{!}} 
{{!}}-
{{!}}primaries
{{!}}<p style="color:red;">red</p>
{{!}} 
{{!}}<p style="color:lime;">lime</p>
{{!}} 
{{!}}<p style="color:blue;">blue</p>
{{!}} 
{{!}}-
{{!}}secondaries
{{!}}<p style="color:yellow;">yellow</p>
{{!}} 
{{!}}<p style="color:aqua;">aqua</p>
{{!}} 
{{!}}<p style="color:fuchsia;">fuchsia</p>
{{!}} 
{{!}}-
{{!}} 
{{!}}<p style="color:maroon;">maroon</p>
{{!}} 
{{!}}<p style="color:orange;">orange</p>
{{!}} 
{{!}}<p style="color:olive;">olive</p>
{{!}} 
{{!}}<p style="color:purple;">purple</p>
{{!}} 
{{!}}<p style="color:green;">green</p>
{{!}} 
{{!}}<p style="color:navy;">navy</p>
{{!}} 
{{!}}<p style="color:teal;">teal</p>
{{!}} 
{{!}}}                                                  
   
===Further color keyword details===
Your browser might support many more named colors, like:

{{{!}} border="1"
{{!}}-
{{!}}<p style="color:dodgerblue;">dodgerblue</p>
{{!}} 
{{!}}<p style="color:peachpuff;">peachpuff</p>
{{!}} 
{{!}}<p style="color:tan;">tan</p>
{{!}} 
{{!}}<p style="color:firebrick;">firebrick</p>
{{!}} 
{{!}}<p style="color:aquamarine;">aquamarine
{{!}} 
{{!}}} 

For details of this extended list, see: [[SVG color keywords]] in the CSS 3 Color Module. Beware of using color names that your reader's browsers might not support.
  
For a larger palette, specify the red, green and blue components of the color you want by using a number sign (hash) and three ''hexadecimal'' digits in the range 0 – 9, a – f. The letters a – f represent the values 10 – 15:

{{{!}} border="1"
{{!}}-
{{!}}black
{{!}} 
{{!}}<code style="color:#000;">#000</code>
{{!}}-
{{!}}pure red
{{!}} 
{{!}}<code style="color:#f00;">#f00</code>
{{!}}-
{{!}}pure green
{{!}} 
{{!}}<code style="color:#0f0;">#0f0</code>
{{!}}-
{{!}}pure blue
{{!}} 
{{!}}<code style="color:#00f;">#00f</code>
{{!}}-
{{!}}white
{{!}} 
{{!}}<code style="color:#fff;background-color:#000">#fff</code>
{{!}}} 

For the full palette, specify two hexadecimal digits for each component:
                             
{{{!}} border="1"
{{!}}-
{{!}}black
{{!}} 
{{!}}<code style="color:#000000;">#000000</code>
{{!}}-
{{!}}pure red
{{!}} 
{{!}}<code style="color:#ff0000;">#ff0000</code>
{{!}}-
{{!}}pure green
{{!}} 
{{!}}<code style="color:#00ff00;">#00ff00</code>
{{!}}-
{{!}}pure blue
{{!}} 
{{!}}<code style="color:#0000ff;">#0000ff</code>
{{!}}-
{{!}}white
{{!}} 
{{!}}<code style="color:#ffffff;background-color:#000000;">#ffffff</code>
{{!}}} 

You can usually get these six-digit hexadecimal codes from your graphics program or some other tool.

  
===Further hex examples=== 

With a little practice, you can adjust the three-digit colors manually for most purposes:
                                  
{{{!}} border="1"
{{!}}-
{{!}}Start with pure red:
{{!}} 
{{!}}<code style="color:#f00;">#f00</code>
{{!}}-
{{!}}To make it paler, add some green and blue:
{{!}} 
{{!}}<code style="color:#f77;">#f77</code>
{{!}}-
{{!}}To make it more orange, add a little extra green:
{{!}} 
{{!}}<code style="color:#fa7;">#fa7</code>
{{!}}-
{{!}}To darken it, reduce all its components:
{{!}} 
{{!}}<code style="color:#c74;">#c74</code>
{{!}}-
{{!}}To reduce its saturation, make its components more equal:
{{!}} 
{{!}}<code style="color:#c98;">#c98</code>
{{!}}-
{{!}}If you make them exactly equal, you get gray:
{{!}} 
{{!}}<code style="color:#ccc;">#ccc</code>
{{!}}} 

For a pastel shade like pale blue:

              
{{{!}} border="1"
{{!}}-
{{!}}Start with pure white:
{{!}} 
{{!}}<code style="color:#fff;background-color:black;">#fff</code>
{{!}}-
{{!}}Reduce the other components a little:
{{!}} 
{{!}}<code style="color:#eef;">#eef</code>
{{!}}}   

==RGB colors== 

You can also specify a color using decimal RGB values in the range 0 – 255, or percentages. For example, this is maroon (dark red):

<pre>rgb(128, 0, 0)</pre>
 
For full details of how to specify colors, see: [[Colors]] in the CSS Specification. For information on matching system colors like Menu and ThreeDFace, see: [[CSS2 System Colors]] in the CSS Specification.

=== Color properties ===
 
You have already used the [color] property on text.You can also use the [background-color] property to change elements' backgrounds. Backgrounds can be set to <code>transparent</code> to explicitly remove any color, revealing the parent element's background.

<pre style="background-color: #fffff4;">background-color: #fffff4;</pre>
 
The '''More details''' boxes use this pale gray:

 
<pre style="background-color: #f4f4f4;">background-color: #f4f4f4;</pre>
   
== Action: Using color codes ==
 
<ol>
<li><p>Edit your CSS file; make the change shown here in bold, to give the initial letters a pale blue background. (The layout and comments in your file probably differ from the file shown here. Keep the layout and comments the way you prefer them.)</p>

<pre>/*** CSS Tutorial: Color page ***/
  
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
.spinach {color: green;}</pre></li>

<li><p>Save the file and refresh your browser to see the result.</p></li>
</ol> 

<p class="note">Need to add screenshot of the result?</p>
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=* [[css/units/color|color]]
* [http://www.w3.org/TR/CSS2/syndata.html#color-units Cascading Style Sheets Level 2 Revision 1 (CSS 2.1) Specification, 4 Syntax and basic data types, 4.3.6 Colors]
* [http://www.w3.org/TR/css3-color/#svg-color CSS Color Module Level 3 , 4.3. Extended color keywords]

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