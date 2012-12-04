{{Page_Title|ApplicationCache}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Tells a browser to cache any downloaded resource (HTML, CSS, JS, images, etc…) for set amount of time. The possible benefits are faster page loads and offline viewing.}}
{{API_Object}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=In order to cache files, you must do the following:
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

'''ApplicationCache'''  functionality is independent of HTTP caching headers.
The manifest file implicitly includes itself as a page to be cached. It also needs to have the same domain of origin as the page that contains it.

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
{{Topics|Connectivity, DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}