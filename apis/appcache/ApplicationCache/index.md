{{Page_Title|ApplicationCache}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The '''Application Cache''' (AppCache) lets web-based applications run offline. Developers can  specify resources that the browser should cache and make available to offline users. They load and work correctly even if users click the refresh button when they are offline.

Using an application cache gives an application the following benefits:

* Offline browsing: users can navigate a site even when they are offline.
* Speed: cached resources are local, and therefore load faster.
* Reduced server load: the browser only downloads resources that have changed from the server.
}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=In order to cache files, you must do the following:
* Create a manifest file that lists the files and other web resources you want to cache.
* Reference the manifest file in the header of every page you want cached.

=== The manifest file ===
The manifest file  defines which web resources are cached when a user browses to your site. The manifest file typically has the extension '''.appcache''' or '''.manifest'''. Each webpage must add a manifest attribute to the HTML element similar to this:

<pre><html manifest="example.appcache"></pre>

You can use an absolute or relative URL. The cache manifest file lists the files that will be cached, using the format:

<pre>CACHE MANIFEST
# Version 1

CACHE:
script/scriptfilename1.js
css/cssfilename.css
images/imagename1.png
images/imagename2.jpg
images/imagename3.png

FALLBACK:
# This will enable imagename4.png to be as a replacement for 
# all resources under the images dir when there is no network connectivity.
images/ images/imagename4.png

NETWORK:
# This will prevent other network resources from being accessed.
images/imagename5.png
</pre>

The first line of the manifest must read CACHE MANIFEST and the lines that follow it list the web resources you want to cache. You can use the # symbol to make comments.

Alternatively, web resources that need to be cached can be specified by adding a “CACHE:” header section before the resources (as shown previously).
In addition, fallback resources can be defined to replace general or specific web resources when there is no network connectivity. This is done by adding a “FALLBACK:” header section before the resources.  These resources can be wildcard to specify a catch all mechanism (as shown previously). Be aware  that there is a space after the first "images/" in the FALLBACK: section. This indicates that any files contained under the "images/" directory will fall back to a specific web resource (for example, images/imagename4.png) if they cannot be accessed from the network.
Also, web resources can be specified to only be loaded from the network. This is done by adding a "NETWORK: " header section before the resources.  This functionality can be used to scope down the number of resources that can be accessed from the network, thus, creating an allowed only list (as shown previously).

{{{!}}
! Section
! Description
{{!}}-
{{!}} CACHE
{{!}} This is the default section for entries. Files listed under this header (or immediately after the CACHE MANIFEST) will be explicitly cached after they're downloaded for the first time.
{{!}}-
{{!}} NETWORK
{{!}} Files listed under this section are white-listed resources that require a connection to the server. All requests to these resources bypass the cache, even if the user is offline. Wildcards may be used.
{{!}}-
{{!}} FALLBACK
{{!}} An optional section specifying fallback pages if a resource is inaccessible. The first URI is the resource, the second is the fallback. Both URIs must be relative and from the same origin as the manifest file. Wildcards may be used.
{{!}}}

'''ApplicationCache''' functionality is independent of HTTP caching headers.
The manifest file implicitly includes itself as a page to be cached. It also needs to have the same domain of origin as the page that contains it.
|Notes==== Limitations ===
A browser can not allocate unlimited disk space for ressources that should be cached. Especially when it comes down to cashing big media files like videos, you should check if the users Browser is able to store that file. There are differences in the browser implementations, as shown below: 

{{{!}}
! Browser
! Max. space per item
! max. space per page
{{!}}-
{{!}} Chrome
{{!}} 32Mb
{{!}} 260Mb
{{!}}}
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
|Chrome_version=4.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.5
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.6
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=4.0
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
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=18.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=11.0
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
{{See_Also_Section
|External_links=*[http://alistapart.com/article/application-cache-is-a-douchebag Application Cache is a Douchebag]
*[http://www.html5rocks.com/en/tutorials/appcache/beginner/ HTML5Rocks - A Beginner's Guide to Using the Application Cache]
*[http://appcachefacts.info/ appcachefacts.info]
*[http://manifest-validator.com Cache Manifest Validator]
}}
{{Topics|Appcache, Connectivity, DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/HTML/Using_the_application_cache
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx
|HTML5Rocks_link=
}}