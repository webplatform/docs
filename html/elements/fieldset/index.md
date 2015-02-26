{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''fieldset''' element is used to group related fields within a form.}}
{{Markup_Element
|DOM_interface=dom/HTMLFieldSetElement
|Tag_omissions=Closing tag required
|CSS_display=block
|Content=The ''fieldset'' element represents a set of form controls. Optionally given a name with a child '''legend''' element.

=== attributes ===

'''NOTE''': Those attributes are considered valid since HTML5

; disabled : If this Boolean attribute is set, the form controls that are its descendants, except descendants of its first optional '''legend''' element, are disabled, i.e., not editable. They won't receive any browsing events, like mouse clicks or focus-related ones. Often browsers display such controls as gray.
; form : This attribute has the value of the id attribute of the '''form''' element its related to. Its default value is the id of the nearest &lt;form> element it is a descendant of.
; name : The name associated with the group. This is for use in the <code>form.elements</code> API.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Simple form with fieldset, legend, and label elements.
|Code=&lt;form action="" method="post"&gt;
  &lt;fieldset&gt;
    &lt;legend&gt;Title&lt;/legend&gt;
    &lt;label for="radio"&gt;Click me&lt;/label&gt;
    &lt;input type="radio" name="radio" id="radio"&gt;
  &lt;/fieldset&gt;
&lt;/form&gt;
|LiveURL=http://code.webplatform.org/gist/f77f0a06304503ecddd6
}}{{Single Example
|Language=HTML
|Description=The following snippet shows a '''fieldset''' with a checkbox in the legend that controls whether or not the fieldset is enabled.
|Code=<form>
  <fieldset name="clubfields" disabled>
    <legend>
      <label for="club">Use Club Card</label>
      <input type="checkbox" id="club" name="club" onchange="form.clubfields.disabled = !checked">
    </legend>
    <div>
      <label for="clubname">Name on card:</label>
      <input name="clubname" type="text">
    </div>
    <div>
      <label for="clubnum">Card number:</label>
      <input name="clubnum" type="number">
    </div>
    <div>
      <label for="clubnum">Expiry date:</label>
      <input name="clubexp" type="date">
    </div>
  </fieldset>
</form>
|LiveURL=http://code.webplatform.org/gist/fc26d3507ee33bdd6043
}}{{Single Example
|Language=HTML
|Description=Example with nested '''fieldset''' elements.
|Code=<form action="">
  <fieldset name="clubfields" disabled>
    <legend>
      <label for="club">Use Club Card</label>
      <input type="checkbox" name="club" id="club" onchange="form.clubfields.disabled = !checked">
    </legend>
    <div>
      <label for="">Name on card:</label>
      <input name="clubname">
    </div>
    <fieldset name="numfields">
      <legend>
        <label for="clubtype">My card has numbers on it</label>
        <input type="radio" checked name="clubtype" id="clubtype" onchange="form.numfields.disabled = !checked">
      </legend>
      <div>
        <label for="clubnum">Card number:</label>
        <input name="clubnum" id="clubnum" type="text">
      </div>
    </fieldset>
    <fieldset name="letfields" disabled>
      <legend>
        <label>My card has letters on it</label>
        <input type="radio" name="clubtype" id="clubtype" onchange="form.letfields.disabled = !checked">
      </legend>
      <div>
        <label for="clublet">Card code:</label>
        <input name="clublet" id="clublet">
      </div>
    </fieldset>
  </fieldset>
</form>
|LiveURL=http://code.webplatform.org/gist/91bca1371d394bf3c52d
}}
}}
{{Notes_Section
|Usage=Fieldsets are not required but useful for grouping elements in a form to enhance the visual flow and usability of complex forms. optionally you can use a [[html/elements/legend|'''legend''']] element to give your '''fieldset''' element a caption.
|Notes====Default layout===
Typically, the browser draws a box around the containing elements of every fieldset. This border can be disabled via CSS <code>border: none;</code> The border contains the legend by default. See [[html/elements/legend|'''legend''']] for details.

The [https://html.spec.whatwg.org/multipage/rendering.html#the-fieldset-and-legend-elements "Rendering" section of the WHATWG HTML specification] suggests [[css/properties/min-width|<code>min-width</code>]]<code>: min-content</code> as part of the default style for '''fieldset''', and many browsers implement such styling (or something that approximates it); almost no other element shares this default style. See also [http://stackoverflow.com/questions/17408815/fieldset-resizes-wrong-appears-to-have-unremovable-min-width-min-content StackOverflow], [https://bugzilla.mozilla.org/show_bug.cgi?id=504622 Mozilla bug #504622], and [https://bugs.webkit.org/show_bug.cgi?id=123507 WebKit bug #123507].

===Nesting fieldsets===
It’s also possible and in certain use cases pretty useful to nest fieldsets.

===Compatibility===
Not all form control descendants of a disabled '''fieldset''' are properly disabled in IE11; see [https://connect.microsoft.com/IE/feedbackdetail/view/817488 IE bug 817488: <code>input[type="file"<nowiki>]</nowiki></code> not disabled inside disabled <code>fieldset</code>] and [https://connect.microsoft.com/IE/feedbackdetail/view/962368/can-still-edit-input-type-text-within-fieldset-disabled IE bug 962368: Can still edit <code>input[type="text"<nowiki>]</nowiki></code> within <code>fieldset[disabled<nowiki>]</nowiki></code>].
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/forms.html#the-fieldset-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/forms.html#the-fieldset-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/interact/forms.html#edef-FIELDSET
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=HTML
|Manual_links=* [[html/elements/legend|'''legend''']] element
* [[html/elements/form|'''form''']] element
|External_links=* http://www.w3.org/TR/html5/forms.html#the-fieldset-element
* http://www.w3.org/TR/html5/rendering.html#the-fieldset-and-legend-elements
* http://www.w3.org/TR/html-markup/fieldset.html#fieldset
|Manual_sections=
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset
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