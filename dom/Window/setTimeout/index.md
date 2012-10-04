{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=expression|Data type=VARIANT|Description='''Variant''' that specifies the function pointer or string that indicates the code to be executed when the specified interval has elapsed.|Optional=}}
{{Method Parameter|Name=msec|Data type=Integer|Description='''Integer''' that specifies the number of milliseconds.|Optional=}}
{{Method Parameter|Name=language|Data type=VARIANT|Description='''String''' that specifies one of the following values:|Optional=}}
|Method_applies_to=dom/window
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''Integer'''

Integer. Returns an identifier that cancels the evaluation with the [[dom/methods/clearTimeout|'''clearTimeout''']] method.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example uses the '''setTimeout''' method to evaluate a simple expression after one second has elapsed.
|LiveURL=
|Code=
window.setTimeout("alert('Hello, world')", 1000);
}}
{{Single_Example
|Description=The following example uses the '''setTimeout''' method to evaluate a slightly more complex expression after one second has elapsed.
|LiveURL=
|Code=
var sMsg {{=}} "Hello, world";
window.setTimeout("alert(" + sMsg + ")", 1000);
}}
{{Single_Example
|Description=This example uses the '''setTimeout''' method to hide a '''input type{{=}}button''' object after three seconds. If the user clicks the '''Count Down''' button and then counts to three, the '''Now You See Me''' button disappears.
|LiveURL=
|Code=
&lt;script type{{=}}"text/javascript"&gt;
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
}}
{{Single_Example
|Description=This example uses a function pointer to pass the data. In this case, the data is stored in a global variable because it cannot be passed directly. In the preceding example, the [[html/attributes/id|'''ID''']] of the button is passed as a parameter to the function invoked by the '''setTimeout''' method. This is possible only when a string is passed as the first argument.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setTimeout.htm
|Code=
&lt;script type{{=}}"text/javascript"&gt;
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
}}}}
{{Notes_Section
|Notes=
===Remarks===
The specified expression or function is evaluated once. For repeated evaluation, use the [[dom/methods/setInterval|'''setInterval''']] method.
When you use the '''setTimeout''' method with Introduction to DHTML Behaviors, the value of ''expression'' should be a function pointer to call a function within the HTML Component (HTC) file or a string to call a function in the primary document.

'''Note'''  In Windows Internet Explorer, you cannot pass arguments to the callback function directly; however, you can simulate passing arguments by creating an anonymous closure function that references variables within scope of the call to [[dom/methods/setInterval|'''setInterval''']] or '''setTimeout'''. For more information, see [[dom/methods/setInterval|'''setInterval''']].
In versions earlier than Microsoft Internet Explorer 5, the first argument of '''setTimeout''' must be a string. Evaluation of the string is deferred until the specified interval elapses.
As of Internet Explorer 5, the first argument of '''setTimeout''' can be a string or a function pointer.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>window</code>
*<code>[[dom/methods/clearTimeout|clearTimeout]]</code>
*<code>[[apis/timing/methods/requestAnimationFrame|requestAnimationFrame]]</code>
*<code>[[apis/timing/methods/setImmediate|setImmediate]]</code>
*<code>[[dom/methods/setInterval|setInterval]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}