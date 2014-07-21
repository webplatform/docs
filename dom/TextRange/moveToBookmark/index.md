{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=needs example
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=Bookmark
|Data type=BSTR
|Description='''String''' that specifies the bookmark to move to.
|Optional=No
}}
|Method_applies_to=dom/TextRange
|Example_object_name=textRange
|Return_value_name=result
|Javascript_data_type=Boolean
|Return_value_description=Boolean

'''Boolean''' that returns one of the following possible values:

{{{!}} class="wikitable"
{{!}}-
!Return value
!Description
{{!}}-
{{!}}true
{{!}}Successfully moved to the bookmark.
{{!}}-
{{!}}false
{{!}}Move to the bookmark failed.
{{!}}}
 
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Bookmarks are opaque strings created with the [[dom/TextRange/getBookmark|'''getBookmark''']] method.
This feature might not be available on non-Microsoft Win32 platforms.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536628(v=vs.85).aspx moveToBookmark Method]
|HTML5Rocks_link=
}}