{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=Bookmark|Data type=BSTR|Description='''String''' that specifies the bookmark to move to.|Optional=}}
|Method_applies_to=dom/traversal/TextRange
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Boolean

'''Boolean''' that returns one of the following possible values:

{| class="wikitable"
|-
!Return value
!Description
|-
|true
|Successfully moved to the bookmark.
|-
|false
|Move to the bookmark failed.
|}
 


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
Bookmarks are opaque strings created with the [[dom/traversal/methods/getBookmark|'''getBookmark''']] method.
This feature might not be available on non-Microsoft Win32 platforms.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/traversal/TextRange|TextRange]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}