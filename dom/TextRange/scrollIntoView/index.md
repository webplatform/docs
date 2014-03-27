{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=varargStart
|Data type=VARIANT
|Description='''Variant''' of type '''Boolean''' that specifies one of the following values:
|Optional=No
}}
|Method_applies_to=dom/TextRange
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
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
|Notes====Remarks===
The '''scrollIntoView''' method is useful for immediately showing the user the result of some action without requiring the user to manually scroll through the document to find the result.
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}