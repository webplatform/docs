{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
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
|This exception is thrown if the status of the cache is invalid.
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
|This exception is thrown if the status of the cache is invalid.
|}
 
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
In order to swap an old cache out for a new one, call [[apis/appcache/methods/update|'''update''']] first. When the status is in the '''UPDATEREADY''' state, calling '''swapCache''' will make the swap.
Calling '''swapCache''' will not update any content on your page.  It will simply allow your webpage to be able to access any further dynamic content from the new cache instead of the old one.  After the page is refreshed, the newly created cache will be used for all in-page and dynamic requests.
The '''swapCache''' method is provided for convenience but is not necessary for basic functionality. Loading or refreshing the page is sufficient. For example, refreshing the page after an '''UpdateReady''' event will reload the page from the new cache without a call to '''swapCache'''.
'''swapCache''' does not cause previously-loaded resources to be reloaded; for example, images do not suddenly get reloaded, and style sheets and scripts do not get reparsed or reevaluated. The only change is that subsequent requests for cached resources will obtain the newer copies.
|Import_Notes====Syntax===
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
*<code>[[apis/appcache/ApplicationCache|ApplicationCache]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}