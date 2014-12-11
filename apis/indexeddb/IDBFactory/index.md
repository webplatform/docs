{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Proposed Recommendation}}
{{API_Name}}
{{Summary_Section|The object type for the [[apis/indexeddb/indexedDB|indexedDB]] property, which provides access to the IndexedDB features supported by the browser and/or device.}}
{{API_Object
|Subclass_of=
|Overview=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example uses feature detection to determine whether IndexedDB is supported by the current browser/device.
|Code=function getIndexedDBHandle() {
   var oResult = null; 
   if ( window.indexedDB ) {
      oResult = window.indexedDB;
   } else if ( window.mozIndexedDB ) { 
      oResult = window.mozIndexedDB;
   } else if ( window.webkitIndexedDB ) {
      oResult = window.webkitIndexedDB;
   }
   return oResult;
}

var ixHandle = getIndexedDBHandle();
if ( getIndexHandle == null ) {
   doFallback();
} else {
   doIndexedDBWork(};
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
Use the [[apis/indexeddb/indexedDB|'''indexedDB''']] property to access IndexedDB databases.

'''Important'''  For security reasons, Internet Explorer support for the '''indexedDB''' property is limited to webpages loaded using the "http://" or "https://" protocols.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C IndexedDB Specification
|URL=http://www.w3.org/TR/IndexedDB/
|Status=W3C Proposed Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=*[http://msdn.microsoft.com/en-us/library/jj154908.aspx How to create a tag cloud using IndexedDB]
|Manual_sections=
}}
{{Topics|API, IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
}








{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=IDBFactory
|Chrome_supported=Yes
|Chrome_version=24
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=22
|Firefox_supported=Yes
|Firefox_version=16
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=15
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row}}
}}}