{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information.
|Checked_Out=No
|Content=Broken Links, Compatibility Incomplete
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''input''' element (&lt;input&gt;) is a multipurpose element for representing form widgets. The type of widget depends on the <code>type</code> attribute.}}
{{Markup_Element
|DOM_interface=dom/HTMLInputElement
|Content====HTML information===
{{{!}} class="wikitable"
{{!}}-
!Closing Tag
{{!}}The input element is a void element. An input element must have a start tag but must not have an end tag
{{!}}-
!CSS Display
{{!}}inline
{{!}}-
!HTML Element Categories
{{!}}flow phrasing interactive
{{!}}}

The input element behavior varies depending on the value of its [[html/elements/input/type|type]] attribute:
* [[html/elements/input/type/button|type=button]]
* [[html/elements/input/type/checkbox|type=checkbox]]
* [[html/elements/input/type/color|type=color]]
* [[html/elements/input/type/date|type=date]]
* [[html/elements/input/type/datetime-local|type=datetime-local]]
* [[html/elements/input/type/email|type=email]]
* [[html/elements/input/type/file|type=file]]
* [[html/elements/input/type/hidden|type=hidden]]
* [[html/elements/input/type/image|type=image]]
* [[html/elements/input/type/month|type=month]]
* [[html/elements/input/type/number|type=number]]
* [[html/elements/input/type/password|type=password]]
* [[html/elements/input/type/radio|type=radio]]
* [[html/elements/input/type/range|type=range]]
* [[html/elements/input/type/reset|type=reset]]
* [[html/elements/input/type/time|type=time]]
* [[html/elements/input/type/search|type=search]]
* [[html/elements/input/type/submit|type=submit]]
* [[html/elements/input/type/tel|type=tel]]
* '''[[html/elements/input/type/text|type=text]]''' (default if type is not set or empty)
* [[html/elements/input/type/url|type=url]]
* [[html/elements/input/type/week|type=week]]

Other valid attributes for the input element are <code>[[html/attributes/accept|accept]]</code>, <code>[[html/attributes/alt|alt]]</code>, <code>[[html/attributes/autocomplete|autocomplete]]</code>, <code>[[html/attributes/autofocus|autofocus]]</code>, <code>[[html/attributes/checked|checked]]</code>, <code>[[html/attributes/dirname|dirname]]</code>, <code>[[html/attributes/disabled|disabled]]</code>, <code>[[html/attributes/form|form]]</code>, <code>[[html/attributes/formaction|formaction]]</code>, <code>[[html/attributes/formenctype|formenctype]]</code>, <code>[[html/attributes/formmethod|formmethod]]</code>, <code>[[html/attributes/formnovalidate|formnovalidate]]</code>, <code>[[html/attributes/formtarget|formtarget]]</code>, <code>[[html/attributes/height|height]]</code>, <code>[[html/attributes/list|list]]</code>, <code>[[html/attributes/max_(HTMLInputElement)|max]]</code>, <code>[[html/attributes/maxLength|maxlength]]</code>, <code>[[html/attributes/min|min]]</code>, <code>[[html/attributes/multiple|multiple]]</code>, <code>[[html/attributes/name|name]]</code>, <code>[[html/attributes/pattern|pattern]]</code>, <code>[[html/attributes/placeholder|placeholder]]</code>, <code>[[html/attributes/readonly|readonly]]</code>, <code>[[html/attributes/required|required]]</code>, <code>[[html/attributes/size|size]]</code>, <code>[[html/attributes/src|src]]</code>, <code>[[html/attributes/step|step]]</code>, <code>[[html/attributes/value|value]]</code>, <code>[[html/attributes/width|width]]</code>, and global element attributes. Note that some attributes do not apply for certain types.

Internationalization topics related to the <code>input</code> element:
* [http://www.w3.org/International/techniques/authoring-html#formdir Managing text direction in form controls]
* [http://www.w3.org/International/techniques/authoring-html#localdata Working with date formats]
* [http://www.w3.org/International/techniques/authoring-html#localnames Working with personal names]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''input''' element to create different types of input controls.
|Code=<form action="http://example.org/survey" method=post>
<p>Name</p>
<br><input name="control1" type="text" value="Your Name">
<P>Password</P>
<br><input type="password" name="control2">
<p>Color</p>
<br><input type="radio" name="control3" value="0" checked>Red
<input type="radio" name="control3" value="1">Green
<input type="radio" name="control3" value="2">Blue
<p>Comments</p>
<br><input type="TEXT" name="control4" size="20,5" maxlength="250">
<p><input name="control5" type=checkbox checked>Send receipt</p>
<p><input type="submit" value="OK"><input type="reset" value="reset"></p>
</form>
|LiveURL=http://code.webplatform.org/gist/6364130
}}
}}
{{Notes_Section
|Usage=To cater for international users see: [http://www.w3.org/International/techniques/authoring-html#form-dir Managing text direction in form controls]
|Notes=For code samples, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251128 Form controls part 1] and [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251131 Form controls part 2: validation] on the Windows Internet Explorer sample site.

Firefox will, unlike other browsers, by default, [http://stackoverflow.com/questions/5985839/bug-with-firefox-disabled-attribute-of-input-not-resetting-when-refreshing persist the dynamic disabled state and (if applicable) dynamic checkedness] of an '''input''' across page loads. Setting the value of the <code>autocomplete</code> attribute to <code>off</code> disables this feature; this works even when the <code>autocomplete</code> attribute would normally not apply to the '''input''' by virtue of its <code>type</code>. See [https://bugzilla.mozilla.org/show_bug.cgi?id=654072 Mozilla bug #654072].
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/forms.html#the-input-element
|Status=W3C Candidate Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=HTML
|Manual_links=
|External_links=http://www.w3.org/TR/html-markup/input.html#input
|Manual_sections=
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}