{{Page_Title|Color units}}
{{Flags
|Checked_Out=No
}}
{{API_Name}}
{{Summary_Section|Specify color and opacity}}
{{Concept_Page
|Content=Several different ways are available to specify simple color values:

* ''Keyword'' values specify common color names such as '''yellow''', '''black''', or '''transparent'''.

* Hexadecimal values specify opaque colors in the range of '''#000000''' ('''black''') to '''#ffffff''' ('''white'''), where  each pair of characters correspond to red, green, and blue.

* An '''rgb()''' function specifies red, green and blue values either as integers between 0 and 255 (corresponding to the hex values above), or as percentages. For example, '''rgb(256,0,0)''' and '''rgb(100%,0%,0%)''' both correspond to '''red'''.

* An '''hsl()''' function specifies hue, saturation, and luminance values. Hue values are specified as an [[css/data_types/angle|angle within the color wheel]] relative to '''red''', and numeric values default to degrees. Saturation specifies vividness as a percentage, with '''0%''' specifying various shades of gray. Luminence specifies brightness, with '''0%''' and '''100%'' corresponding to '''black''' and '''white''', and '''50%''' appearing as a more vivid hue. For example, '''hsl(0%,100%,50%)''' also corresponds to '''red'''.

The following variations on the above allow you to incorporate an
''alpha'' channel specifying transparencies:

* An '''rgba()''' function specifies red, green and blue values as described above, along with opacity expressed in decimal terms between 0 and 1. For example, '''rgba(100%,0%,0%,0.5)''' specifies a semi-transparent red, which appears as pink.

* An '''hsla()''' function specifies hue, saturation, and luminance as described above, but with an additional ''alpha'' channel. For example, '''hsla(0%,100%,50%,0.5)''' specifies the same semi-transparent red as the '''rgba()''' example above.

The recently introduced '''transparent''' color name specifies a full transparency.


}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=aside {
    color: white;              /* white letterforms */
    text-shadow: 0 0 4px red;  /* red backlight effect */
    text-shadow: 0 0 4px rgb(100%, 0%, 0%);  /* same */
    background-color: #777777; /* gray background */
}
.semitrans {
    /* elements behind this show through */
    background-color: rgba(50%, 50%, 50%, 0.5); 
}
}}
}}
{{Notes_Section
|Usage===Color Keywords==

.

{| class="wikitable"
|-
! Example !! Name !! Hex !! RGB !! HSL
|-
| <div style="background-color: aliceblue; color: aliceblue;"> Example </div> || aliceblue || #f0f8ff || rgb(94%,97%,100%) || hsl(208,100%,97%)
|-
| <div style="background-color: antiquewhite; color: antiquewhite;">Non-visible-example</div> || antiquewhite || #faebd7 || rgb(98%,92%,84%) || hsl(34,78%,91%)
|- 
| <div style="background-color: aqua; color: aqua;">Non-visible-example</div> || aqua || #00ffff || rgb(0%,100%,100%) || hsl(180,100%,50%)
|- 
| <div style="background-color: aquamarine; color: aquamarine;">Non-visible-example</div> || aquamarine || #7fffd4 || rgb(50%,100%,83%) || hsl(160,100%,75%)
|- 
| <div style="background-color: azure; color: azure;">Non-visible-example</div> || azure || #f0ffff || rgb(94%,100%,100%) || hsl(180,100%,97%)
|- 
| <div style="background-color: beige; color: beige;">Non-visible-example</div> || beige || #f5f5dc || rgb(96%,96%,86%) || hsl(60,56%,91%)
|- 
| <div style="background-color: bisque; color: bisque;">Non-visible-example</div> || bisque || #ffe4c4 || rgb(100%,89%,77%) || hsl(33,100%,88%)
|- 
| <div style="background-color: black; color: black;">Non-visible-example</div> || black || #000000 || rgb(0%,0%,0%) || hsl(0,0%,0%)
|- 
| <div style="background-color: blanchedalmond; color: blanchedalmond;">Non-visible-example</div> || blanchedalmond || #ffebcd || rgb(100%,92%,80%) || hsl(36,100%,90%)
|- 
| <div style="background-color: blue; color: blue;">Non-visible-example</div> || blue || #0000ff || rgb(0%,0%,100%) || hsl(240,100%,50%)
|- 
| <div style="background-color: blueviolet; color: blueviolet;">Non-visible-example</div> || blueviolet || #8a2be2 || rgb(54%,17%,89%) || hsl(271,76%,53%)
|- 
| <div style="background-color: brown; color: brown;">Non-visible-example</div> || brown || #a52a2a || rgb(65%,16%,16%) || hsl(0,59%,41%)
|- 
| <div style="background-color: burlywood; color: burlywood;">Non-visible-example</div> || burlywood || #deb887 || rgb(87%,72%,53%) || hsl(34,57%,70%)
|- 
| <div style="background-color: cadetblue; color: cadetblue;">Non-visible-example</div> || cadetblue || #5f9ea0 || rgb(37%,62%,63%) || hsl(182,25%,50%)
|- 
| <div style="background-color: chartreuse; color: chartreuse;">Non-visible-example</div> || chartreuse || #7fff00 || rgb(50%,100%,0%) || hsl(90,100%,50%)
|- 
| <div style="background-color: chocolate; color: chocolate;">Non-visible-example</div> || chocolate || #d2691e || rgb(82%,41%,12%) || hsl(25,75%,47%)
|- 
| <div style="background-color: coral; color: coral;">Non-visible-example</div> || coral || #ff7f50 || rgb(100%,50%,31%) || hsl(16,100%,66%)
|- 
| <div style="background-color: cornflowerblue; color: cornflowerblue;">Non-visible-example</div> || cornflowerblue || #6495ed || rgb(39%,58%,93%) || hsl(219,79%,66%)
|- 
| <div style="background-color: cornsilk; color: cornsilk;">Non-visible-example</div> || cornsilk || #fff8dc || rgb(100%,97%,86%) || hsl(48,100%,93%)
|- 
| <div style="background-color: crimson; color: crimson;">Non-visible-example</div> || crimson || #dc143c || rgb(86%,8%,24%) || hsl(348,83%,47%)
|- 
| <div style="background-color: cyan; color: cyan;">Non-visible-example</div> || cyan || #00ffff || rgb(0%,100%,100%) || hsl(180,100%,50%)
|- 
| <div style="background-color: darkblue; color: darkblue;">Non-visible-example</div> || darkblue || #00008b || rgb(0%,0%,55%) || hsl(240,100%,27%)
|- 
| <div style="background-color: darkcyan; color: darkcyan;">Non-visible-example</div> || darkcyan || #008b8b || rgb(0%,55%,55%) || hsl(180,100%,27%)
|- 
| <div style="background-color: darkgoldenrod; color: darkgoldenrod;">Non-visible-example</div> || darkgoldenrod || #b8860b || rgb(72%,53%,4%) || hsl(43,89%,38%)
|- 
| <div style="background-color: darkgray; color: darkgray;">Non-visible-example</div> || darkgray || #a9a9a9 || rgb(66%,66%,66%) || hsl(0,0%,66%)
|- 
| <div style="background-color: darkgreen; color: darkgreen;">Non-visible-example</div> || darkgreen || #006400 || rgb(0%,39%,0%) || hsl(120,100%,20%)
|- 
| <div style="background-color: darkgrey; color: darkgrey;">Non-visible-example</div> || darkgrey || #a9a9a9 || rgb(66%,66%,66%) || hsl(0,0%,66%)
|- 
| <div style="background-color: darkkhaki; color: darkkhaki;">Non-visible-example</div> || darkkhaki || #bdb76b || rgb(74%,72%,42%) || hsl(56,38%,58%)
|- 
| <div style="background-color: darkmagenta; color: darkmagenta;">Non-visible-example</div> || darkmagenta || #8b008b || rgb(55%,0%,55%) || hsl(300,100%,27%)
|- 
| <div style="background-color: darkolivegreen; color: darkolivegreen;">Non-visible-example</div> || darkolivegreen || #556b2f || rgb(33%,42%,18%) || hsl(82,39%,30%)
|- 
| <div style="background-color: darkorange; color: darkorange;">Non-visible-example</div> || darkorange || #ff8c00 || rgb(100%,55%,0%) || hsl(33,100%,50%)
|- 
| <div style="background-color: darkorchid; color: darkorchid;">Non-visible-example</div> || darkorchid || #9932cc || rgb(60%,20%,80%) || hsl(280,61%,50%)
|- 
| <div style="background-color: darkred; color: darkred;">Non-visible-example</div> || darkred || #8b0000 || rgb(55%,0%,0%) || hsl(0,100%,27%)
|- 
| <div style="background-color: darksalmon; color: darksalmon;">Non-visible-example</div> || darksalmon || #e9967a || rgb(91%,59%,48%) || hsl(15,72%,70%)
|- 
| <div style="background-color: darkseagreen; color: darkseagreen;">Non-visible-example</div> || darkseagreen || #8fbc8f || rgb(56%,74%,56%) || hsl(120,25%,65%)
|- 
| <div style="background-color: darkslateblue; color: darkslateblue;">Non-visible-example</div> || darkslateblue || #483d8b || rgb(28%,24%,55%) || hsl(248,39%,39%)
|- 
| <div style="background-color: darkslategray; color: darkslategray;">Non-visible-example</div> || darkslategray || #2f4f4f || rgb(18%,31%,31%) || hsl(180,25%,25%)
|- 
| <div style="background-color: darkslategrey; color: darkslategrey;">Non-visible-example</div> || darkslategrey || #2f4f4f || rgb(18%,31%,31%) || hsl(180,25%,25%)
|- 
| <div style="background-color: darkturquoise; color: darkturquoise;">Non-visible-example</div> || darkturquoise || #00ced1 || rgb(0%,81%,82%) || hsl(181,100%,41%)
|- 
| <div style="background-color: darkviolet; color: darkviolet;">Non-visible-example</div> || darkviolet || #9400d3 || rgb(58%,0%,83%) || hsl(282,100%,41%)
|- 
| <div style="background-color: deeppink; color: deeppink;">Non-visible-example</div> || deeppink || #ff1493 || rgb(100%,8%,58%) || hsl(328,100%,54%)
|- 
| <div style="background-color: deepskyblue; color: deepskyblue;">Non-visible-example</div> || deepskyblue || #00bfff || rgb(0%,75%,100%) || hsl(195,100%,50%)
|- 
| <div style="background-color: dimgray; color: dimgray;">Non-visible-example</div> || dimgray || #696969 || rgb(41%,41%,41%) || hsl(0,0%,41%)
|- 
| <div style="background-color: dimgrey; color: dimgrey;">Non-visible-example</div> || dimgrey || #696969 || rgb(41%,41%,41%) || hsl(0,0%,41%)
|- 
| <div style="background-color: dodgerblue; color: dodgerblue;">Non-visible-example</div> || dodgerblue || #1e90ff || rgb(12%,56%,100%) || hsl(210,100%,56%)
|- 
| <div style="background-color: firebrick; color: firebrick;">Non-visible-example</div> || firebrick || #b22222 || rgb(70%,13%,13%) || hsl(0,68%,42%)
|- 
| <div style="background-color: floralwhite; color: floralwhite;">Non-visible-example</div> || floralwhite || #fffaf0 || rgb(100%,98%,94%) || hsl(40,100%,97%)
|- 
| <div style="background-color: forestgreen; color: forestgreen;">Non-visible-example</div> || forestgreen || #228b22 || rgb(13%,55%,13%) || hsl(120,61%,34%)
|- 
| <div style="background-color: fuchsia; color: fuchsia;">Non-visible-example</div> || fuchsia || #ff00ff || rgb(100%,0%,100%) || hsl(300,100%,50%)
|- 
| <div style="background-color: gainsboro; color: gainsboro;">Non-visible-example</div> || gainsboro || #dcdcdc || rgb(86%,86%,86%) || hsl(0,0%,86%)
|- 
| <div style="background-color: ghostwhite; color: ghostwhite;">Non-visible-example</div> || ghostwhite || #f8f8ff || rgb(97%,97%,100%) || hsl(240,100%,99%)
|- 
| <div style="background-color: gold; color: gold;">Non-visible-example</div> || gold || #ffd700 || rgb(100%,84%,0%) || hsl(51,100%,50%)
|- 
| <div style="background-color: goldenrod; color: goldenrod;">Non-visible-example</div> || goldenrod || #daa520 || rgb(85%,65%,13%) || hsl(43,74%,49%)
|- 
| <div style="background-color: gray; color: gray;">Non-visible-example</div> || gray || #808080 || rgb(50%,50%,50%) || hsl(0,0%,50%)
|- 
| <div style="background-color: green; color: green;">Non-visible-example</div> || green || #008000 || rgb(0%,50%,0%) || hsl(120,100%,25%)
|- 
| <div style="background-color: greenyellow; color: greenyellow;">Non-visible-example</div> || greenyellow || #adff2f || rgb(68%,100%,18%) || hsl(84,100%,59%)
|- 
| <div style="background-color: grey; color: grey;">Non-visible-example</div> || grey || #808080 || rgb(50%,50%,50%) || hsl(0,0%,50%)
|- 
| <div style="background-color: honeydew; color: honeydew;">Non-visible-example</div> || honeydew || #f0fff0 || rgb(94%,100%,94%) || hsl(120,100%,97%)
|- 
| <div style="background-color: hotpink; color: hotpink;">Non-visible-example</div> || hotpink || #ff69b4 || rgb(100%,41%,71%) || hsl(330,100%,71%)
|- 
| <div style="background-color: indianred; color: indianred;">Non-visible-example</div> || indianred || #cd5c5c || rgb(80%,36%,36%) || hsl(0,53%,58%)
|- 
| <div style="background-color: indigo; color: indigo;">Non-visible-example</div> || indigo || #4b0082 || rgb(29%,0%,51%) || hsl(275,100%,25%)
|- 
| <div style="background-color: ivory; color: ivory;">Non-visible-example</div> || ivory || #fffff0 || rgb(100%,100%,94%) || hsl(60,100%,97%)
|- 
| <div style="background-color: khaki; color: khaki;">Non-visible-example</div> || khaki || #f0e68c || rgb(94%,90%,55%) || hsl(54,77%,75%)
|- 
| <div style="background-color: lavender; color: lavender;">Non-visible-example</div> || lavender || #e6e6fa || rgb(90%,90%,98%) || hsl(240,67%,94%)
|- 
| <div style="background-color: lavenderblush; color: lavenderblush;">Non-visible-example</div> || lavenderblush || #fff0f5 || rgb(100%,94%,96%) || hsl(340,100%,97%)
|- 
| <div style="background-color: lawngreen; color: lawngreen;">Non-visible-example</div> || lawngreen || #7cfc00 || rgb(49%,99%,0%) || hsl(90,100%,49%)
|- 
| <div style="background-color: lemonchiffon; color: lemonchiffon;">Non-visible-example</div> || lemonchiffon || #fffacd || rgb(100%,98%,80%) || hsl(54,100%,90%)
|- 
| <div style="background-color: lightblue; color: lightblue;">Non-visible-example</div> || lightblue || #add8e6 || rgb(68%,85%,90%) || hsl(195,53%,79%)
|- 
| <div style="background-color: lightcoral; color: lightcoral;">Non-visible-example</div> || lightcoral || #f08080 || rgb(94%,50%,50%) || hsl(0,79%,72%)
|- 
| <div style="background-color: lightcyan; color: lightcyan;">Non-visible-example</div> || lightcyan || #e0ffff || rgb(88%,100%,100%) || hsl(180,100%,94%)
|- 
| <div style="background-color: lightgoldenrodyellow; color: lightgoldenrodyellow;">Non-visible-example</div> || lightgoldenrodyellow || #fafad2 || rgb(98%,98%,82%) || hsl(60,80%,90%)
|- 
| <div style="background-color: lightgray; color: lightgray;">Non-visible-example</div> || lightgray || #d3d3d3 || rgb(83%,83%,83%) || hsl(0,0%,83%)
|- 
| <div style="background-color: lightgreen; color: lightgreen;">Non-visible-example</div> || lightgreen || #90ee90 || rgb(56%,93%,56%) || hsl(120,73%,75%)
|- 
| <div style="background-color: lightgrey; color: lightgrey;">Non-visible-example</div> || lightgrey || #d3d3d3 || rgb(83%,83%,83%) || hsl(0,0%,83%)
|- 
| <div style="background-color: lightpink; color: lightpink;">Non-visible-example</div> || lightpink || #ffb6c1 || rgb(100%,71%,76%) || hsl(351,100%,86%)
|- 
| <div style="background-color: lightsalmon; color: lightsalmon;">Non-visible-example</div> || lightsalmon || #ffa07a || rgb(100%,63%,48%) || hsl(17,100%,74%)
|- 
| <div style="background-color: lightseagreen; color: lightseagreen;">Non-visible-example</div> || lightseagreen || #20b2aa || rgb(13%,70%,67%) || hsl(177,70%,41%)
|- 
| <div style="background-color: lightskyblue; color: lightskyblue;">Non-visible-example</div> || lightskyblue || #87cefa || rgb(53%,81%,98%) || hsl(203,92%,75%)
|- 
| <div style="background-color: lightslategray; color: lightslategray;">Non-visible-example</div> || lightslategray || #778899 || rgb(47%,53%,60%) || hsl(210,14%,53%)
|- 
| <div style="background-color: lightslategrey; color: lightslategrey;">Non-visible-example</div> || lightslategrey || #778899 || rgb(47%,53%,60%) || hsl(210,14%,53%)
|- 
| <div style="background-color: lightsteelblue; color: lightsteelblue;">Non-visible-example</div> || lightsteelblue || #b0c4de || rgb(69%,77%,87%) || hsl(214,41%,78%)
|- 
| <div style="background-color: lightyellow; color: lightyellow;">Non-visible-example</div> || lightyellow || #ffffe0 || rgb(100%,100%,88%) || hsl(60,100%,94%)
|- 
| <div style="background-color: lime; color: lime;">Non-visible-example</div> || lime || #00ff00 || rgb(0%,100%,0%) || hsl(120,100%,50%)
|- 
| <div style="background-color: limegreen; color: limegreen;">Non-visible-example</div> || limegreen || #32cd32 || rgb(20%,80%,20%) || hsl(120,61%,50%)
|- 
| <div style="background-color: linen; color: linen;">Non-visible-example</div> || linen || #faf0e6 || rgb(98%,94%,90%) || hsl(30,67%,94%)
|- 
| <div style="background-color: magenta; color: magenta;">Non-visible-example</div> || magenta || #ff00ff || rgb(100%,0%,100%) || hsl(300,100%,50%)
|- 
| <div style="background-color: maroon; color: maroon;">Non-visible-example</div> || maroon || #800000 || rgb(50%,0%,0%) || hsl(0,100%,25%)
|- 
| <div style="background-color: mediumaquamarine; color: mediumaquamarine;">Non-visible-example</div> || mediumaquamarine || #66cdaa || rgb(40%,80%,67%) || hsl(160,51%,60%)
|- 
| <div style="background-color: mediumblue; color: mediumblue;">Non-visible-example</div> || mediumblue || #0000cd || rgb(0%,0%,80%) || hsl(240,100%,40%)
|- 
| <div style="background-color: mediumorchid; color: mediumorchid;">Non-visible-example</div> || mediumorchid || #ba55d3 || rgb(73%,33%,83%) || hsl(288,59%,58%)
|- 
| <div style="background-color: mediumpurple; color: mediumpurple;">Non-visible-example</div> || mediumpurple || #9370db || rgb(58%,44%,86%) || hsl(260,60%,65%)
|- 
| <div style="background-color: mediumseagreen; color: mediumseagreen;">Non-visible-example</div> || mediumseagreen || #3cb371 || rgb(24%,70%,44%) || hsl(147,50%,47%)
|- 
| <div style="background-color: mediumslateblue; color: mediumslateblue;">Non-visible-example</div> || mediumslateblue || #7b68ee || rgb(48%,41%,93%) || hsl(249,80%,67%)
|- 
| <div style="background-color: mediumspringgreen; color: mediumspringgreen;">Non-visible-example</div> || mediumspringgreen || #00fa9a || rgb(0%,98%,60%) || hsl(157,100%,49%)
|- 
| <div style="background-color: mediumturquoise; color: mediumturquoise;">Non-visible-example</div> || mediumturquoise || #48d1cc || rgb(28%,82%,80%) || hsl(178,60%,55%)
|- 
| <div style="background-color: mediumvioletred; color: mediumvioletred;">Non-visible-example</div> || mediumvioletred || #c71585 || rgb(78%,8%,52%) || hsl(322,81%,43%)
|- 
| <div style="background-color: midnightblue; color: midnightblue;">Non-visible-example</div> || midnightblue || #191970 || rgb(10%,10%,44%) || hsl(240,64%,27%)
|- 
| <div style="background-color: mintcream; color: mintcream;">Non-visible-example</div> || mintcream || #f5fffa || rgb(96%,100%,98%) || hsl(150,100%,98%)
|- 
| <div style="background-color: mistyrose; color: mistyrose;">Non-visible-example</div> || mistyrose || #ffe4e1 || rgb(100%,89%,88%) || hsl(6,100%,94%)
|- 
| <div style="background-color: moccasin; color: moccasin;">Non-visible-example</div> || moccasin || #ffe4b5 || rgb(100%,89%,71%) || hsl(38,100%,85%)
|- 
| <div style="background-color: navajowhite; color: navajowhite;">Non-visible-example</div> || navajowhite || #ffdead || rgb(100%,87%,68%) || hsl(36,100%,84%)
|- 
| <div style="background-color: navy; color: navy;">Non-visible-example</div> || navy || #000080 || rgb(0%,0%,50%) || hsl(240,100%,25%)
|- 
| <div style="background-color: oldlace; color: oldlace;">Non-visible-example</div> || oldlace || #fdf5e6 || rgb(99%,96%,90%) || hsl(39,85%,95%)
|- 
| <div style="background-color: olive; color: olive;">Non-visible-example</div> || olive || #808000 || rgb(50%,50%,0%) || hsl(60,100%,25%)
|- 
| <div style="background-color: olivedrab; color: olivedrab;">Non-visible-example</div> || olivedrab || #6b8e23 || rgb(42%,56%,14%) || hsl(80,60%,35%)
|- 
| <div style="background-color: orange; color: orange;">Non-visible-example</div> || orange || #ffa500 || rgb(100%,65%,0%) || hsl(39,100%,50%)
|- 
| <div style="background-color: orangered; color: orangered;">Non-visible-example</div> || orangered || #ff4500 || rgb(100%,27%,0%) || hsl(16,100%,50%)
|- 
| <div style="background-color: orchid; color: orchid;">Non-visible-example</div> || orchid || #da70d6 || rgb(85%,44%,84%) || hsl(302,59%,65%)
|- 
| <div style="background-color: palegoldenrod; color: palegoldenrod;">Non-visible-example</div> || palegoldenrod || #eee8aa || rgb(93%,91%,67%) || hsl(55,67%,80%)
|- 
| <div style="background-color: palegreen; color: palegreen;">Non-visible-example</div> || palegreen || #98fb98 || rgb(60%,98%,60%) || hsl(120,93%,79%)
|- 
| <div style="background-color: paleturquoise; color: paleturquoise;">Non-visible-example</div> || paleturquoise || #afeeee || rgb(69%,93%,93%) || hsl(180,65%,81%)
|- 
| <div style="background-color: palevioletred; color: palevioletred;">Non-visible-example</div> || palevioletred || #db7093 || rgb(86%,44%,58%) || hsl(340,60%,65%)
|- 
| <div style="background-color: papayawhip; color: papayawhip;">Non-visible-example</div> || papayawhip || #ffefd5 || rgb(100%,94%,84%) || hsl(37,100%,92%)
|- 
| <div style="background-color: peachpuff; color: peachpuff;">Non-visible-example</div> || peachpuff || #ffdab9 || rgb(100%,85%,73%) || hsl(28,100%,86%)
|- 
| <div style="background-color: peru; color: peru;">Non-visible-example</div> || peru || #cd853f || rgb(80%,52%,25%) || hsl(30,59%,53%)
|- 
| <div style="background-color: pink; color: pink;">Non-visible-example</div> || pink || #ffc0cb || rgb(100%,75%,80%) || hsl(350,100%,88%)
|- 
| <div style="background-color: plum; color: plum;">Non-visible-example</div> || plum || #dda0dd || rgb(87%,63%,87%) || hsl(300,47%,75%)
|- 
| <div style="background-color: powderblue; color: powderblue;">Non-visible-example</div> || powderblue || #b0e0e6 || rgb(69%,88%,90%) || hsl(187,52%,80%)
|- 
| <div style="background-color: purple; color: purple;">Non-visible-example</div> || purple || #800080 || rgb(50%,0%,50%) || hsl(300,100%,25%)
|- 
| <div style="background-color: red; color: red;">Non-visible-example</div> || red || #ff0000 || rgb(100%,0%,0%) || hsl(0,100%,50%)
|- 
| <div style="background-color: rosybrown; color: rosybrown;">Non-visible-example</div> || rosybrown || #bc8f8f || rgb(74%,56%,56%) || hsl(0,25%,65%)
|- 
| <div style="background-color: royalblue; color: royalblue;">Non-visible-example</div> || royalblue || #4169e1 || rgb(25%,41%,88%) || hsl(225,73%,57%)
|- 
| <div style="background-color: saddlebrown; color: saddlebrown;">Non-visible-example</div> || saddlebrown || #8b4513 || rgb(55%,27%,7%) || hsl(25,76%,31%)
|- 
| <div style="background-color: salmon; color: salmon;">Non-visible-example</div> || salmon || #fa8072 || rgb(98%,50%,45%) || hsl(6,93%,71%)
|- 
| <div style="background-color: sandybrown; color: sandybrown;">Non-visible-example</div> || sandybrown || #f4a460 || rgb(96%,64%,38%) || hsl(28,87%,67%)
|- 
| <div style="background-color: seagreen; color: seagreen;">Non-visible-example</div> || seagreen || #2e8b57 || rgb(18%,55%,34%) || hsl(146,50%,36%)
|- 
| <div style="background-color: seashell; color: seashell;">Non-visible-example</div> || seashell || #fff5ee || rgb(100%,96%,93%) || hsl(25,100%,97%)
|- 
| <div style="background-color: sienna; color: sienna;">Non-visible-example</div> || sienna || #a0522d || rgb(63%,32%,18%) || hsl(19,56%,40%)
|- 
| <div style="background-color: silver; color: silver;">Non-visible-example</div> || silver || #c0c0c0 || rgb(75%,75%,75%) || hsl(0,0%,75%)
|- 
| <div style="background-color: skyblue; color: skyblue;">Non-visible-example</div> || skyblue || #87ceeb || rgb(53%,81%,92%) || hsl(197,71%,73%)
|- 
| <div style="background-color: slateblue; color: slateblue;">Non-visible-example</div> || slateblue || #6a5acd || rgb(42%,35%,80%) || hsl(248,53%,58%)
|- 
| <div style="background-color: slategray; color: slategray;">Non-visible-example</div> || slategray || #708090 || rgb(44%,50%,56%) || hsl(210,13%,50%)
|- 
| <div style="background-color: slategrey; color: slategrey;">Non-visible-example</div> || slategrey || #708090 || rgb(44%,50%,56%) || hsl(210,13%,50%)
|- 
| <div style="background-color: snow; color: snow;">Non-visible-example</div> || snow || #fffafa || rgb(100%,98%,98%) || hsl(0,100%,99%)
|- 
| <div style="background-color: springgreen; color: springgreen;">Non-visible-example</div> || springgreen || #00ff7f || rgb(0%,100%,50%) || hsl(150,100%,50%)
|- 
| <div style="background-color: steelblue; color: steelblue;">Non-visible-example</div> || steelblue || #4682b4 || rgb(27%,51%,71%) || hsl(207,44%,49%)
|- 
| <div style="background-color: tan; color: tan;">Non-visible-example</div> || tan || #d2b48c || rgb(82%,71%,55%) || hsl(34,44%,69%)
|- 
| <div style="background-color: teal; color: teal;">Non-visible-example</div> || teal || #008080 || rgb(0%,50%,50%) || hsl(180,100%,25%)
|- 
| <div style="background-color: thistle; color: thistle;">Non-visible-example</div> || thistle || #d8bfd8 || rgb(85%,75%,85%) || hsl(300,24%,80%)
|- 
| <div style="background-color: tomato; color: tomato;">Non-visible-example</div> || tomato || #ff6347 || rgb(100%,39%,28%) || hsl(9,100%,64%)
|- 
| <div style="background-color: turquoise; color: turquoise;">Non-visible-example</div> || turquoise || #40e0d0 || rgb(25%,88%,82%) || hsl(174,72%,56%)
|- 
| <div style="background-color: violet; color: violet;">Non-visible-example</div> || violet || #ee82ee || rgb(93%,51%,93%) || hsl(300,76%,72%)
|- 
| <div style="background-color: wheat; color: wheat;">Non-visible-example</div> || wheat || #f5deb3 || rgb(96%,87%,70%) || hsl(39,77%,83%)
|- 
| <div style="background-color: white; color: white;">Non-visible-example</div> || white || #ffffff || rgb(100%,100%,100%) || hsl(0,0%,100%)
|- 
| <div style="background-color: whitesmoke; color: whitesmoke;">Non-visible-example</div> || whitesmoke || #f5f5f5 || rgb(96%,96%,96%) || hsl(0,0%,96%)
|- 
| <div style="background-color: yellow; color: yellow;">Non-visible-example</div> || yellow || #ffff00 || rgb(100%,100%,0%) || hsl(60,100%,50%)
|- 
| <div style="background-color: yellowgreen; color: yellowgreen;">Non-visible-example</div> || yellowgreen || #9acd32 || rgb(60%,80%,20%) || hsl(80,61%,50%)
|}
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Color Module Level 3
|URL=http://www.w3.org/TR/2011/REC-css3-color-20110607/
|Status=Recommendation
}}{{Related Specification
|Name=CSS Values and Units Module Level 3
|URL=http://www.w3.org/TR/css3-values/
|Status=Candidate Recommendation
}}
}}
{{See_Also_Section
|Manual_links=* [[tutorials/setting_color_in_css|Setting color in CSS]]
* [[css/color|color]]
* [[css/properties/color|color]]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}