{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Allows the user to look up the Entry for a file or directory referred to by a local URL.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=url
|Data type=String
|Description=A URL referring to a local file in a filesystem accessable via this API.
|Optional=No
}}{{Method Parameter
|Name=successCallback
|Data type=String
|Description=A callback that is called to report the Entry to which the supplied URL refers.
|Optional=No
}}{{Method Parameter
|Name=errorCallback
|Data type=String
|Description=A callback that is called when errors happen, or when the request to obtain the Entry is denied.
|Optional=Yes
}}
|Method_applies_to=apis/filesystem/LocalFileSystem
|Example_object_name=LocalFileSystem
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=Yes
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
|Desktop_rows=
|Mobile_rows=
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