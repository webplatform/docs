{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Non-standard; deletion candidate
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Non standard. Removes a rule from a style sheet.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=index
|Data type=Number
|Description=The index value of the rule to be deleted from the style sheet. If an index is not provided, the first rule in the [[css/cssom/rules|'''rules''']] collection is removed.
|Optional=No
}}
|Method_applies_to=css/cssom/styleSheet
|Example_object_name=stylesheet
|Return_value_name=object
|Javascript_data_type=void
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''removeRule''' method to delete a rule from the [[css/cssom/rules|'''rules''']] collection, which causes the text to reflow according to the new rules.
|Code=&lt;style&gt;
P {color:green}
&lt;/style&gt;
:
&lt;script&gt;
function removeTheRule() {
    // Style sheets and rules are zero-based collections; therefore,
    // the first item is item 0 in the collection.
    var iSheets {{=}} document.styleSheets.length;
    var iRules {{=}} document.styleSheets[iSheets-1].rules.length;
    // make sure there is a rule to delete
    if (1 &lt; iRules) {            
        document.styleSheets[iSheets-1].removeRule(1);
        // Force the page to render the change.
        effectRules = document.getElementById("oEffectRules");
        effectRules.innerHTML {{=}} effectRules.innerHTML;
	}
}
&lt;/script&gt;
:
&lt;p id{{=}}"oEffectRules"&gt;This text has the new style applied to it.
&lt;/p&gt;
:
&lt;button onclick{{=}}"removeTheRule()"&gt;Remove the new rule.&lt;/button&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/removeRule.htm
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The document does not automatically reflow when the rule is removed. To see the change, you must reflow the document. You can reflow the objects affected using a number of methods. For example, you can reflow the style change only on affected text by setting the text equal to itself. Alternately, you can reload the entire document using the [[dom/Location/reload|'''reload''']] method. When you use the '''refresh''' method on a table, its content is reflowed.
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
|Topic_clusters=CSSOM
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>IHTMLStyleSheet</code>
*<code>[[css/cssom/styleSheet|styleSheet]]</code>
*<code>Reference</code>
*<code>[[css/cssom/methods/addRule|addRule]]</code>
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