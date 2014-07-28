{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Causes the object to scroll into view, aligning it either at the top or bottom of the window. }}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=varargStart
|Data type=VARIANT
|Description='''Variant''' of type '''Boolean''' that specifies one of the following values:
|Optional=No
}}
|Method_applies_to=dom/TextRange
|Example_object_name=node
|Return_value_name=result
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example uses the '''scrollIntoView''' method to underline the content of the document's fifth paragraph and scroll it into view at the top of the window.
|Code=var coll {{=}} document.all.tags("P");
   if (coll.length &gt;{{=}} 5)
   {
      coll(4).style.textDecoration {{=}} "underline";
      coll(4).scrollIntoView(true);
   }
}}
}}
{{Notes_Section
|Usage=The '''scrollIntoView''' method is useful for immediately showing the user the result of some action without requiring the user to manually scroll through the document to find the result.
|Notes====Remarks===
Depending on the size of the given object and the current window, this method might not be able to put the item at the very top or very bottom, but will position the object as close to the requested position as possible.
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536730(v=vs.85).aspx scrollIntoView Method]
|HTML5Rocks_link=
}}