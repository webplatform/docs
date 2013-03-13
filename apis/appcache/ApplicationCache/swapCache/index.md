{{Page_Title}}
{{Flags
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Switches to the most recent application cache, if there is a newer one. If there isn't, throws an '''InvalidStateError''' exception.

This does not cause previously-loaded resources to be reloaded; for example, images do not suddenly get reloaded and style sheets and scripts do not get reparsed or reevaluated. The only change is that subsequent requests for cached resources will obtain the newer copies.

The '''updateready''' event will fire before this method can be called. Once it fires, the Web application can, at its leisure, call this method to switch the underlying cache to the one with the more recent updates. To make proper use of this, applications have to be able to bring the new features into play; for example, reloading scripts to enable new features. An easier alternative to <code>swapCache()</code> is just to reload the entire page at a time suitable for the user, using <code>location.reload()</code>.
}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/appcache/ApplicationCache
|Example_object_name=window.applicationCache
|Javascript_data_type=void
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
{{!}}This exception is thrown if the status of the cache is invalid.
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=// Attempt to update the user's cache.
window.applicationCache.update(); 

…

if (window.applicationCache.status === window.applicationCache.UPDATEREADY) {
  // The fetch was successful, swap in the new cache.
  window.applicationCache.swapCache();
}
}}
}}
{{Notes_Section
|Usage=In order to swap an old cache out for a new one, call [[apis/appcache/methods/update|update]] first. When the status is in the '''UPDATEREADY''' state, calling '''swapCache''' will make the swap.

Calling '''swapCache''' will not update any content on your page.  It will simply allow your webpage to be able to access any further dynamic content from the new cache instead of the old one.  After the page is refreshed, the newly created cache will be used for all in-page and dynamic requests.
The '''swapCache''' method is provided for convenience but is not necessary for basic functionality. Loading or refreshing the page is sufficient. For example, refreshing the page after an '''UpdateReady''' event will reload the page from the new cache without a call to '''swapCache'''.

'''swapCache''' does not cause previously-loaded resources to be reloaded; for example, images do not suddenly get reloaded, and style sheets and scripts do not get reparsed or reevaluated. The only change is that subsequent requests for cached resources will obtain the newer copies.
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
|Sources=MSDN, HTML5Rocks
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/appcache/beginner/
}}