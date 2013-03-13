{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Invokes the application cache download process. Throws an InvalidStateError exception if there is no application cache to update. Calling this method is not usually necessary, as user agents will generally take care of updating application caches automatically. The method can be useful in situations such as long-lived applications. For example, a Web mail application might stay open in a browser tab for weeks at a time. Such an application could want to test for updates each day.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/appcache/ApplicationCache
|Example_object_name=window.applicationCache
|Javascript_data_type=null
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
}}
{{Examples_Section
|Not_required=No
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
|Imported_tables={{Imported Compatibility Table
|Page=apis/appcache/ApplicationCache
}}
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Appcache, API}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx
|HTML5Rocks_link=
}}