{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name|close}}
{{Summary_Section|Closes an output stream and forces the sent data to display.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/document
|Example_object_name=document
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes={{TODO|The method name should be '''close''' and not '''close (document)'''.}}
{{TODO|Clarify this weird note.}}
When a function fired by an event on any object calls the 
[[dom/methods/close|'''close''']] method, the window.'''close''' method is implied.
When an event on any 
object calls the [[dom/methods/close|'''close''']] method, the 
document.'''close''' method is implied.


When [[dom/document|'''document''']].[[dom/methods/write|'''write''']] or '''document'''.[[dom/methods/writeln|'''writeln''']] is used in an event handler, '''document'''.'''close''' should also be used.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 HTML
|URL=http://www.w3org/TR/DOM-Level-2-HTML/
|Status=Recommendation
|Relevant_changes=Section 1.5
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>[[dom/methods/open (document)|open]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}