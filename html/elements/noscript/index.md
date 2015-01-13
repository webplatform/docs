{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=See to make the listing of events, methods etc to be generated automatically instead of being hardcoded.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic
|Content=Incomplete, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The HTML NoScript Element (<noscript>) defines a section of html to be inserted if a script type on the page is unsupported or if scripting is currently turned off in the browser.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Content=The ''noscript'' element content will not be visible if scripting is enabled in the browsers. It is used to present different contents and guide the user on what he should be seeing.

===HTML information===
{{{!}} class="wikitable"
{{!}}-
!Closing Tag
{{!}}required
{{!}}-
!CSS Display
{{!}}inline
{{!}}}


 
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=You must disable javascript for this to work.
|Code=&lt;script&gt;
    /* Do stuff with JavaScript */
&lt;/script&gt;
&lt;noscript&gt;
For full functionality of this site it is necessary to enable JavaScript. Here are the &lt;a href="http://www.enable-javascript.com/" &gt;instructions how to enable JavaScript in your web browser&lt;/a&gt;.
&lt;/noscript&gt;
|LiveURL=https://rawgithub.com/WebPlatformDocs/6364342/raw/47a37f3fe0d920a0c6a8a7974dca473589f1e4f5/dabblet.html
}}
}}
{{Notes_Section
|Usage=
|Notes=Browsers that don't support the noscript tag will render the content regardless of whether the javascript is supported
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5, section 4.3.2
|URL=http://www.w3.org/TR/html5/scripting-1.html#the-noscript-element
|Status=W3C Candidate Recommendation 31 July 2014
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01, section 18.3.1
|URL=http://www.w3.org/TR/html401/interact/scripts.html#h-18.3.1
|Status=W3C Recommendation 24 December 1999
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
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