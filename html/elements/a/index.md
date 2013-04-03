{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''a''' element (&lt;a&gt;) defines a hyperlink (a link) to any content, may be another page, another section of the same page, an image/file or it may invoke a JavaScript function.}}
{{Markup_Element
|DOM_interface=dom/HTMLAnchorElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following examples use the '''a''' element to link to files, open a file, include an image as part of a link, define an anchor, and invoke a function.
|Code=&lt;!-- Link to a server. --&gt;
&lt;a href{{=}}"http://www.microsoft.com"&gt;Microsoft home page.&lt;/a&gt;

&lt;!-- Link to a file in the same directory. --&gt;
&lt;a href{{=}}"home.htm"&gt;home.htm&lt;/a&gt;

&lt;!-- Open a file in the window specified by TARGET. --&gt;
&lt;a target{{=}}"viewer" HREF{{=}}"sample.htm"&gt;Open in window&lt;/a&gt;

&lt;!-- Include an IMG element as a part of the link. --&gt;
&lt;a href{{=}}"http://www.microsoft.com"&gt;&lt;img src{{=}}"images/bullet.png"&gt;link&lt;/a&gt; 

&lt;!-- Link to an anchor. --&gt;
&lt;a href{{=}}"#anchor"&gt;anchor&lt;/a&gt;

&lt;!-- Define an anchor. --&gt;
&lt;a name{{=}}"anchor"&gt;

&lt;!-- Invoke a JScript function. --&gt;
&lt;a href{{=}}"javascript:window.open()"&gt;link&lt;/a&gt;

&lt;!-- Links to a document and uses the ''rel'' attribute to add semantics to the link. --&gt;
&lt;a href{{=}}"http://creativecommons.org/licenses/by/3.0/" rel{{=}}"license"&gt;cc by 3.0&lt;/a&gt;
|LiveURL=http://code.webplatform.org/gist/5281100
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''a''' element requires the [[html/attributes/href|'''href''']] or the [[html/attributes/name|'''name''']] attribute to be specified.
Both text and images can be included within an anchor. An image that is an anchor has a border whose color indicates whether the link has been visited.  To prevent this border from appearing, you can set the '''img''' element's [[html/attributes/border|'''border''']] attribute to 0 or omit the '''border''' attribute.  You can also use CSS attributes to override the default appearance of '''a''' and '''img''' elements.

Optionally the [[html/attributes/rel|'''rel''']] element may be specified to provide semantic meaning to the link target.
|Import_Notes====HTML information===
{{{!}} class="wikitable"
{{!}}-
!Closing Tag
{{!}}required
{{!}}-
!CSS Display
{{!}}inline
{{!}}}

 
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=22.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8 and later
|Note=A [[html/elements/table|'''table''']] object does not function properly when contained within an '''a''' tag. The value of the [[html/attributes/href|'''href''']] attribute depends on the current document compatibility mode.  Internet Explorer 8 and later. When Protected Mode is enabled and a Web page contains an '''anchor link''' with a named [[html/attributes/target|'''target''']], Windows Internet Explorer opens the target of the link in a new window when the target has a different integrity level than the Web page containing the link. For more information, see Understanding and Working in Protected Mode Internet Explorer.
}}
}}
{{See_Also_Section
|Topic_clusters=HTML
|External_links=* [http://www.w3.org/TR/html4/struct/links.html#edef-A HTML 4.01 specification]
* [http://www.w3.org/TR/2012/CR-html5-20121217/text-level-semantics.html#the-a-element HTML 5 specification]
* [http://www.whatwg.org/specs/web-apps/current-work/multipage/text-level-semantics.html#the-a-element WHATWG specification]
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/HTML/Element/a
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}