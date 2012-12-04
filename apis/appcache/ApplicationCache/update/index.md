{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Invokes the application cache download process. Throws an InvalidStateError exception if there is no application cache to update. Calling this method is not usually necessary, as user agents will generally take care of updating application caches automatically. The method can be useful in situations such as long-lived applications. For example, a Web mail application might stay open in a browser tab for weeks at a time. Such an application could want to test for updates each day.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/appcache/ApplicationCache
|Example_object_name=ApplicationCache
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{{{!}} class="wikitable"
{{!}}-
!Return code/value
!Description
{{!}}-
{{!}}S_OK
{{!}}
{{!}}-
{{!}}DOMException.INVALID_STATE_ERR
11
{{!}}This exception is thrown if the application cache cannot be found or the status of the cache is obsolete.
{{!}}}
 

Type: '''HRESULT'''

This method can return one of these values.

{{{!}} class="wikitable"
{{!}}-
!Return code/value
!Description
{{!}}-
{{!}}S_OK
{{!}}
{{!}}-
{{!}}DOMException.INVALID_STATE_ERR
11
{{!}}This exception is thrown if the application cache cannot be found or the status of the cache is obsolete.
{{!}}}

}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=Use this method and check the [[apis/appcache/properties/status|status]] before using [[apis/appcache/methods/swapCache|swapCache]].
The '''update''' method returns before the update check is complete, so it is a best practice to wait before checking the [[apis/appcache/properties/status|status]] property or calling the [[apis/appcache/methods/swapCache|swapCache]] method.
The '''update'''  method is provided for convenience, but is not necessary for basic functionality. Loading or refreshing the page is sufficient.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C ApplicationCache Specification
|URL=http://dev.w3.org/html5/spec/single-page.html#application-cache-api
|Status=W3C Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Offline web applications
|Chrome_supported=Yes
|Chrome_version=22.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=15.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=Offline web applications
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}