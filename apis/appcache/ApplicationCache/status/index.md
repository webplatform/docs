{{Page_Title}}
{{Flags
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns the current status of the application cache, as given by the constants defined below.}}
{{API_Object_Property
|Property_applies_to=apis/appcache/ApplicationCache
|Read_only=Yes
|Example_object_name=ApplicationCache
|Javascript_data_type=unsigned short
|Return_value_description=;'''UNCACHED''' (numeric value 0)
: The current webpage doesn't use an application cache at this time.

;'''IDLE''' (numeric value 1)
: The current webpage's application cache is the newest available, it's content is not being updated or marked as obsolete.

;'''CHECKING''' (numeric value 2)
: The current webpage's application cache is checking for an update.

;'''DOWNLOADING''' (numeric value 3)
: An update for the cached resources was found and is now being downloaded.

;'''UPDATEREADY''' (numeric value 4)
: The updated ressources have been newly redownloaded.

;'''OBSOLETE''' (numeric value 5)
: The current webpage's application cache is marked as obsolete.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var appCache = window.applicationCache;

switch (appCache.status) {
  case appCache.UNCACHED: // UNCACHED == 0
    return 'UNCACHED';
    break;
  case appCache.IDLE: // IDLE == 1
    return 'IDLE';
    break;
  case appCache.CHECKING: // CHECKING == 2
    return 'CHECKING';
    break;
  case appCache.DOWNLOADING: // DOWNLOADING == 3
    return 'DOWNLOADING';
    break;
  case appCache.UPDATEREADY:  // UPDATEREADY == 4
    return 'UPDATEREADY';
    break;
  case appCache.OBSOLETE: // OBSOLETE == 5
    return 'OBSOLETE';
    break;
  default:
    return 'UKNOWN CACHE STATUS';
    break;
};
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C ApplicationCache Specification
|URL=http://dev.w3.org/html5/spec/single-page.html#dom-appcache-status
|Status=W3C Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Off-line Storage
}}
{{Topics|Appcache, API}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN, HTML5Rocks
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/appcache/beginner/
}}