{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|HTML}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=In the following two examples, the value of '''scheme''' defines how to interpret the value of the "date" property.
|LiveURL=<pre xml:space{{=}}"preserve"><code>
//Here scheme{{=}}"USA" implies "MM-DD-YYYY"
&lt;META scheme{{=}}"USA" name{{=}}"date" content{{=}}"04-05-1962"&gt;</code></pre>
|Code=

//Here scheme{{=}}"Europe" implies "DD-MM-YYYY"
&lt;META scheme{{=}}"Europe" name{{=}}"date" content{{=}}"05-04-1962"&gt;
}}
{{Single_Example
|Description=The following example of the '''meta''' shows how the '''scheme''' can be used to clarify the value of the "id" property.
|LiveURL=
|Code=
&lt;META scheme{{=}}"customer" name{{=}}"id" content{{=}}"Fancy Pants"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''scheme''' was introduced in Microsoft Internet Explorer 6
The '''scheme''' property can provide a context to correctly interpret otherwise ambiguous data formats such as those for date and time.  It can also be used to identify the object's content itself.
There is no functionality implemented for this property unless defined by the author.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>meta</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}