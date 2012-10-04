{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=x0|Data type=float|Description=The x-coordinate of the starting circle of the gradient.|Optional=}}
{{Method Parameter|Name=y0|Data type=float|Description=The y-coordinate of the starting circle of the gradient.|Optional=}}
{{Method Parameter|Name=r0|Data type=float|Description=The radius of the starting circle.|Optional=}}
{{Method Parameter|Name=x1|Data type=float|Description=The x-coordinate of the ending circle of the gradient.|Optional=}}
{{Method Parameter|Name=y1|Data type=float|Description=The y-coordinate of the ending circle of the gradient.|Optional=}}
{{Method Parameter|Name=r1|Data type=float|Description=The radius of the ending circle.|Optional=}}
|Method_applies_to=canvas/objects/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''ICanvasGradient'''

A [[canvas/objects/CanvasGradient|'''CanvasGradient''']] object that represents the radial gradient.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code example creates a rainbow-colored radial gradient. By  using  a mouse event, you can move it around the screen.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
  &lt;title&gt;Canvas Radial Gradient test &lt;/title&gt;
  &lt;style&gt; 
     canvas 
        {  
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 100%;
        }
   &lt;/style&gt;
&lt;/head&gt;
  &lt;body&gt;
    &lt;canvas height{{=}}"600" width{{=}}"600"&gt;&lt;/canvas&gt;
    &lt;script&gt;
      var canvas {{=}} document.getElementsByTagName('canvas')[0];
      body {{=}} document.getElementsByTagName('body')[0];
      if (canvas.getContext('2d')) 
      {  
        // Create the initial canvas and start the gradient.
        ctx {{=}} canvas.getContext('2d');
        ctx.clearRect(0, 0, 600, 600); 
        gradient {{=}} ctx.createRadialGradient(300,300,0,300,300,300);
        ctx.fillStyle {{=}} getColors(gradient); 
        ctx.fillRect(0,0,600,600); 
        body.onmousemove {{=}} function (event) 
        {
            var width {{=}} window.innerWidth,  
                height {{=}} window.innerHeight, 
                x {{=}} event.clientX, 
                y {{=}} event.clientY, 
                rx {{=}} 600 * x / width,  
                ry {{=}} 600 * y / height;
                
            gradient {{=}} ctx.createRadialGradient(rx, ry, 0, rx, ry, 300);
            ctx.fillStyle {{=}} getColors(gradient);            // Use the gradient for the fill style.
            ctx.fillStyle {{=}} gradient; 
            ctx.fillRect(0,0,600,600); 
       };
      }
             
      function getColors(gradient)  // Get the colors. Because they are used twice, get them when they are needed.
        {
          gradient.addColorStop("0","magenta");
          gradient.addColorStop(".25","blue");
          gradient.addColorStop(".50","green");
          gradient.addColorStop(".75","yellow");
          gradient.addColorStop("1.0","red");
          return(gradient);
        }
      &lt;/script&gt;             
   &lt;/body&gt;
 &lt;/html&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
You can use radial gradients  together  with the  [[canvas/methods/fillText|'''fillText''']] or [[canvas/methods/fillRect|'''fillRect''']] method. The following  illustration uses '''fillRect'''.

|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[canvas/objects/CanvasRenderingContext2D|CanvasRenderingContext2D]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}