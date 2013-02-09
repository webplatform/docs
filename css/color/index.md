{{Page_Title|Color table}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Move Candidate, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
|Editorial notes={{Editorial/Move_Candidate
| color defines a CSS data type, so it should probably be moved to [[css/data types]] and be turned into the proper template
}}
}}
{{Summary_Section}}
{{Basic Page}}
{{Standardization_Status|}}
{{API_Name}}



{{See_Also_Section
|Topic_clusters=Visual Effects
}}
{{Notes_Section
|Import_Notes====Basic HTML Color Names===
Only 16 color "keywords" (names) are defined by the HTML 4.01 standard. These colors can always be rendered properly, regardless of the color resolution of the user's display card.
[[Image:named_colors.png]]
The Cascading Style Sheets, Level 2 Revision 1 (CSS2.1) specification includes "orange" (#FFA500) for a total of 17 color keywords.

====Extended Color Names====
In addition to the colors listed above, Internet Explorer supports a wide variety of named colors. Click the links below to view tables of colors sorted in various ways. The code example provides a table that you can sort dynamically by clicking the column headers. The named colors do not represent the full color spectrum; therefore, for best results, use RGB or HSL color values. The basic and extended color keywords are defined in [http://go.microsoft.com/fwlink/p/?linkid{{=}}203761 CSS Color Module Level 3].

*[[css/color/colors by name|Colors by Name]]
*[[css/color/colors by hue|Colors by Hue]]
*[[css/color/colors by lightness|Colors by Lightness]]
*[[css/color/colors by saturation|Colors by Saturation]]

[http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/colors/ColorTable.htm Click to view sample.]

===RGB Notation===
An RGB color value normally consists of a '#' immediately followed by a triad of two-digit hexadecimal numbers specifying the intensity of the corresponding color: (R)ed, (G)reen, and (B)lue. For example, the color value #FF0000 is rendered red because the red number is set to its highest value, FF (or 255, in decimal).
Each of the following style rules refer to the same color—namely, red. The three digit short-hand form is converted into the six digit form by replicating digits (#F00 becomes #FF0000). The functional <code>rgb()</code> notation uses a comma-separated list of integer numbers from 0 to 255, or percentage values.
 <code>em { color: #f00; }              /* #rgb */
 em { color: #ff0000; }           /* #rrggbb */
 em { color: rgb(255, 0, 0); }    /* integer range 0 - 255 */
 em { color: rgb(100%, 0%, 0%); } /* float range 0.0% - 100.0% */ 
 em { color: red; }               /* color keyword */ </code>

====Standards-Compliant Mode====
When you use the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration to specify standards-compliant mode, Microsoft Internet Explorer 6 and later versions ignore style sheet declarations that do not comply with Cascading Style Sheets, Level 1 (CSS1). According to CSS1, colors specified with hexadecimal RGB values must have a leading '#' character. Values like "FFFFFF" are ignored, not treated the same as "#FFFFFF" as in previous versions of Internet Explorer. This affects all Cascading Style Sheets (CSS) attributes and properties that accept an RGB color value.

===RGBA and HSL Notation===
In Internet Explorer 9, the RGB color model also includes an "alpha" value that specify the opacity of a color. The format of an RGBA value in the functional notation is a comma-separated list of three numerical values (either three integer numbers or three percentage values), followed by an decimal value between 0 and 1.
 <code>em { color: rgb(255, 0, 0) }        /* integer range 0 - 255 */
 em { color: rgba(255, 0, 0, 1) }    /* the same, with explicit opacity of 1 */
 em { color: rgb(100%, 0%, 0%) }     /* float range 0.0% - 100.0% */
 em { color: rgba(100%, 0%, 0%, 1) } /* the same, with explicit opacity of 1 */ </code>
'''Note'''  Though RGB values support hexadecimal notation, RGBA values do not.
Internet Explorer 9 also supports numerical hue, saturation, luminosity (HSL) colors as a complement to numerical RGB colors. HSL colors are encoding as a triple (hue, saturation, lightness).
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
*'''Saturation''' is represented as a percentage, where <code>100%</code> is full saturation and <code>0%</code> percent is a shade of gray.
*'''Lightness''' is also represented as a percentage, where <code>50%</code> percent is normal, <code>0%</code> is black, and <code>100%</code> is white.

The <code>hsl()</code> functional notation also has an <code>hsla()</code> alpha counterpart that allows you to specify opacity by using a floating point number between 1 and 0, as demonstrated in the following examples:
 <code>em { color: hsl(0, 100%, 50%) }   /* red */
 em { color: hsl(120, 100%, 50%) } /* lime green */ 
 em { color: hsl(120, 100%, 20%) } /* dark green */ 
 em { color: hsl(120, 100%, 80%) } /* light green */ 
 em { color: hsl(120, 75%, 75%) }  /* pastel green, and so on */ 
 p { color: hsla(240, 100%, 50%, 0.5) } /* semi-transparent solid blue */
 p { color: hsla(30, 100%, 50%, 0.1) }  /* very transparent solid orange */</code>

===System Colors===
Unlike the named colors, system colors have no numeric RGB equivalent because the exact color is not known until the Web page is viewed on the user's system. In this way, system colors are user-defined because users can choose their own system color scheme from the Windows Control Panel. System colors are especially useful for UI components.
Not all of the system colors are appropriate for a background or text color; however, some of them are intended to be used in combination. The following table demonstrates appropriate text and background colors, as they would appear on a Windows Vista system with default colors.
[[Image:named_system_colors.png]]
'''Note'''   The system color names have been deprecated in the Cascading Style Sheets, Level 3 (CSS3) recommendation.
For a complete list of sytem colors, see [[css/color/user-defined system colors|User-Defined System Colors]].

===Related topics===
;'''Other Resources''':CSS Enhancements in Internet Explorer 6
;CSS Enhancements in Internet Explorer 6:
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}