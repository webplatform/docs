{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=Selector
|Data type=String
|Description='''String''' that specifies the selector for the new rule. Single contextual selectors are valid. For example, "'''div''' '''p''' '''b'''" is a valid contextual selector.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=Style
|Data type=String
|Description='''String''' that specifies the style assignments for this style rule. This style takes the same form as an inline style specification. For example, "<code>color:blue</code>" is a valid style parameter.
|Optional=No
}}{{Method Parameter
|Index=2
|Name=Index
|Data type=Number
|Description='''Integer''' that specifies the zero-based position in the '''rules''' collection where the new style rule should be placed. Default is '''-1''', which specifies that the rule is added to the end of the collection.
|Optional=No
}}
|Method_applies_to=css/cssom/methods
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=
|Return_value_description=Reserved.  
Always returns -1.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''addRule''' method to add a rule that sets all bold text appearing in a DIV to the color blue.
|Code=&lt;STYLE&gt;
&lt;/STYLE&gt;
&lt;DIV&gt;
Internet Explorer makes &lt;B&gt;HTML&lt;/B&gt; dynamic.
&lt;/DIV&gt;
&lt;SCRIPT&gt;
   var new_rule;
   new_rule {{=}} document.styleSheets[0].addRule("DIV B", "color:blue", 0);
&lt;/SCRIPT&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
You can add up to 4095 style rules with the '''addRule''' method. After that, the method returns an "Invalid Argument" exception.
You can apply rules to a disabled [[css/cssom/styleSheet|'''styleSheet''']], but they do not apply to the document until you enable the '''styleSheet'''.
|Import_Notes=
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
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>IHTMLStyleSheet</code>
*<code>[[css/cssom/styleSheet|styleSheet]]</code>
*<code>Reference</code>
*<code>[[css/cssom/methods/removeRule|removeRule]]</code>
*<code>[[css/cssom/rules|rules]]</code>
*<code>[[css/cssom/styleSheets|styleSheets]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}