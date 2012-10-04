{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example shows how to use the '''rules''' collection to identify the color specified in style sheet rules.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rules_1.htm
|Code=
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;SCRIPT&gt;
function ruleColor(ruleIndex) {
    alert("The color of rule " + ruleIndex + " is " +
        document.styleSheets[0].rules.item(ruleIndex).style.color + ".");
}
&lt;/SCRIPT&gt;
&lt;STYLE&gt;
.rule0 {color:"red"}
.rule1 {color:"blue"} 
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;P class{{=}}"rule0" id{{=}}"oRule0Span"&gt;
    Rule 0 is applied to this line.
&lt;/P&gt;
&lt;P class{{=}}"rule1" id{{=}}"oRule1Span"&gt;
    Rule 1 is applied to this line.
&lt;/P&gt;
&lt;BUTTON onclick{{=}}"ruleColor(0)"&gt;Color of Rule 0&lt;/BUTTON&gt; 
&lt;BUTTON onclick{{=}}"ruleColor(1)"&gt;Color of Rule 1&lt;/BUTTON&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
This collection is always accessible, even if the style sheet is not enabled. Rules are added to the '''rules''' collection with the [[css/cssom/methods/addRule|'''addRule''']] method on the individual style sheet. A rule that is added to a [[html/attributes/disabled|'''disabled''']] style sheet does not apply to the document unless the style sheet is enabled. Rules are deleted with the [[css/cssom/methods/removeRule|'''removeRule''']] method.
The rules in this collection are in the source order of the document. As rules are added or deleted through the Cascading Style Sheets (CSS) Object Model, a rule's absolute position in the '''rules''' collection might change, but its position relative to other rules remains the same. When you add rules without specifying an index, the rule gets added to the document last. If you specify an index, however, the rule is inserted before the rule currently in that ordinal position in the collection. If the specified index is greater than the number of rules in the collection, the rule is added to the end.
|Import_Notes=
===Members===
The '''rules''' collection has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''rules''' collection has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[css/cssom/rules/item|'''item (rules)''']]
|Retrieves an object from the '''rules''' collection.
|}
 

====Properties====
The '''rules''' collection has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[css/cssom/properties/length|'''length''']]
|Retrieves  the number of properties that  are  explicitly set on the parent object.
|-
|[[dom/properties/length|'''length''']]
|Sets or retrieves the number of objects in a collection.
|}
 

}}
{{See_Also_Section
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}