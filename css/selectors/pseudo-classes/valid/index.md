{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Needs title, summary, spec reference, standardization status, fix table coding, fix broken links
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS_Selector}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example puts a green border on a field when it is valid and a red border with bold text when it isn't. The email field is required, but the others aren't. The URL field is pre-filled with a bad URL, so it isn't valid when the page opens. In addition, the two optional fields are styled with light gray backgrounds, and the required field with an eye-catching yellow background.
|Code=&lt;!DOCTYPE html &gt;
&lt;html&gt;
&lt;head&gt;
  &lt;title&gt;:valid/:invalid Pseudo-class Example&lt;/title&gt;
  &lt;style type{{=}}"text/css"&gt;

  #PC1 input:valid { 
    border:solid lime;
    font-weight:normal;
  }
  #PC1 input:invalid { 
    border:solid red;
    font-weight:bold;
  }
  #PC1 input:required {
    background-color:Yellow;
  }
  #PC1 input:optional {
    background-color:LightGray;
  }       
  &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;form id{{=}}"PC1"&gt;
    &lt;p&gt;&lt;label&gt;Enter some text: &lt;input type{{=}}"text"/&gt;&lt;/label&gt;&lt;/p&gt;
    &lt;p&gt;&lt;label&gt;*Enter a valid email address: &lt;input type{{=}}"email" required /&gt;&lt;/label&gt;&lt;/p&gt;
    &lt;p&gt;&lt;label&gt;Enter a valid URL: &lt;input type{{=}}"url" value{{=}}"not a url"/&gt;&lt;/label&gt;&lt;/p&gt;       
    &lt;p&gt;* required field&lt;/p&gt;
  &lt;/form&gt;
&lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===

The criteria used to determine whether an input field is ''valid'' correspond to the properties of the [http://go.microsoft.com/fwlink/p/?LinkID{{=}}233317 ValidityState] Document Object Model (DOM) object. For more information on determining validity, see the following reference topics:
{| class="wikitable"
|-
!Term
!Description
|-
|[http://go.microsoft.com/fwlink/p/?LinkId{{=}}238204 customError]
|The input field has raised a custom error, which has been set by the element's [http://go.microsoft.com/fwlink/p/?LinkId{{=}}233319 setCustomValidity] method (string is not empty).
|-
|[http://go.microsoft.com/fwlink/p/?LinkId{{=}}238207 patternMismatch]
|The user entered something that does not match what the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}233320 pattern] attribute specifies, such as letters when numbers were expected.
|-
|[http://go.microsoft.com/fwlink/p/?LinkId{{=}}238208 rangeOverflow]
|The user entered a value greater than what was specified by the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}233323 max] attribute on a range control.
|-
|[http://go.microsoft.com/fwlink/p/?LinkId{{=}}238209 rangeUnderflow]
|The user entered a value less than what was specified by the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}233322 min] attribute on a range control.
|-
|[http://go.microsoft.com/fwlink/p/?LinkId{{=}}238205 stepMismatch]
|The user entered a value that doesn't correspond to an allowed value as specified by the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}233324 step] and [http://go.microsoft.com/fwlink/p/?LinkId{{=}}233322 min] attributes. For example, the user entered an odd number when even numbers were expected.
|-
|[http://go.microsoft.com/fwlink/p/?LinkId{{=}}238211 tooLong]
|A control has a value that is longer than the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}238222 maxlength] attribute specifies. Because Windows Internet Explorer allows a user to enter only the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}238222 maxlength] number of characters, this usually occurs when the default value contains too many characters.
|-
|[http://go.microsoft.com/fwlink/p/?LinkId{{=}}238212 typeMismatch]
|The user entered something that is not the correct syntax, such as an incorrectly formatted URL or email address.
|-
|[http://go.microsoft.com/fwlink/p/?LinkId{{=}}238213 valid]
|The input field value does not have any validity errors.
|-
|[http://go.microsoft.com/fwlink/p/?LinkId{{=}}238216 valueMissing]
|The user has not entered a value on a required field.
|}
 
A required field will be invalid until the correct input is entered. A field that isn't required but has validation, such as a URL field, will be valid until text is entered.
|Import_Notes====Syntax===

selector
:valid
===Parameters===
;''selector'':A CSS simple selector.
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
|Topic_clusters=Pseudo-Classes, Selectors
|Manual_sections====Related pages (MSDN)===
*<code>[http://go.microsoft.com/fwlink/p/?LinkId{{=}}238198 HTML5 Forms (Internet Explorer 10 Guide for Developers)]</code>
*<code>[http://go.microsoft.com/fwlink/p/?LinkID{{=}}233316 validity attribute]</code>
*<code>[http://go.microsoft.com/fwlink/p/?LinkID{{=}}233317 ValidityState object]</code>
*<code>Related pseudo-classes</code>
*<code>[[css/selectors/pseudo-classes/:invalid|:invalid]]</code>
*<code>[[css/selectors/pseudo-classes/:optional|:optional]]</code>
*<code>[[css/selectors/pseudo-classes/:required|:required]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}