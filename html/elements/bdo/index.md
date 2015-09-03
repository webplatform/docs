{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information. Delete HTML information sub section.
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''bdo''' element (&lt;bdo&gt;) forces a string to be displayed in order specified by the DIR attribute. ("BDO" stands for Bi-Directional Override.)}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=Closing tag required
|CSS_display=inline
|Content=Internationalization topics related to the <code>bdo</code> element:
* [http://www.w3.org/International/techniques/authoring-html#bdo Overriding the Unicode bidirectional algorithm]
* [http://www.w3.org/International/techniques/authoring-html#inline Mixing text direction inline]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''BDO''' element to enforce a left-to-right reading order on a block of text.

The following string includes a product code containing some Arabic alphabets followed by hyphens and ASCII digits, which, on the whole, is expected to be displayed with the alphabet part on the left, and the number part on the right, just like N-T-12345.

Note that the order of characters of input (in other words the order of characters that is stored on disk or read from disk) is the same for the product numbers in both languages, i.e. N, HYPHEN, T, HYPHEN, 1, 2, 3, 4, 5 for English, and NUN, HYPHEN, TA, HYPHEN, 1, 2, 3, 4, 5 for Arabic.
|Code=Our product N-T-12345 will be shipped as &lt;BDO DIR{{=}}"ltr"&gt;ن-ت-12345&lt;/BDO&gt; in Egypt.
|LiveURL=The solution is to override the bidirectional attribute and force the order in the block of text inside a '''BDO''' element whose [[html/attributes/dir|'''DIR''']] attribute is set to '''ltr'''.
}}
}}
{{Notes_Section
|Notes====Remarks===
Without the BDO tag, the expectation is broken because of the Unicode bidirectional algorithm applied implicitly. While the Arabic alphabets are given inherent right-to-left attribute and the English alphabet left-to-right attribute, symbols such as a hyphen are given neutral attribute. During the process of the bidirectional algorithm, the neutral ones are treated as either right-to-left or left-to-right depending on the context. Thus a mixture of text containing bidirectional and neutral elements may result in unwanted presentation. Use BDO tag to force the context to be strong right-to-left or left-to-right, overwriting the inherent directionality.

This element is available in HTML and script as of Microsoft Internet Explorer 5.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-bdo-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-bdo-element
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/dirlang.html#edef-BDO
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[css/properties/direction|direction]]</code>
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
|Notes_rows=
}}