{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information.
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Represents the main content of the body of a document or application.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example shows a basic usage of the <code>&lt;main&gt;</code> element
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
  &lt;title&gt;Main element example&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;header&gt;
    &lt;h1&gt;The main element&lt;/h1&gt;
  &lt;/header&gt;
  &lt;main&gt;
    &lt;h2&gt;Some content on the main element&lt;/h2&gt;

    &lt;article&gt;
      ...
    &lt;/artice&gt;
    &lt;section&gt;
      ...
    &lt;/section&gt;
  &lt;/main&gt;
  &lt;footer&gt;
    Copyright 2013 Web Platform
  &lt;/footer&gt;
&lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes=* It is advised to use ARIA <code>role="main"</code> attribute on the main element until browsers have implemented the element.

* There must not be more than one <code>&lt;main&gt;</code>  element in a document, and it must not be a descendent of an <code>&lt;article&gt;</code>, <code>&lt;aside&gt;</code>, <code>&lt;footer&gt;</code>, <code>&lt;header&gt;</code>, or <code>&lt;nav&gt;</code>  element.
}}
{{Related_Specifications_Section
|Specifications={{Related_Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/grouping-content.html#the-main-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/grouping-content.html#the-main-element
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=Chrome Canary 26.0.1396.1
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=Firefox Nightly 21.0a1
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Document Structure
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}