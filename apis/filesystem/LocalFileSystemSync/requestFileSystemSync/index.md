{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Requests a file system where data should be stored. You access a sandboxed file system by requesting a LocalFileSystemSync object from within a web worker using this global method, window.requestFileSystemSync().}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=type
|Data type=unsigned short
|Description=The storage type of the file system. The value can be either TEMPORARY (0) or PERSISTENT (1).
|Optional=No
}}{{Method Parameter
|Name=size
|Data type=unsigned long
|Description=The storage space in bytes that you need for your app.
|Optional=No
}}
|Method_applies_to=apis/filesystem/LocalFileSystemSync
|Example_object_name=LocalFileSystemSync
|Javascript_data_type=Object
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