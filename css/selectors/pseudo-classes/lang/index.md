{{Page_Title|:lang(c)}}
{{Flags
|State=Not Ready
|Editorial notes=Needs title, summary, spec reference, standardization status, remove topic cluster flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The ''':lang(c)''' pseudo selector applies to documents that specifies the <code>lang</code> attribute to an HTML element.
{{Compatibility
|feature=pseudo-lang
}}
{{CSS_Selector}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following code example uses the ''':lang(C)''' pseudo-class to apply a color to any '''p''' elements that are explicitly given a language value of "en" (or a hyphen-separated subset thereof). The first paragraph gets "en-us" (a subset of "en") and thus turns green.
|Code=&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" 
    "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd"&gt;
&lt;html&gt;
&lt;head&gt;
&lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}8" /&gt;
&lt;title&gt;:lang pseudo-class&lt;/title&gt;
&lt;style type{{=}}"text/css"&gt;
p:lang(en) {
	color: green;
}
&lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div class{{=}}"body"&gt;
	
	&lt;h1&gt;:lang(C) Sample&lt;/h1&gt;
	
	&lt;!-- This paragraph gets "en-us" (a subset of "en") and thus turns green. --&gt;
	&lt;p lang{{=}}"en-us"&gt;This paragraph's language is set to "en-us", so it's green.&lt;/p&gt;
	&lt;!-- This paragraph has no language value and thus does not turn green. --&gt;
	&lt;p&gt;This paragraph has no language attribute, so it doesn't turn green.&lt;/p&gt;
	&lt;!-- This paragraph is actually a div; therefore, even though its language value 
	    is "en-us", it does not turn green. --&gt;
	&lt;div lang{{=}}"en-us"&gt;This div's language is set to "en-us", but this page's :lang 
	    pseudo-class only applies to paragraphs, so it doesn't turn green.&lt;/div&gt;
		
&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The set rules are applied when the value of ''C'' matches (or is a hyphen-separated substring of) the element's language value. The value of ''C'' should be a language code that is  indicated by [http://www.ietf.org/rfc/rfc3066.txt RFC3066: Tags for the Identification of Languages].
If ''C'' is empty or invalid, the selector will have no effect.
This pseudo-class requires that Windows Internet Explorer be in IE8 Standards mode or higher. For more information, see Defining Document 

Compatibility.
In Internet Explorer 10, the ''':lang(C)''' pseudo-class accepts a comma-separated list of language codes. However, because this behavior is based on an early draft of the World Wide Web Consortium (W3C)'s [http://dev.w3.org/csswg/selectors-4/#lang-pseudo Selectors Level 4] specification, you must add the "-ms-" vendor prefix to the pseudo-class to enable this functionality. In effect, the pseudo-class becomes ''':-ms-lang(C)'''. Following is an example of its usage:
 <code>html:-ms-lang(ar, dv, fa, he, ku-Arab, pa-Arab, prs, ps, sd-Arab, syr, ug, ur, qps-plocm) {
   direction: rtl;
 }
 </code>
In this example, the selector will match all of the listed language codes (and any corresponding hyphen-separated substrings of language codes). This example is equivalent to the following, which is the only way in which to achieve this functionality in versions of Windows Internet Explorer prior to Internet Explorer 10:
 <code>html:lang(ar), html:lang(dv), html:lang(fa), html:lang(he), html:lang(ku-Arab), html:lang(pa-Arab), html:lang(prs), html:lang(ps), html:lang(sd-Arab), html:lang(syr), html:lang(ug), html:lang(ur), html:lang(qps-plocm) {
   direction: rtl;
 }</code>
|Import_Notes=
===Syntax===
<code>
selector:lang(C) { /* ... */ }
</code>
===Parameters===
;''selector'':A CSS simple selector
;''C'':Language code as specified in [http://www.ietf.org/rfc/rfc3066.txt RFC3066: Tags for the Identification of Languages]
===Standards information===
*[http://www.w3.org/TR/CSS2/ CSS 2.1], Section 5.11.4
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Topic_clusters=Pseudo-Classes, Selectors
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
}}