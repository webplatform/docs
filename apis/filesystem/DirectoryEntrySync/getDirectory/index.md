{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Creates or looks up a directory.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=path
|Data type=String
|Description=Either an absolute path or a relative path from this DirectoryEntrySync to the directory to be looked up or created. It is an error to attempt to create a directory whose immediate parent does not yet exist.
|Optional=No
}}{{Method Parameter
|Name=options
|Data type=String
|Description=*If create and exclusive are both true and the path already exists, getDirectory must fail.
*If create is true, the path doesn't exist, and no other error occurs, getDirectory must create and return a corresponding DirectoryEntry.
*If create is not true and the path doesn't exist, getDirectory must fail.
*If create is not true and the path exists, but is a file, getDirectory must fail.
*Otherwise, if no other error occurs, getDirectory must return a DirectoryEntrySync corresponding to path.
|Optional=Yes
}}
|Method_applies_to=apis/filesystem/DirectoryEntrySync
|Example_object_name=DirectoryEntrySync
|Return_value_description=DirectoryEntrySync
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C File API: Directories and System Specification
|URL=http://dev.w3.org/2009/dap/file-system/pub/FileSystem/
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Filesystem and FileWriter API
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=23.0
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=Filesystem and FileWriter API
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Yes
|Blackberry_prefixed_version=10.0
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
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|FileSystemAPI}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}