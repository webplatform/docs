{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=expression|Data type=VARIANT|Description='''Variant''' that specifies a function pointer or string that indicates the code to be executed when the specified interval has elapsed.|Optional=}}
{{Method Parameter|Name=msec|Data type=Integer|Description='''Integer''' that specifies the number of milliseconds.|Optional=}}
{{Method Parameter|Name=language|Data type=VARIANT|Description='''String''' that specifies any one of the possible values for the [[html/attributes/language|'''LANGUAGE''']] attribute.|Optional=}}
|Method_applies_to=dom/window
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''Integer'''

Integer. Returns an identifier that cancels the timer with the [[dom/methods/clearInterval|'''clearInterval''']] method.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''setInterval''' method to create a DHTML clock. A variable is assigned to the interval, and can be used as a reference to stop the interval by using the [[dom/methods/clearInterval|'''clearInterval''']] method.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setInterval.htm
|Code=
var oInterval {{=}} "";
function fnStartClock(){
   oInterval {{=}} setInterval(fnDoClock,200);
}
function fnDoClock(){
   // Code to display hours, minutes, and seconds.
}
window.onload {{=}} fnStartClock; 
}}
{{Single_Example
|Description=The next example demonstrates how to pass arguments to a function with [[dom/methods/setTimeout|'''setTimeout''']] or '''setInterval'''. To do this, create an inner anonymous function to wrap the real callback function. In the new function scope, you can refer to variables declared prior to the call to '''setTimeout''' (such as <code>div</code>). This structure is referred to as a "closure" in JScript
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setInterval2.htm
|Code=
// The first example of a closure passes the variable to a named function.
function startTimer() {
    var div {{=}} document.getElementById('currentTime');
    setTimeout(function(){doClock(div)},200);
}
// The second example also uses a closure, by referring to an argument passed to the function.
function doClock(obj) {
    setInterval(function(){obj.innerHTML{{=}}(new Date()).toLocaleString()},200);
} 
}}
{{Single_Example
|Description=This example demonstrates that more than one closure can refer to the same variable. Here, the callback function that displays the value of <code>count</code> is called at a different interval than the function that updates its value.
|LiveURL=
|Code=
function startCounter() {
    var div {{=}} document.getElementById('counter');
    var count {{=}} 0;
    setInterval(function(){count++},143);
    setInterval(function(){div.innerHTML{{=}}count},667);
} 
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''setInterval''' method continuously evaluates the specified expression until the timer is removed with the [[dom/methods/clearInterval|'''clearInterval''']] method.
To pass a function as a string, be sure to append the function name with parentheses.
 <code>window.setInterval("someFunction()", 5000);</code>
When passing a function pointer, do not include the parentheses.
 <code>window.setInterval(someFunction, 5000);</code>
When you use the '''setInterval''' method with Introduction to DHTML Behaviors, the value of ''expression'' should be a function pointer to call a function within the HTML Component (HTC) file or a string to call a function in the primary document.

'''Note'''  In Windows Internet Explorer, you cannot pass arguments to the callback function directly; however, you can simulate passing arguments by creating an anonymous closure function that references variables within scope of the call to '''setInterval''' or [[dom/methods/setTimeout|'''setTimeout''']]. For more information, see Examples.
In versions earlier than Microsoft Internet Explorer 5, the first argument of '''setInterval''' must be a string. Evaluation of the string is deferred until the specified interval elapses.
As of Internet Explorer 5, the first argument of '''setInterval''' can be passed as a string or as a function pointer.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>window</code>
*<code>Reference</code>
*<code>[[dom/methods/clearInterval|clearInterval]]</code>
*<code>[[apis/timing/methods/requestAnimationFrame|requestAnimationFrame]]</code>
*<code>[[dom/methods/setTimeout|setTimeout]]</code>
*<code>[[apis/timing/methods/setImmediate|setImmediate]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}