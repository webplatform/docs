{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=Not part of user_timing, resource_timing, or navigation_timing interfaces.
|Checked_Out=No
|High-level issues=Deletion Candidate, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Cancels a requestAnimationFrame request}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=handle
|Data type=any
|Description=A handle of the animation request to cancel. The handle is the value returned by [[dom/Window/requestAnimationFrame|'''requestAnimationFrame''']].
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=window
|Javascript_data_type=void
|Return_value_description=This method does not return a value.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;Script-based animation using requestAnimationFrame&lt;/title&gt;
&lt;style type{{=}}"text/css"&gt;
div { position: absolute; left: 10px; top:100px; padding: 50px;
  background: crimson; color: white }
&lt;/style&gt;

&lt;/head&gt;
&lt;body&gt;

&lt;div id{{=}}"animated" style{{=}}"left: 549.5px;"&gt;Hello there.&lt;/div&gt;
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
&lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Usage=Script based animations.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}229562 Timing control for script-based animations]
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Window.cancelAnimationFrame cancelAnimationFrame]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/windows/apps/hh453388.aspx cancelAnimationFrame Method]
|HTML5Rocks_link=
}}