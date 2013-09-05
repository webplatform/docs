{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Creates an instance of the element for the specified tag.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=tagName
|Data type=String
|Description=The name of an element. The element may be be an existing DOM element or an extension of a DOM element.
|Optional=No
}}{{Method Parameter
|Name=typeExtension
|Data type=String
|Description=Specifies the element that is extended with this method. The user specifies the extension with the element's <code>is=''</code> attribute. See examples.
|Optional=Yes
}}
|Method_applies_to=dom/document
|Example_object_name=document
|Return_value_name=element
|Javascript_data_type=Element
|Return_value_description=The created element.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''createElement''' method to dynamically update the contents of a Web page by adding an element selected from a drop-down list box.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;script&gt;
function create() {
  var output, option, newElement, tagSelect, contentSelect;
  tagSelect {{=}} document.getElementById("tag-select");
  contentSelect {{=}} document.getElementById("content-select");
  output {{=}} document.getElementById("output");
  output.innerHTML {{=}} "";
  option {{=}} tagSelect.options[tagSelect.selectedIndex];
  if (option.text.length &gt; 0) {
    newElement {{=}} document.createElement(option.textContent);
    newElement[option.value] {{=}} contentSelect.value;
    if (option.textContent {{=}}{{=}}{{=}} "a") {
      newElement.href {{=}} "http://www.bing.com";
    }
  }
  output.appendChild(newElement);
}
document.addEventListener("change", create, false);
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
  &lt;select id{{=}}"tag-select"&gt;
   &lt;option value{{=}}"textContent"&gt;a&lt;/option&gt;
   &lt;option value{{=}}"value"&gt;textarea&lt;/option&gt;
  &lt;/select&gt;
  &lt;select id{{=}}"content-select"&gt;
   &lt;option&gt;&lt;/option&gt;
   &lt;option value{{=}}"Text"&gt;Text&lt;/option&gt;
   &lt;option value{{=}}"More and More Text"&gt;More and More Text&lt;/option&gt;
  &lt;/select&gt;
  &lt;span id{{=}}"output"&gt;&lt;/span&gt;
 &lt;body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/createElement.htm
}}{{Single Example
|Language=HTML
|Description=Declaring an extended custom element.
|Code=<!-- <button> "is a" mega button -->
<button is="mega-button">
}}{{Single Example
|Language=JavaScript
|Description=Extending a DOM element.
|Code=var megaButton = document.createElement('button', 'mega-button');
// megaButton instanceof MegaButton === true
}}
}}
{{Notes_Section
|Usage=The properties of these created elements are read/write and can be accessed programmatically. Before you use new objects, you must explicitly add them to their respective collections or to the document. To insert new elements into the current document, use the [[dom/methods/insertBefore|'''insertBefore''']] method or the [[dom/methods/appendChild|'''appendChild''']] method.
|Notes=You must perform a second step when you use '''createElement''' to create the [[html/elements/input|'''input''']] element. The '''createElement''' method generates an input text box, because that is the default '''input''' [[html/attributes/type|'''type''']] property. To insert any other kind of '''input''' element, first invoke '''createElement''' for '''input''', and then set the '''type''' property to the appropriate value in the next line of code.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.4
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=5 - 7
|Note=When creating elements, setting a name attribute/property will fail to make the element enumerable by name (in forms, like someForm.someName. A non standard syntax must be used instead, ''document.createElement("<input name=\"someName\">")''.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=4
|Note=It is only possible to create [[html/elements/img|img]], [[html/elements/area|area]], and [[html/elements/option|option]] elements.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=5
|Note=It is not possible to create [[html/elements/frame|frame]] and [[html/elements/iframe|iframe]] elements.
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>Reference</code>
*<code>[[dom/methods/cloneNode|cloneNode]]</code>
*<code>[[dom/methods/removeNode|removeNode]]</code>
*<code>Conceptual</code>
*<code>About the W3C Document Object Model</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}