{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/appcache/ApplicationCache
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code/value
!Description
|-
|S_OK
|
|-
|DOMException.INVALID_STATE_ERR
11
|This exception is thrown if the application cache cannot be found or the status of the cache is obsolete.
|}
 

Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code/value
!Description
|-
|S_OK
|
|-
|DOMException.INVALID_STATE_ERR
11
|This exception is thrown if the application cache cannot be found or the status of the cache is obsolete.
|}
 


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
Use this method and check the [[apis/appcache/properties/status|'''status''']] before using [[apis/appcache/methods/swapCache|'''swapCache''']].
The '''update''' method returns before the update check is complete, so it is a best practice to wait before checking the [[apis/appcache/properties/status|'''status''']] property or calling the [[apis/appcache/methods/swapCache|'''swapCache''']] method.
The '''update'''  method is provided for convenience, but is not necessary for basic functionality. Loading or refreshing the page is sufficient.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/appcache/ApplicationCache|ApplicationCache]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}