{{Page_Title|ApplicationCache}}
{{Flags}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
In order to cache files, you must do the following:
*Create a manifest file that lists the files and other web resources you want to cache.
*Reference the manifest file in the header of every page you want cached.

The manifest file  defines which web resources are cached when a user browses to your site. The manifest file typically has the extension '''.appcache''' and must be served as a  '''text/cache-manifest''' mime type. Each webpage must add a manifest attribute to the HTML element similar to this:
 <code>&lt;html manifest{{=}}"clock.appcache"&gt;</code>
You can use an absolute or relative URL. The cache manifest file lists the files that will be cached, using the format:
 <code>CACHE MANIFEST
 #Version 1
 
 CACHE:
 script/scriptfilename1.js
 css/cssfilename.css
 images/imagename1.png
 images/imagename2.jpg
 images/imagename3.png
 
 FALLBACK:
 #This will enable imagename4.png to be as a replacement for 
 #all resources under the images dir when there is no network connectivity.
 images/ images/imagename4.png
 
 NETWORK:
 #This will prevent other network resources from being accessed.
 images/imagename5.png
 
 </code>
The first line of the manifest must read CACHE MANIFEST and the lines that follow it list the web resources you want to cache. You can use the # symbol to make comments.
Alternatively, web resources that need to be cached can be specified by adding a “CACHE:” header section before the resources (as shown previously).
In addition, fallback resources can be defined to replace general or specific web resources when there is no network connectivity.  This is done by adding a “FALLBACK:” header section before the resources.  These resources can be wildcard to specify a catch all mechanism (as shown previously). Be aware  that there is a space after the first "images/" in the FALLBACK: section. This indicates that any files contained under the "images/" directory will fall back to a specific web resource (for example, images/imagename4.png) if they cannot be accessed from the network.
Also, web resources can be specified to only be loaded from the network. This is done by adding a "NETWORK: " header section before the resources.  This functionality can be used to scope down the number of resources that can be accessed from the network, thus, creating an allowed only list (as shown previously).
The '''ApplicationCache''' object has the following properties:
*[[apis/appcache/properties/applicationCache|'''applicationCache''']]
*[[apis/appcache/properties/status|'''status''']]

The '''ApplicationCache''' object supports the following events:
*[[apis/appcache/properties/oncached|'''oncached''']]
*[[apis/appcache/properties/onchecking|'''onchecking''']]
*[[apis/appcache/properties/ondownloading|'''ondownloading''']]
*[[apis/appcache/properties/onerror|'''onerror''']]
*[[apis/appcache/properties/onnoupdate|'''onnoupdate''']]
*[[apis/appcache/properties/onobsolete|'''onobsolete''']]
*[[apis/appcache/properties/onprogress|'''onprogress''']]
*[[apis/appcache/properties/onupdateready|'''onupdateready''']]

The ApplicationCache object has the following methods:
*[[apis/appcache/methods/swapCache|'''swapCache''']]
*[[apis/appcache/methods/update|'''update''']]

'''ApplicationCache'''  functionality is independent of HTTP caching headers.
The manifest file implicitly includes itself as a page to be cached. It also needs to have the same domain of origin as the page that contains it.
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_appcache\ie]:%20ApplicationCache object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
|Import_Notes====Syntax===
===Members===
The '''ApplicationCache''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''ApplicationCache''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/appcache/methods/swapCache|'''swapCache''']]
|Swaps an old cache for a newer one.
|-
|[[apis/appcache/methods/update|'''update''']]
|Triggers the update of the existing cache.  If no updates are available, an update will not be forced.
|}
 

====Properties====
The '''ApplicationCache''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/appcache/properties/oncached|'''oncached''']]
|Event handler provided to see if the resources have been loaded into the cache.
|-
|[[apis/appcache/properties/onchecking|'''onchecking''']]
|Event handler provided to see if the browser is in the process of checking for an update, or is attempting to download the manifest for the first time.
|-
|[[apis/appcache/properties/ondownloading|'''ondownloading''']]
|Event handler provided to determine if the browser has found an update and is downloading it, or is downloading the resources for the first time.
|-
|[[apis/appcache/properties/onerror|'''onerror''']]
|Event handler provided if an error has taken place.
|-
|[[apis/appcache/properties/onnoupdate|'''onnoupdate''']]
|Event handler provided to indicate that the manifest has not changed.
|-
|[[apis/appcache/properties/onobsolete|'''onobsolete''']]
|Event handler provided to indicate that the application cache cannot be found.
|-
|[[apis/appcache/properties/onprogress|'''onprogress''']]
|Event handler provided to indicate that the resources for the cache are still being downloaded.
|-
|[[apis/appcache/properties/onupdateready|'''onupdateready''']]
|Event handler provided to indicate that previously cached resources have been updated.
|-
|[[apis/appcache/properties/status|'''status''']]
|Indicates the current status of the cache.
|}
 
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}