{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent and Children information. Complete Compatibility table. Complete HTML information subsection.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Denotes one choice in a [[html/elements/select|select]] element.}}
{{Markup_Element
|DOM_interface=dom/HTMLOptionElement
|Tag_omissions=Closing tag omissible in certain cases
|Content=== Attributes ==
*<code>disabled</code> = boolean<br />if present, disable a option.
*<code>label</code> = string<br />Provides a label for element.<br />If there isn't, the label of an option element is the textContent of the element. 
*<code>value</code> = string<br />Provides a value for element.<br />If there isn't, the value of an option element is the textContent of the element. 
*<code>selected</code> = boolean<br />Represents the default selectedness of the element. [[#Example_A|[Example A]]]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''OPTION''' element to create individual items in a drop-down list box.
|Code=<nowiki><!DOCTYPE html>
<html>
 <head>
  <title>Example</title>
 </head>
 <body>
  <select id="car-list" size="1">
   <option value="1">BMW</option>
   <option value="2">PORSCHE</option>
   <option value="3" selected>MERCEDES</option>
  </select>
  <textarea id="text-area"></textarea>
 </body>
</html></nowiki>
}}{{Single Example
|Language=JavaScript
|Description=Using the markup of the previous example, this JavaScript example uses the [[dom/HTMLElement/options|'''options''']] collection to append the selected item of the list box in a text area.
|Code=function appendCar() {
  var carListElement = document.getElementById("car-list");
   document.getElementById("text-area").value +{{=}}carListElement.options[carListElement.selectedIndex].text + "\n";
}
document.addEventListener("DOMContentLoaded", appendCar, false);
}}{{Single Example
|Language=HTML
|Description=As a child of an optgroup element
|Code=<nowiki><form action="courseselector.dll" method="get">
  <p>Which course would you like to watch today?
  <p><label>Course:
    <select name="c">
      <optgroup label="8.01 Physics I: Classical Mechanics">
        <option value="8.01.1">Lecture 01: Powers of Ten</option>
        <option value="8.01.2">Lecture 02: 1D Kinematics</option>
        <option value="8.01.3">Lecture 03: Vectors</option>
      </optgroup>
      <optgroup label="8.02 Electricity and Magnestism">
        <option value="8.02.1">Lecture 01: What holds our world together?</option>
        <option value="8.02.2">Lecture 02: Electric Field</option>
        <option value="8.02.3">Lecture 03: Electric Flux</option>
      </optgroup>
      <optgroup label="8.03 Physics III: Vibrations and Waves">
        <option value="8.03.1">Lecture 01: Periodic Phenomenon</option>
        <option value="8.03.2">Lecture 02: Beats</option>
        <option value="8.03.3">Lecture 03: Forced Oscillations with Damping</option>
      </optgroup>
    </select>
  </label>
  <p><input type=submit value="▶ Play">
</form></optgroup></nowiki>
}}
}}
{{Notes_Section
|Notes=You can create new '''OPTION''' elements dynamically with the [[dom/Document/createElement|'''document.createElement''']] method, but you cannot change properties until the new element is added to a '''SELECT''' object. Or, you can create fully formed elements by using the [[dom/Option|'''Option''']] object, as follows:
 <code> var opt {{=}} new Option( 'Text', 'Value', fDefaultSelected ); </code>
You can add '''OPTION''' elements only to a '''SELECT''' element that is located in the same window where the '''OPTION''' elements are created.
Except for [[css/properties/background-color|'''background-color''']] and [[css/properties/color|'''color''']], style settings applied through the [[css/cssom/style|'''style''']] object for the '''option''' element are ignored. In addition, style settings applied directly to individual [[dom/HTMLElement/options|'''options''']] override those applied to the containing '''SELECT''' element as a whole.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/forms.html#the-option-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/forms.html#the-option-element
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/interact/forms.html#edef-OPTION
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|Topic_clusters=HTML
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=WebKit, Blink (Chrome, Safari and more)
|Version=Any
|Note=No support for event handlers.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=Earlier than 5
|Note=[[dom/HTMLAllCollection|'''document.all''']] excludes '''option''' elements. Instead, you can use the [[dom/HTMLElement/options|options]] collection property of the [[dom/HTMLSelectElement|select]] element to get them.
}}
}}