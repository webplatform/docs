{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=expression
|Data type=String
|Description='''Variant''' that specifies the function pointer or string that indicates the code to be executed when the specified interval has elapsed.
|Optional=No
}}{{Method Parameter
|Name=msec
|Data type=String
|Description='''Integer''' that specifies the number of milliseconds.
|Optional=No
}}{{Method Parameter
|Name=language
|Data type=String
|Description='''String''' that specifies one of the following values:
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''Integer'''

Integer. Returns an identifier that cancels the evaluation with the [[dom/methods/clearTimeout|'''clearTimeout''']] method.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example uses the '''setTimeout''' method to evaluate a simple expression after one second has elapsed.
|Code=window.setTimeout("alert('Hello, world')", 1000);
}}{{Single Example
|Description=The following example uses the '''setTimeout''' method to evaluate a slightly more complex expression after one second has elapsed.
|Code=var sMsg {{=}} "Hello, world";
window.setTimeout("alert(" + sMsg + ")", 1000);
}}{{Single Example
|Description=This example uses the '''setTimeout''' method to hide a '''input type{{=}}button''' object after three seconds. If the user clicks the '''Count Down''' button and then counts to three, the '''Now You See Me''' button disappears.
|Code=&lt;script type{{=}}"text/javascript"&gt;
function fnHide(oToHide){
   window.setTimeout("fnHide2(" + oToHide.id + ")", 3000);
}
function fnHide2(sID){
   var o {{=}} eval(sID);
   o.style.display{{=}}"none";
}
&lt;/script&gt;
&lt;input type{{=}}"button" value{{=}}"Count Down" 
    id{{=}}"oHideButton" onclick{{=}}"fnHide(this)"&gt;
}}{{Single Example
|Description=This example uses a function pointer to pass the data. In this case, the data is stored in a global variable because it cannot be passed directly. In the preceding example, the [[html/attributes/id|'''ID''']] of the button is passed as a parameter to the function invoked by the '''setTimeout''' method. This is possible only when a string is passed as the first argument.
|Code=&lt;script type{{=}}"text/javascript"&gt;
var g_oToHide {{=}} null;
function fnHide(oToHide){
    g_oToHide {{=}} oToHide;
    window.setTimeout(fnHide2, 3000);
}
function fnHide2(sID){
    if (g_oToHide) {
       g_oToHide.style.display{{=}}"none";
    }
}
&lt;/script&gt;
&lt;input type{{=}}"button" value{{=}}"Now you see me ..." 
    id{{=}}"oHideButton" onclick{{=}}"fnHide(this)"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setTimeout.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The specified expression or function is evaluated once. For repeated evaluation, use the [[dom/methods/setInterval|'''setInterval''']] method.
When you use the '''setTimeout''' method with Introduction to DHTML Behaviors, the value of ''expression'' should be a function pointer to call a function within the HTML Component (HTC) file or a string to call a function in the primary document.

'''Note'''  In Windows Internet Explorer, you cannot pass arguments to the callback function directly; however, you can simulate passing arguments by creating an anonymous closure function that references variables within scope of the call to [[dom/methods/setInterval|'''setInterval''']] or '''setTimeout'''. For more information, see [[dom/methods/setInterval|'''setInterval''']].
In versions earlier than Microsoft Internet Explorer 5, the first argument of '''setTimeout''' must be a string. Evaluation of the string is deferred until the specified interval elapses.
As of Internet Explorer 5, the first argument of '''setTimeout''' can be a string or a function pointer.

=== Reliability & timeout clamping ===
This API does not guarantee that timers will run exactly on schedule. Delays due to CPU load, other tasks, etc, are to be expected. Additionally a setTimeout or [[dom/methods/setInterval|setInterval]] call has a minimum interval of of 4 ms, as specified by the HTML4 spec.

Generally all browsers implement this timeout "clamp" to 4 ms, although some browsers also clamp to a higher value when the window is not focused. For instance, the minimum timeout for a setInterval call can be up to a second in Chrome when the tab is inactive.

|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.
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
|Manual_sections====Related pages (MSDN)===
*<code>window</code>
*<code>[[dom/methods/clearTimeout|clearTimeout]]</code>
*<code>[[apis/timing/methods/requestAnimationFrame|requestAnimationFrame]]</code>
*<code>[[apis/timing/methods/setImmediate|setImmediate]]</code>
*<code>[[dom/methods/setInterval|setInterval]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/DOM/window.setTimeout
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}