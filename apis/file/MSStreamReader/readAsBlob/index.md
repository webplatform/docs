{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=stream|Data type=MSStream|Description=Object that holds the [[apis/file/MSStream|'''MSStream''']] object to read.|Optional=}}
{{Method Parameter|Name=size|Data type=signed long long|Description=String that specifies the  maximum size of the  object to read.|Optional=}}
|Method_applies_to=dom/Element
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=[[apis/file/Blob|'''Blob''']]

The [[apis/file/Blob|'''Blob''']] that was created from the specified stream.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The '''readAsBlob''' method is used by [[apis/file/MSStreamReader|'''msStreamReader''']] to create a [[apis/file/Blob|'''Blob''']] object from an [[apis/file/MSStream|'''MSStream''']]. When the read begins, the [[apis/file/properties/readyState|'''readyState''']] property is set to the <code>LOADING</code> state on '''MSStreamReader''' and the [[apis/file/events/onloadstart|'''onloadstart''']] event is fired. Progress for the read is monitored by the [[apis/file/events/onprogress|'''onprogress''']] event. When the read completes, the [[apis/file/events/onloadend|'''onloadend''']] event fires and '''readyState''' is set to <code>DONE</code> and '''MSStreamReader'''.[[apis/file/properties/result|'''result''']] returns the new '''Blob''' object.
A read operation can be interrupted if an error occurs or the [[apis/file/methods/abort|'''abort''']] method is run. If an error occurs, the [[apis/file/events/onloadend|'''onloadend''']]event, sets the [[apis/file/properties/readyState|'''readyState''']] to <code>DONE</code>, and passes the error using the [[apis/file/properties/error|'''error''']] property.
For a code example, see [[apis/file/MSStreamReader|'''MSStreamReader''']].
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/file/MSStreamReader|msStreamReader]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}