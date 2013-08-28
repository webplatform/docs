{{Page_Title|button}}
{{Flags
|High-level issues=Needs Review
|Content=Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''button''' element (<code>&lt;button&gt;</code>) defines a clickable button.|The "button" tag is one of many ways to create buttons on an HTML page_ A web developer can also use the "input" tag in conjunction with type="button" or by styling an "a" tag to achieve the same functionality. However, those may be harder and their results may not be as clean.
}}
{{Markup_Element
|DOM_interface=dom/HTMLButtonElement
|Content=Inside a &lt;button&gt; element you can put content, like text or images. It generates a clickable button with the specific value of the element displayed on the button.

The &lt;button&gt; element can also be used as submit button to send [[html/elements/form|'''form''']] data to the server. The usage is the same as with any other button.

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This examples uses the <code>&lt;button&gt;</code> element to display a clickable button.
|Code=<button name="button">Click me</button>
|LiveURL=http://code.webplatform.org/gist/6365019
}}{{Single Example
|Language=HTML
|Description=This example shows how to use a submit <code>&lt;button&gt;</code> to send a form. Read about the [[html/elements/form|'''form''']] element to get further information about how to use forms.
|Code=<form action="fileOnTheServerWhichHandlesTheNewData.php">
  <label for="name">Name:</label>
  <input id="name" type="text" name="user_name">
  <button name="submitbutton">Submit</button>
</form>
|LiveURL=http://code.webplatform.org/gist/6365027
}}
}}
{{Notes_Section
|Usage=Generally, a button can be used whenever there should be a button clickable by the user. 

The ending tag is mandatory. The button should have a descriptive text inside it, otherwise the button will be empty and the user doesn't know what the button will do.

Please note that styling a submit button using the &lt;button&gt; element is easier than styling an [[html/elements/input|'''input''']] element with type <code>submit</code>.
|Notes====Remarks===
Since the default for the <code>type</code> attribute is <code>submit</code>, the type can be omitted if no other type needs to be used. Historical browser versions may have different standard <code>type</code> values.

Internet Explorer historically has had problems with the button element, especially when used in conjunction with type="submit".  This is fixed with newer versions.
|Import_Notes====Standards information===
*[http://www.w3.org/TR/html401/ HTML 4.01 Specification], Section 17.5
*[http://www.w3.org/TR/html5/ HTML5 Candidate Specification], Section 4.10.8
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Document Structure, HTML, Mobile
}}
{{Topics|HTML, UI}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button <button> on MDN]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}