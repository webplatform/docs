{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=x|Data type=float|Description=The horizontal scaling factor, where 1 equals unity or 100% scale.|Optional=}}
{{Method Parameter|Name=y|Data type=float|Description=The vertical scaling factor.|Optional=}}
|Method_applies_to=canvas/objects/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code example shows scaling when it draws several rectangles .
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
    &lt;title&gt;Scale example&lt;/title&gt;
  &lt;script type{{=}}"text/javascript"&gt;    
function draw()
{
  var canvas {{=}} document.getElementById("MyCanvas");
 	if (canvas.getContext) 
    {
 	  var ctx {{=}} canvas.getContext("2d");   
      ctx.beginPath();
      ctx.lineWidth {{=}} "3";
      ctx.strokeStyle {{=}} "blue";
      ctx.rect (5,5,300,250);  
      ctx.stroke();
      ctx.beginPath();
      ctx.lineWidth {{=}} "5";
      ctx.strokeStyle {{=}} "red";
      ctx.rect (150,200,300,150);
      ctx.stroke();
      ctx.beginPath();
      ctx.lineJoin {{=}} "round";
      ctx.lineWidth {{=}} "10";
      ctx.strokeStyle {{=}} "green";
      ctx.rect (250,50,150,250);
      ctx.stroke();     
    }      
}
function scaleRect()
{
    var canvas {{=}} document.getElementById("MyCanvas");
 	if (canvas.getContext) 
    {
 	  var ctx {{=}} canvas.getContext("2d");
      ctx.clearRect(0,0,canvas.width,canvas.height);    // Clear the rectangle before scaling.
      var xFactor {{=}} document.getElementById("xScale").value;
      var yFactor {{=}} document.getElementById("yScale").value;     
      ctx.scale(xFactor,yFactor);
      draw();
    }
}
function refresh()                 
   {
    window.location.reload( false );           // Reload the page.
   }
  &lt;/script&gt;
&lt;/head&gt;
&lt;body bgcolor{{=}}"lightgray" onload{{=}}"draw();"&gt;   
        &lt;div&gt;
            &lt;button onclick{{=}}"scaleRect()"&gt;Do scaling&lt;/button&gt;
                  
            &lt;select id{{=}}"xScale" name{{=}}"xScale"&gt;
                &lt;option value{{=}}".25"&gt;25%&lt;/option&gt;
                &lt;option value{{=}}".5"&gt;50%&lt;/option&gt;
                &lt;option value{{=}}".75"&gt;75%&lt;/option&gt;
                &lt;option value{{=}}"1"&gt;100%&lt;/option&gt;
                &lt;option value{{=}}"1.25"&gt;125%&lt;/option&gt;
                &lt;option value{{=}}"1.5"&gt;150%&lt;/option&gt;
                &lt;option value{{=}}"1.75"&gt;175%&lt;/option&gt;
                &lt;option value{{=}}"2."&gt;200%&lt;/option&gt;
                &lt;option value{{=}}"3"&gt;300%&lt;/option&gt;
            &lt;/select&gt;
            &lt;select id{{=}}"yScale" name{{=}}"yScale"&gt;
                &lt;option value{{=}}".25"&gt;25%&lt;/option&gt;
                &lt;option value{{=}}".5"&gt;50%&lt;/option&gt;
                &lt;option value{{=}}".75"&gt;75%&lt;/option&gt;
                &lt;option value{{=}}"1"&gt;100%&lt;/option&gt;        
                &lt;option value{{=}}"1.25"&gt;125%&lt;/option&gt;
                &lt;option value{{=}}"1.5"&gt;150%&lt;/option&gt;
                &lt;option value{{=}}"1.75"&gt;175%&lt;/option&gt;
                &lt;option value{{=}}"2."&gt;200%&lt;/option&gt;
                &lt;option value{{=}}"3"&gt;300%&lt;/option&gt;
            &lt;/select&gt;                
            &lt;button onclick{{=}}"refresh()"&gt;refresh page&lt;/button&gt;
    &lt;/div&gt;        
    &lt;div&gt;
	    &lt;canvas id{{=}}"MyCanvas" width{{=}}"600" height{{=}}"600"&gt; &lt;/canvas&gt; 
    &lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
When  you create a [[canvas/objects/CanvasRenderingContext2D|'''CanvasRenderingContext2D''']]  object, it has a transformation matrix that identifies the current state.  The '''scale''' method  modifies the transformation by multiplying the matrix by the  specified  factor. For example, <code>context.scale(1,.5)</code> halves the vertical (or y-axis) values  that are used in context and  leaves  the horizontal (or x-axis) values the same. Similarly, <code>context.scale(2,2)</code>  doubles  the size of the graphics.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 3


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