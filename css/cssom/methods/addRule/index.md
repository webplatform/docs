{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=
|Example_object_name=
|Return_value_name=
|Javascript_data_type=DOM Node
|Return_value_description=C++

Reserved.  
Always returns -1.

JavaScript

Reserved.  
Always returns -1.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''addRule''' method to add a rule that sets all bold text appearing in a DIV to the color blue.
|LiveURL=
|Code=
&lt;STYLE&gt;
&lt;/STYLE&gt;
&lt;DIV&gt;
Internet Explorer makes &lt;B&gt;HTML&lt;/B&gt; dynamic.
&lt;/DIV&gt;
&lt;SCRIPT&gt;
   var new_rule;
   new_rule {{=}} document.styleSheets[0].addRule("DIV B", "color:blue", 0);
&lt;/SCRIPT&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
You can add up to 4095 style rules with the '''addRule''' method. After that, the method returns an "Invalid Argument" exception.
You can apply rules to a disabled [[css/cssom/styleSheet|'''styleSheet''']], but they do not apply to the document until you enable the '''styleSheet'''.
|Import_Notes=
===Syntax===
===Parameters===
;''sSelector'' [in]:'''String''' that specifies the selector for the new rule. Single contextual selectors are valid. For example, "'''div''' '''p''' '''b'''" is a valid contextual selector.
;''sStyle'' [in]:'''String''' that specifies the style assignments for this style rule. This style takes the same form as an inline style specification. For example, "<code>color:blue</code>" is a valid style parameter.
;''iIndex'' [in, optional]:'''Integer''' that specifies the zero-based position in the [[css/cssom/rules|'''rules''']] collection where the new style rule should be placed.<dl class{{=}}"indent"><dt><a id{{=}}"-1"/>'''-1'''</dt><dd>Default. The rule is added to the end of the collection.</dd></dl>
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>IHTMLStyleSheet</code>
*<code>[[css/cssom/styleSheet|styleSheet]]</code>
*<code>Reference</code>
*<code>[[css/cssom/methods/removeRule|removeRule]]</code>
*<code>[[css/cssom/rules|rules]]</code>
*<code>[[css/cssom/styleSheets|styleSheets]]</code>
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}