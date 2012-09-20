{{Flags}}
{{Summary_Section}}
{{Tutorial
|Content=In all of our previous examples, shapes were always drawn one on top of the other. This is more than adequate for most situations. This, for instance, limits in what order composite shapes are built up. We can however change this behaviour by setting the <code>globalCompositeOperation</code> property.

==<code>globalCompositeOperation</code>==

We can not only draw new shapes behind existing shapes but we can also use it to mask off certain areas, clear sections from the canvas (not limited to rectangles like the <code>clearRect</code> method does) and more.

<div style="border: 1px solid rgb(208, 221, 158); background: rgb(239, 248, 206) none repeat scroll 0% 50%; padding-left: 10px">

<code>'''globalCompositeOperation''' = type</code>

</div>

<code>type</code> is a string representing any one of twelve compositing operations. Each of the available types is described below.

'''Note:''' In all of the examples below the blue square is drawn first and referred to as 'existing canvas content'. The red circle is drawn second and referred to as 'new shape'.

{| style="width: 100%"
| style="padding: 5px; vertical-align: top" |
'''source-over''' (default)<br /> This is the default setting and draws new shapes on top of the existing canvas content.
| style="padding: 5px; vertical-align: top" |
[[Image:=Canvas_composite_srcovr.png|Image:Canvas_composite_srcovr.png]]
| style="padding: 5px; vertical-align: top" |
'''destination-over'''<br /> New shapes are drawn behind the existing canvas content.
| style="padding: 5px; vertical-align: top" |
[[Image:=Canvas_composite_destovr.png|Image:Canvas_composite_destovr.png]]
|-
| style="padding: 5px; vertical-align: top" |
'''source-in'''<br /> The new shape is drawn only where both the new shape and the destination canvas overlap. Everything else is made transparent
| style="padding: 5px; vertical-align: top" |
[[Image:=Canvas_composite_srcin.png|Image:Canvas_composite_srcin.png]]
| style="padding: 5px; vertical-align: top" |
'''destination-in'''<br /> The existing canvas content is kept where both the new shape and existing canvas content overlap. Everything else is made transparent.
| style="padding: 5px; vertical-align: top" |
[[Image:=Canvas_composite_destin.png|Image:Canvas_composite_destin.png]]
|-
| style="padding: 5px; vertical-align: top" |
'''source-out'''<br /> The new shape is drawn where it doesn't overlap the existing canvas content.
| style="padding: 5px; vertical-align: top" |
[[Image:=Canvas_composite_srcout.png|Image:Canvas_composite_srcout.png]]
| style="padding: 5px; vertical-align: top" |
'''destination-out'''<br /> The existing content is kept where it doesn't overlap the new shape.
| style="padding: 5px; vertical-align: top" |
[[Image:=Canvas_composite_destout.png|Image:Canvas_composite_destout.png]]
|-
| style="padding: 5px; vertical-align: top" |
'''source-atop'''<br /> The new shape is only drawn where it overlaps the existing canvas content.
| style="padding: 5px; vertical-align: top" |
[[Image:=Canvas_composite_srcatop.png|Image:Canvas_composite_srcatop.png]]
| style="padding: 5px; vertical-align: top" |
'''destination-atop'''<br /> The existing canvas is only kept where it overlaps the new shape. The new shape is drawn behind the canvas content.
| style="padding: 5px; vertical-align: top" |
[[Image:=Canvas_composite_destatop.png|Image:Canvas_composite_destatop.png]]
|-
| style="padding: 5px; vertical-align: top" |
'''lighter'''<br /> Where both shapes overlap the color is determined by adding color values.
| style="padding: 5px; vertical-align: top" |
[[Image:=Canvas_composite_lighten.png|Image:Canvas_composite_lighten.png]]
| style="padding: 5px; vertical-align: top" |
'''darker''' <span class="unimplementedInline">Unimplemented</span><br /> Where both shapes overlap the color is determined by subtracting color values.

This value is supported until (Firefox 3.6 / Thunderbird 3.1 / Fennec 1.0). Support has been removed from later versions (due to removal from the canvas specification).
| style="padding: 5px; vertical-align: top" |
[[Image:=Canvas_composite_darken.png|Image:Canvas_composite_darken.png]]
|-
| style="padding: 5px; vertical-align: top" |
'''xor'''<br /> Shapes are made transparent where both overlap and drawn normal everywhere else.
| style="padding: 5px; vertical-align: top" |
[[Image:=Canvas_composite_xor.png|Image:Canvas_composite_xor.png]]
| style="padding: 5px; vertical-align: top" |
'''copy'''<br /> Only draws the new shape and removes everything else.
| style="padding: 5px; vertical-align: top" |
[[Image:=Canvas_composite_copy.png|Image:Canvas_composite_copy.png]]
|}

'''Note:''' Currently the <code>copy</code> setting doesn't do anything in the Gecko 1.8 based browsers (Firefox 1.5 betas, etc).

[/samples/canvas-tutorial/6_1_canvas_composite.html View all the examples]

==Clipping paths==

[[Image:=Canvas_clipping_path.png]]A clipping path is like a normal canvas shape but it acts as a mask to hide unwanted parts of shapes. This is visualized in the image on the right. The red star shape is our clipping path. Everything that falls outside of this path won't get drawn on the canvas.

If we compare clipping paths to the <code>globalCompositeOperation</code> property we've seen above; settings that achieve more or less the same effect are <code>source-in</code> and <code>source-atop</code>. The most important differences between the two are that clipping paths are never actually drawn to the canvas and the clipping path is never affected by adding new shapes. This makes clipping paths ideal for drawing multiple shapes in a restricted area.

In the chapter about [/en/Canvas_tutorial/Drawing_shapes#Drawing_paths Drawing shapes] I only mentioned the <code>stroke</code> and <code>fill</code> methods, but there's a third method we can use with paths, called <code>clip</code>.

<div style="border: 1px solid rgb(208, 221, 158); background: rgb(239, 248, 206) none repeat scroll 0% 50%; padding-left: 10px">

<code>'''clip'''()</code>

</div>

We use the <code>clip</code> method to create a new clipping path. By default the canvas element has a clipping path that's the exact same size as the canvas itself (i.e. no clipping occurs).

====A <code>clip</code> example====

[[Image:=Canvas_clip.png]]In this example I'll be using a circular clipping path to restrict the drawing of a set of random stars to a particular region.

In the first few lines of code I draw a black rectangle the size of the canvas as a backdrop and translate the origin to the center. Below this I create the circular clipping path by drawing an arc. By calling the <code>clip</code> method the clipping path is created. Clipping paths are also part of the canvas save state. If we wanted to keep the original clipping path we could have saved the canvas state before creating the new one.

Everything that's drawn after creating the clipping path will only appear inside that path. You can see this clearly in the linear gradient that's drawn next. After this a set of 50 randomly positioned and scaled stars is drawn (I'm using a custom function for this). Again the stars only appear inside the defined clipping path.

[/samples/canvas-tutorial/6_2_canvas_clipping.html View this example]

 function draw() {
   var ctx = document.getElementById('canvas').getContext('2d');
   ctx.fillRect(0,0,150,150);
   ctx.translate(75,75);
 
   // Create a circular clipping path
   ctx.beginPath();
   ctx.arc(0,0,60,0,Math.PI*2,true);
   ctx.clip();
 
   // draw background
   var lingrad = ctx.createLinearGradient(0,-75,0,75);
   lingrad.addColorStop(0, '#232256');
   lingrad.addColorStop(1, '#143778');
   
   ctx.fillStyle = lingrad;
   ctx.fillRect(-75,-75,150,150);
 
   // draw stars
   for (var j=1;j<50;j++){
     ctx.save();
     ctx.fillStyle = '#fff';
     ctx.translate(75-Math.floor(Math.random()*150),
                   75-Math.floor(Math.random()*150));
     drawStar(ctx,Math.floor(Math.random()*4)+2);
     ctx.restore();
   }
   
 }
 function drawStar(ctx,r){
   ctx.save();
   ctx.beginPath()
   ctx.moveTo(r,0);
   for (var i=0;i<9;i++){
     ctx.rotate(Math.PI/5);
     if(i%2 == 0) {
       ctx.lineTo((r/0.525731)*0.200811,0);
     } else {
       ctx.lineTo(r,0);
     }
   }
   ctx.closePath();
   ctx.fill();
   ctx.restore();
 }

[[canvas/tutorial/Canvas tutorial/Transformations|&lt;&lt;Previous      ||    ]][[canvas/tutorial/Canvas tutorial/Basic animations|   Next&gt;&gt;]]

}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/Canvas_tutorial/Compositing
|MSDN_link=
|HTML5Rocks_link=
}}