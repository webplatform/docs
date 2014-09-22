{{Page_Title|regionfragmentchange}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Fires on the  [[apis/css-regions/NamedFlow|'''NamedFlow''']] object when there is a change in how content flows through a [[css/concepts/region_chain|region chain]].}}
{{Event
|Event_applies_to=apis/css-regions/NamedFlow
|Synchronous=No
|Bubbles=No
|Target=[[apis/css-regions/NamedFlow|'''NamedFlow''']]
|Cancelable=Yes
|Default_action=none
|Content=Fires on the [[apis/css-regions/NamedFlow|'''NamedFlow''']]
object when there is 'any' change in how content flows through a
[[css/concepts/region_chain|region chain]], even minor changes that don't affect the total number of
[[css/concepts/region|regions]] the content requires.
|Interface=UIEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This simple example logs each time content reflows among regions, and works with the CSS and JavaScript that follow. Define layout and content elements:
|Code=&lt;html>
&lt;body>
&lt;section class="page">
    &lt;div> &lt;h1>Region #1&lt;/h1> &lt;/div>
    &lt;div> &lt;h1>Region #2&lt;/h1> &lt;/div>
    &lt;aside>&lt;/aside>
&lt;/section>
&lt;article>
&lt;h1>Sample CSS Regions Layout&lt;/h1>
&lt;p>Riverrun, past Eve and Adam's, from swerve of shore to bend of bay, brings us by a commodius vicus of recirculation back to Howth Castle and Environs.&lt;/p>
&lt;p>...&lt;/p>
&lt;/article>
&lt;/body>
&lt;/html>
|LiveURL=http://letmespellitoutforyou.com/samples/region_fragmentchange.html
}}{{Single Example
|Language=CSS
|Description=Flow the content into the layout:
|Code=body { background: #aaa; }
article { flow-into: main; }

div {
    flow-from: main;
    region-fragment: break;
    top: 5%;
    width: 40%;
    height: 75%;
}

div, aside {
    position: absolute;
    background: #fff;    
    padding: 1em;
    border-radius: 1em;
}

aside {
    min-width: 40%;
    left: 5%;
    top: 90%;
}

div:first-of-type { left: 5%; }
div:last-of-type { left: 55%; }
|LiveURL=http://letmespellitoutforyou.com/samples/region_fragmentchange.html
}}{{Single Example
|Language=JavaScript
|Description=Log to console any shifts of content from one region to another that result when resizing the window, and thus the layout elements.
|Code=document.getNamedFlows().namedItem('main').addEventListener(
    'regionfragmentchange',
    function() { console.log(inc++); }
);
|LiveURL=http://letmespellitoutforyou.com/samples/region_fragmentchange.html
}}
}}
{{Notes_Section
|Usage=
|Notes=The event fires when content shifts 'in any way' within the
[[css/concepts/region_chain|region chain]], such as when linebreaks change. That is, when any
[[css/concepts/region|region's]] [[apis/css-regions/Region/getRegionFlowRanges|collection of
DOM Range fragments]] changes their dimensions or offsets.  (Compare
with the
[[apis/css-regions/NamedFlow/regionoversetchange|'''regionoversetchange''']]
event, which fires much less frequently in response to changing
content or dimensions.)
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Regions Module Level 1
|URL=http://www.w3.org/TR/css3-regions/
|Status=W3C Working Draft
|Relevant_changes=
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
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
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=534
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=
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
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=537
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Regions
|Manual_links=
|External_links=* W3C editor's draft: [http://dev.w3.org/csswg/css3-regions/ CSS Regions Module Level 3]
* Adobe Web Standards: [http://html.adobe.com/webstandards/cssregions CSS Regions]
* Adobe Developer's Network: [http://www.adobe.com/devnet/html5/articles/css3-regions.html CSS3 Regions: Rich page layout with HTML and CSS3]
* [http://adobe.github.com/web-platform/samples/css-regions Sample pages]
|Manual_sections=
}}
{{Topics|API, CSS, CSS-Regions}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}