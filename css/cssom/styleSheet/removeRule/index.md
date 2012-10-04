{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''removeRule''' method to delete a rule from the [[css/cssom/rules|'''rules''']] collection, which causes the text to reflow according to the new rules.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/removeRule.htm
|Code=
&lt;STYLE&gt;
P {color:green}
&lt;/STYLE&gt;
:
&lt;SCRIPT&gt;
function removeTheRule() {
    // Style sheets and rules are zero-based collections; therefore,
    // the first item is item 0 in the collection.
    var iSheets {{=}} document.styleSheets.length;
    var iRules {{=}} document.styleSheets[iSheets-1].rules.length;
    // make sure there is a rule to delete
    if (1 &lt; iRules) {            
        document.styleSheets[iSheets-1].removeRule(1);
        // Force the page to render the change.
        oEffectRules.innerHTML{{=}}oEffectRules.innerHTML;
	}
}
&lt;/SCRIPT&gt;
:
&lt;P ID{{=}}oEffectRules&gt;This text has the new style applied to it.
&lt;/P&gt;
:
&lt;BUTTON onclick{{=}}"removeTheRule()"&gt;Remove the new rule.&lt;/BUTTON&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The document does not automatically reflow when the rule is removed. To see the change, you must reflow the document. You can reflow the objects affected using a number of methods. For example, you can reflow the style change only on affected text by setting the text equal to itself. Alternately, you can reload the entire document using the [[dom/methods/reload|'''reload''']] method. When you use the '''refresh''' method on a table, its content is reflowed.
|Import_Notes=
===Syntax===
===Parameters===
;''iIndex'' [in, optional]:'''Integer''' that specifies the index value of the rule to be deleted from the style sheet. If an index is not provided, the first rule in the [[css/cssom/rules|'''rules''']] collection is removed.
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>IHTMLStyleSheet</code>
*<code>[[css/cssom/styleSheet|styleSheet]]</code>
*<code>Reference</code>
*<code>[[css/cssom/methods/addRule|addRule]]</code>
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