{{Page_Title|button}}
{{Flags
|High-level issues=Needs Review
|Content=Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''button''' element (<code>&lt;button&gt;</code>) defines a clickable button.|The "button" tag is one of many ways to create buttons on an HTML page_ A web developer can also use the "input" tag in conjunction with type="button" or by styling an "a" tag to achieve the same functionality. However, those may be harder and their results may not be as clean.
}}
{{Markup_Element
|DOM_interface=dom/HTMLButtonElement
|Content=Inside a &lt;button&gt; element you can put content, like text or images. It generates a clickable button with the specific value of the element displayed on the button.

The &lt;button&gt; element can also be used as submit button to send [[html/elements/form|'''form''']] data to the server. The usage is the same as with any other button.

<b>Attributes (HTML 4):</b>
<ul>
<li><b>name</b>
<ul>
<li>The name of the button. This can be used to identify which button was used to submit a form.</li>
</ul>
</li>
<li><b>type</b>
<ul>
<li>This specifies the type of the button. If omitted, the type is <code>submit</code>. The following types are possible:
<ul>
<li>submit: the button submits the form it is associated with. This is the default value.</li>
<li>reset: the button resets the form it is associated with. All form fields will be cleared.</li>
<li>button: the button has no default action</li> 
</ul>
</li>
</ul>
</li>
<li><b>value</b>
<ul>
<li>The initial value of the button.</li>
</ul>
</li>
<li><b>disabled</b>
<ul>
<li>This specifies whether the button is disabled or not (true, false). A disabled button won't be clickable.</li>
</ul>
</li>
</ul>

<b>Additional attributes (HTML 5, candidate specification):</b>
<ul>
<li><b>autofocus</b>
<ul>
<li>When this attribute is set to "true" the button will automatically be focused after the page load. Only one form-associated element can have this attribute set to "true".</li>
</ul>
</li>
<li><b>form</b>
<ul>
<li>Specifies which form the button is associated with. The value of the attribute must be the id attribute of the form. If this attribute is not specified, the button must be a descendant of the form itself to be able to submit form data. Use this, if you don't want to put the submit button within the form itself.</li>
</ul>
</li>
<li><b>formaction</b>
<ul>
<li>The URI of a programm that pocesses the information from the form. When present, it will override the action attribute of the form.</li>
</ul>
</li>
<li><b>formmethod</b>
<ul>
<li>The HTTP method to send the form data. This can either be "post" or "get". If specified, it will override the form's method attribute.</li>
</ul>
</li>
<li><b>formnovalidate</b>
<ul>
<li>If the button is a submit button, this attribute specifies whether the form should be validated or not. It overrides the novalidate attribute of the form it belongs to.</li>
</ul>
</li>
<li><b>formtarget</b>
<ul>
<li>This attribute is a keyword, indicating where to display the response that is received after submitting the form. This can be one of the following:
<ul>
<li>_self: load the reponse into the same context as the form itself. This is the default value.</li>
<li>_blank: load the reponse into a new, unnamed context</li>
<li>_parent: loads the response into the parent context. If there is no parent, it will behave the same as _self.</li>
<li>_top: loads the response into the top-most context. This is the browsing context of an ancestor of the current context. If there is no parent, it will behave the same as _self.</li>
</ul>
</li>
</ul>
</li>
</ul>

All these attributes, except <code>name</code>, have default values and can be omitted.
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
|Notes=Since the default for the <code>type</code> attribute is <code>submit</code>, the type can be omitted if no other type needs to be used. Historical browser versions may have different standard <code>type</code> values.

Internet Explorer historically has had problems with the button element, especially when used in conjunction with type="submit".  This is fixed with newer versions.
|Import_Notes====Standards information===
*[http://www.w3.org/TR/html401/ HTML 4.01 Specification], Section 17.5
*[http://http://www.w3.org/html/wg/drafts/html/CR HTML5 Candidate Specification], Section 4.10.8
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