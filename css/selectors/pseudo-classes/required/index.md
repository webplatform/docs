{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Needs title, summary, spec reference, standardization status, broken links
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
A ''required'' field is a field that cannot be submitted without a value. A required field has the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}233321 required] attribute set in its [http://go.microsoft.com/fwlink/p/?LinkID{{=}}219805 input] element. The [http://go.microsoft.com/fwlink/p/?LinkId{{=}}233321 required] attribute can be set on text, URL, email, select, checkbox, or radio button controls, and on [http://go.microsoft.com/fwlink/p/?LinkId{{=}}233312 select] and [http://go.microsoft.com/fwlink/p/?LinkID{{=}}236896 textarea] elements. It is a Boolean attribute, and need be specified only on an element. When users hover the mouse over a required field, they'll see a tooltip stating that it is a required field. (If you've set the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}236898 title] attribute, that will be shown instead.)
|Import_Notes====Syntax===

selector
:required
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
*<code>[http://go.microsoft.com/fwlink/p/?LinkId{{=}}233321 required attribute]</code>
*<code>Related pseudo-classes</code>
*<code>[[css/selectors/pseudo-classes/:invalid|:invalid]]</code>
*<code>[[css/selectors/pseudo-classes/:optional|:optional]]</code>
*<code>[[css/selectors/pseudo-classes/:valid|:valid]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}