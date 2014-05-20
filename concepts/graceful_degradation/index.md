{{Page_Title|Graceful Degradation}}
{{Flags
|High-level issues=Stub, Needs Flags, Needs Topics
|Checked_Out=No
}}
{{API_Name}}
{{Summary_Section|Graceful degradation, also known as '''Fault tolerance''' is a concept of building a web site or application so it provides a good level of user experience in modern browsers.}}
{{Concept_Page
|Content=However, it will degrade ''gracefully'' for those using older browsers. The system may not be as pleasant or as pretty, but the basic functionality will work on older systems.
<blockquote>
[..] Graceful Degradation (GD) is the journey from complexity to simplicity
</blockquote>
[http://www.smashingmagazine.com/2009/04/22/progressive-enhancement-what-it-is-and-how-to-use-it/ @smashingmag]
You start creating your website or web-application with the use of features that are available in the latest generation of modern browsers. Thereafter, have a look on older browsers and systems and start creating fallbacks by using [[concepts/polyfill|polyfills]] or other workarounds.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description='''Definition of Done:''' Create a videoplayer that is working on IE6 up to IE10.

Cause you trust the approach of GD, you prefer the  HTML5 <code><video></code> tag over Flash as your entry point. Now your videoplayer is works well on IE9 & 10. 
For you need to create a fallback for IE6-8, that does not support HTML5 Video. You'll now create another instance of your player based on Flash, which is a graceful replacement of your HTML5 player.
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|External_links=* [http://www.w3.org/wiki/Graceful_degredation_versus_progressive_enhancement W3C: Graceful degredation versus progressive enhancement]
* [http://en.wikipedia.org/wiki/Fault_tolerance  Wikipedia: Fault tolerance]
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}