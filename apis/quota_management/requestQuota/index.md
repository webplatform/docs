{{Page_Title}}
{{Flags
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Requests a new quota for the requesting application.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=newQuotaInBytes
|Data type=unsigned long
|Description=The requested new quota, expressed in bytes.
|Optional=No
}}{{Method Parameter
|Name=successCallback
|Data type=String
|Description=This callback is used to return new quota information granted by a User Agent. Quota is provided by the ''grantedQuotaInBytes'' parameter.

'''void (unsigned long grantedQuotaInBytes)'''
|Optional=Yes
}}{{Method Parameter
|Name=errorCallback
|Data type=String
|Description=This callback is used to return information when an error has occured. Details are provided by the ''error'' parameter.

'''void (DOMError error)'''
|Optional=Yes
}}
|Method_applies_to=apis/quota management/StorageQuota
|Example_object_name=object
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=It is not guaranteed that the requested amount of space is granted just by calling this API. Calling this API may trigger user prompting to request explicit user permission to proceed. The successCallback callback may return a smaller amount of quota than requested.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Quota Management Specification
|URL=https://dvcs.w3.org/hg/quota/raw-file/tip/Overview.html
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
{{Topics|Quota Management}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}