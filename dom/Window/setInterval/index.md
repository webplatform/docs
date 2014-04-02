{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=expression
|Data type=String
|Description='''Variant''' that specifies a function pointer or string indicating the code to be executed when the specified interval has elapsed.

Passing a string as a parameter suffers the same hazards as [[tutorials/JavaScript_gotchas/Why_eval()_is_evil|eval()]], so it is generally recommended to pass a function pointer instead.
|Optional=No
}}{{Method Parameter
|Name=msec
|Data type=String
|Description='''Integer''' that specifies the number of milliseconds.

Note that there may be a minimum interval for this function. See [[dom/Window/setTimeout|setTimeout]].
|Optional=No
}}{{Method Parameter
|Name=language
|Data type=String
|Description='''String''' that specifies any one of the possible values for the [[html/attributes/language|'''LANGUAGE''']] attribute.
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''Integer'''

Integer. Returns an identifier that cancels the timer with the [[dom/Window/clearInterval|'''clearInterval''']] method.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''setInterval''' method to create a DHTML clock. A variable is assigned to the interval, and can be used as a reference to stop the interval by using the [[dom/Window/clearInterval|'''clearInterval''']] method.
|Code=var oInterval {{=}} "";
function fnStartClock(){
   oInterval {{=}} setInterval(fnDoClock,200);
}
function fnDoClock(){
   // Code to display hours, minutes, and seconds.
}
window.onload {{=}} fnStartClock;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setInterval.htm
}}{{Single Example
|Description=The next example demonstrates how to pass arguments to a function with [[dom/Window/setTimeout|'''setTimeout''']] or '''setInterval'''. To do this, create an inner anonymous function to wrap the real callback function. In the new function scope, you can refer to variables declared prior to the call to '''setTimeout''' (such as <code>div</code>). This structure is referred to as a "closure" in JScript
|Code=// The first example of a closure passes the variable to a named function.
function startTimer() {
    var div {{=}} document.getElementById('currentTime');
    setTimeout(function(){doClock(div)},200);
}
// The second example also uses a closure, by referring to an argument passed to the function.
function doClock(obj) {
    setInterval(function(){obj.innerHTML{{=}}(new Date()).toLocaleString()},200);
}
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setInterval2.htm
}}{{Single Example
|Description=This example demonstrates that more than one closure can refer to the same variable. Here, the callback function that displays the value of <code>count</code> is called at a different interval than the function that updates its value.
|Code=function startCounter() {
    var div {{=}} document.getElementById('counter');
    var count {{=}} 0;
    setInterval(function(){count++},143);
    setInterval(function(){div.innerHTML{{=}}count},667);
}
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''setInterval''' method continuously evaluates the specified expression until the timer is removed with the [[dom/Window/clearInterval|'''clearInterval''']] method.
To pass a function as a string, be sure to append the function name with parentheses.
 <code>window.setInterval("someFunction()", 5000);</code>
When passing a function pointer, do not include the parentheses.
 <code>window.setInterval(someFunction, 5000);</code>
When you use the '''setInterval''' method with Introduction to DHTML Behaviors, the value of ''expression'' should be a function pointer to call a function within the HTML Component (HTC) file or a string to call a function in the primary document.

'''Note'''  In Windows Internet Explorer, you cannot pass arguments to the callback function directly; however, you can simulate passing arguments by creating an anonymous closure function that references variables within scope of the call to '''setInterval''' or [[dom/Window/setTimeout|'''setTimeout''']]. For more information, see Examples.
In versions earlier than Microsoft Internet Explorer 5, the first argument of '''setInterval''' must be a string. Evaluation of the string is deferred until the specified interval elapses.
As of Internet Explorer 5, the first argument of '''setInterval''' can be passed as a string or as a function pointer.
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}