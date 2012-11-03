{{Page_Title|IndexedDB reference}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Needed, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|IndexedDB is an API for client-side storage of significant amounts of structured data and for high performance searches on this data using indexes}}
{{API_Listing
|Query=indexeddb
|Use_page_title=No
|List_all_subpages=Yes
}}
{{Notes_Section
|Usage=indexedDB = window.indexedDB;
|Notes=IndexedDB provides separate APIs for synchronous and asynchronous access. The synchronous API is intended to be used only inside of Web Workers but it isn't implemented by any browser yet. The asynchronous API works both within and without Web Workers.
}}
{{See_Also_Section
|External_links=* [http://www.w3.org/TR/IndexedDB/ W3C IndexedDB Specification]
|Manual_sections=====Storage Limits====

There isn't any limit on an single item size. There may be limits on each IndexedDB database. The constraints and UI on limits may vary:

*For Firefox there is no limit on the IndexedDB database's size, Firefox will just ask the user for permission for blobs bigger than 50 MB. [http://support.mozilla.org/en-US/questions/818987 Reference]
*For Google Chrome, see the [https://developers.google.com/chrome/whitepapers/storage#temporary reference on temporary storage]

}}
{{Topics|IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/IndexedDB
|MSDN_link=
|HTML5Rocks_link=
}}
[[Category:API_Listings]]