{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs compat
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Mixed}}
{{API_Name}}
{{Summary_Section|Parses and inserts HTML code at or beyond the edges of an element within the document hierarchy.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=where
|Data type=String
|Description=Where to insert the HTML text. Must be one of the following values:
{{{!}} class="wikitable"
{{!}}-
!Value
!Description
{{!}}-
{{!}}"beforebegin"
{{!}}Before the element itself.
{{!}}-
{{!}}"afterbegin"
{{!}}Just inside the element, before its first child.
{{!}}-
{{!}}"beforeend"
{{!}}Just inside the element, after its last child.
{{!}}-
{{!}}"afterend"
{{!}}After the element itself.
{{!}}}
|Optional=No
}}{{Method Parameter
|Index=1
|Name=html
|Data type=String
|Description=Well-formed HTML code to insert. The string can be a combination of text and HTML tags.
|Optional=No
}}
|Method_applies_to=dom/Element
|Example_object_name=element
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example uses the '''insertAdjacentHTML''' method to insert script into the page.
|Code=var sHTML{{=}}"&lt;input type{{=}}button onclick{{=}}" + 
    "go2()" + " value{{=}}'Click Me'&gt;&lt;BR&gt;"
var sScript{{=}}'&lt;SCRIPT DEFER&gt;'
sScript {{=}} sScript + 
    'function go2(){ alert("Hello from inserted script.") }'
sScript {{=}} sScript + '&lt;/script' + '&gt;';
ScriptDiv.insertAdjacentHTML("afterBegin",sHTML + sScript);
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/insertscript_1.htm
}}
}}
{{Notes_Section
|Usage=Use this method to add HTML to the page before/after an element or at the beginning or at the end of an element.
|Notes=*In XML documents, this methods will fail if the '''html''' parameter is not well-formed, valid HTML.
*This method will fail if "afterend" or "beforebegin" is used when the context is the root element of the document.
*If the text contains HTML tags, the method parses and formats the text as it is inserted.
{{TODO|The notes below need to be verified.}}
*You cannot insert text while the document is loading. Wait for the [[dom/Element/load|'''onload''']] event to fire before attempting to call this method.
*When using the '''insertAdjacentHTML''' method to insert script, you must include the [[html/attributes/defer|'''DEFER''']] attribute in the [[html/elements/script|'''script''']] element.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Parsing and Serialization
|URL=http://domparsing.spec.whatwg.org/
|Status=Living Standard
|Relevant_changes=Section 6, 6.3
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/HTMLElement/innerHTML|innerHTML]]</code>
*<code>[[dom/HTMLElement/outerHTML|outerHTML]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}