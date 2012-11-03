{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Adds the specified arc to the current subpath.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=String
|Description=The x-coordinate, in pixels, for the center point of the arc in relation to the upper-left corner of the canvas rectangle.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=String
|Description=The y-coordinate, in pixels, for the center point of the arc in relation to the upper-left corner of the canvas rectangle.
|Optional=No
}}{{Method Parameter
|Name=radius
|Data type=String
|Description=The radius or distance from the point (x,y) that the arc's path  follows.
|Optional=No
}}{{Method Parameter
|Name=startAngle
|Data type=String
|Description=The starting angle, in radians, where 0 is at the 3 o'clock position of the arc's circle.
|Optional=No
}}{{Method Parameter
|Name=endAngle
|Data type=String
|Description=The ending angle, in radians.
|Optional=No
}}{{Method Parameter
|Name=anticlockwise
|Data type=String
|Description='''true'''



The arc is drawn in a counterclockwise direction from start to end.


'''false'''



The arc  is drawn in a clockwise direction from start to end.
|Optional=No
}}
|Method_applies_to=canvas/objects/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{{{!}} class="wikitable"
{{!}}-
!Return code
!Description
{{!}}-
{{!}}S_OK
{{!}}The operation completed successfully.
{{!}}-
{{!}}IndexSizeError
{{!}}The  specified radius value  is negative.
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following code example shows several different arcs.
|Code=&lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
  &lt;script type{{=}}"text/javascript"&gt;
	 function curves()
        {
         var canvas {{=}} document.getElementById("canvas");
 	      if (canvas.getContext) 
          {
 	        var ctx {{=}} canvas.getContext("2d");
 	        for(var i{{=}}0;i&lt;2;i++)                            // Step through two rows.
            {   
                for(var j{{=}}0;j&lt;3;j++)                        // Step through three versions.    
                {
     	        ctx.beginPath();
 	            var x              {{=}} 25+j*50;               // The x-coordinate.
 	            var y              {{=}} 25+i*50;               // The y-coordinate.
 	            var radius         {{=}} 20;                    // The arc radius.
     	        var startAngle     {{=}} 0;                     // The starting point on the circle.
        	    var endAngle       {{=}} Math.PI+(Math.PI*j)/2; // The end point on the circle.
    	        var anticlockwise  {{=}} i%2{{=}}{{=}}0 ? false : true; // The direction of drawing.
 	
    	        ctx.arc(x,y,radius,startAngle,endAngle, anticlockwise); // Create the arc path.
 	            ctx.stroke();                               // Display the work.
 	            }
 	         }
           }
        }// Curves	  
  &lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;canvas id{{=}}"canvas" width{{=}}"300" height{{=}}"300"&gt;Sorry, canvas not supported&lt;/canvas&gt;
    &lt;button onclick{{=}}"curves();"&gt;Show arcs&lt;/button&gt;
&lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes=If the ''startAngle'' and ''endAngle''  angles are equal,  the '''arc'''  method  creates a circle. To convert degrees to radians use the following formula.
 <code>var radians {{=}} degrees * Math.PI/180</code>
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 9
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=*<code>[[canvas/objects/CanvasRenderingContext2D|CanvasRenderingContext2D]]</code>
*[[tutorials/canvas/canvas_tutorial|Canvas tutorial]]
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}