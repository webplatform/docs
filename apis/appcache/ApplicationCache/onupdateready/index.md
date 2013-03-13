{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The ApplicationCache object's cache host is associated with an application cache whose application cache group's update status is idle, and whose application cache group is not marked as obsolete, but that application cache is not the newest cache in its group.}}
{{API_Object_Property
|Property_applies_to=apis/appcache/ApplicationCache
|Read_only=No
|Example_object_name=window.applicationCache
|Javascript_data_type=null
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Checking fo the updateready status
|Code=// try to trigger an application cache update
window.applicationCache.update();

if (window.applicationCache.status === window.applicationCache.UPDATEREADY) {
   console.log('Cache is now ready for an update');
   // now you can call the swapCache() method to switch to the new cache
   window.applicationCache.swapCache();
}
}}{{Single Example
|Language=JavaScript
|Description=Listening for updateready events
|Code=window.applicationCache.addEventListener('updateready',function () {
  console.log('The manifest update download has been completed successfully');
}, false);
}}
}}
{{Notes_Section
|Notes=If this event indicates that the resources have been redownloaded,  the script can use [[apis/appcache/ApplicationCache/swapCache|swapCache]] to switch to the new cache.
If there is more than one event, the '''updateready''' event will be the last one in the sequence.
Alternatively, you could use an anonymous delegate function such as
 <code>object.onupdateready {{=}} function (e) { … }</code>
where e is the cached event.
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