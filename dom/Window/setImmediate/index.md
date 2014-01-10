{{Page_Title}}
{{Flags
|High-level issues=Deletion Candidate, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
|Editorial notes=Not part of user_timing, resource_timing, or navigation_timing interfaces.
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=handler
|Data type=any
|Description=The function to be called.
|Optional=No
}}{{Method Parameter
|Name=arguments
|Data type=any
|Description=Arguments to be passed to the function.
|Optional=No
}}{{Method Parameter
|Name=retVal
|Data type=any
|Description=A handle to the request.
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

S_OK

'''Integer'''

A handle to the request.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
JavaScript operations run in the same thread as events, display updates, and other additional tasks. As a result, extended JavaScript operations (such as functions containing many lines of code) prevent additional tasks from being handled.  In turn, this makes an application  appear to be unresponsive  because events (such as [[dom/events/click|'''onclick''']] or [[dom/events/keypress|'''onkeypress''']]) are not handled and the screen is not updated until the extended operation completes.
The '''setImmediate''' method schedules  the function specified in the '''handler''' parameter to run after the current script block completes.  If additional actions are pending when the current script block completes, they are processed before the '''handler''' function is called.   This effectively creates a ''yield'' between the current script block and the '''handler''' function.
If you break extended operations into separate functions, you can use '''setImmediate''' to call each function in sequence.  When you do this, '''setImmediate''' allows additional  tasks to complete  before calling each function in the sequence.  In turn, this enables the application to respond to user input and to handle additional tasks in a predictable and responsive fashion.

'''Note'''  
Some developers use [[dom/methods/setTimeout|'''setTimeout''']] (or [[dom/methods/setInterval|'''setInterval''']]) to create events that accomplish similar results; however, there are subtle, but important differences   between the two techniques.
The [[dom/methods/setTimeout|'''setTimeout''']] method is restricted to 250 requests per second on most systems.  This means that <code>setTimeout(0, handler)</code> waits roughly 4ms before executing, even if no additional actions are pending.  In contrast, '''setImmediate''' yields between each request, no matter how many requests are waiting to processed. If no additional actions are pending, '''setImmediate''' calls the '''handler''' function immediately.
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>window</code>
*<code>[[apis/timing/methods/clearImmediate|clearImmediate]]</code>
*<code>[[apis/timing/methods/requestAnimationFrame|requestAnimationFrame]]</code>
}}
{{Topics|API, DOM, JavaScript, Timing}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}