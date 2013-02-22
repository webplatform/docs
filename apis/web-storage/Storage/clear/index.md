{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Causes the list associated with the object to be emptied of all key/value pairs, if there are any.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/web-storage/Storage
|Example_object_name=object
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following button clears the local storage area for the current domain.
|Code=&lt;button onclick{{=}}"localStorage.clear()"&gt;
    Clear Stored Values&lt;/button&gt;
}}
}}
{{Notes_Section
|Notes=sessionStorage is cleared immediately. localStorage key/value pairs are removed from memory, and disk storage quota is updated.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Web Storage Specification
|URL=http://dev.w3.org/html5/webstorage
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
{{See_Also_Section}}
{{Topics|Webstorage}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}