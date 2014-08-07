{{Page_Title}}
{{Flags
|Editorial notes=Not part of user_timing, resource_timing, or navigation_timing interfaces.
|Checked_Out=No
|High-level issues=Missing Relevant Sections
|Content=Incomplete, Compatibility Incomplete
}}
{{Standardization_Status|Mixed}}
{{API_Name}}
{{Summary_Section|A method to invoke at the optimal time a callback to update the frame of an animation.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=callback
|Data type=function
|Description=The animation code to be run when the system is ready.
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=window
|Return_value_name=handle
|Javascript_data_type=Number
|Return_value_description=A handle or ID to the animationFrame request that can be used to cancel the request if needed.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;requestAnimationFrame&lt;/title&gt;
&lt;style type{{=}}"text/css"&gt;
div { position: absolute; left: 10px; top:100px; padding: 50px;
  background: crimson; color: white }
&lt;/style&gt;

&lt;/head&gt;
&lt;body&gt;

&lt;div id{{=}}"animated"&gt;Hello there.&lt;/div&gt;
&lt;button onclick{{=}}"start()"&gt;Start&lt;/button&gt;
&lt;button onclick{{=}}"stop()"&gt;Stop&lt;/button&gt;
    &lt;script type{{=}}"text/javascript"&gt;
        var elm {{=}} document.getElementById("animated");
        var stopped;
        var requestId {{=}} 0;
        var starttime;

        function render(time) {
            // set left style to a function of time. 
          if (!stopped) {
            elm.style.left {{=}} ((Date.now() - starttime) / 4 % 600) + "px";
            requestId {{=}} window.requestAnimationFrame(render);
            }
        }

        function start() {
            starttime {{=}} Date.now();
            requestId {{=}} window.requestAnimationFrame(render);
            stopped {{=}} false;
        }
        function stop() {
            if (requestId) {
                window.cancelAnimationFrame(requestId);
            }
            stopped {{=}} true;
        }


&lt;/script&gt;


&lt;/body&gt;&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes=Unlike older animation techniques based on [[dom/Window/setTimeout|'''setTimeout''']] and [[dom/Window/setInterval|'''setInterval''']] methods, '''requestAnimationFrame''' based animation occurs when the system is ready.  This leads to smoother animations and less power consumption than animations because '''requestAnimationFrame''' takes the visibility of the web application and the refresh rate of the display  into account,
The '''requestAnimationFrame''' method creates only a single animation request.  To create continous animation, a new request must be registered for each frame.
To cancel an animation request before the animation function is called back, use [[dom/Window/cancelAnimationFrame|'''cancelAnimationFrame''']].
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Timing control for script-based animations
|URL=http://www.w3.org/TR/animation-timing/
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=24
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=21
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=14
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=6
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh773174(v=vs.85).aspx requestAnimationFrame]
|HTML5Rocks_link=
}}