{{Page_Title|Kontur (outline)}}
{{Flags
|High-level issues=Missing Relevant Sections
|Content=Incomplete, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Enheten <code>outline</code> i CSS är en regel för att ställa in en eller fler individuella konturregler [[css/properties/outline-style|outline-style]], [[css/properties/outline-width|outline-width]] och [[css/properties/outline-color|outline-color]] i en enda regel. I de flesta fall är det föredraget och mer passande att använda denna enhet.}}
{{CSS_Selector
|Content=Konturer skiljer sig från [[css/properties/border|kanter (borders)]] på följande sätt:

* Konturer tar inte upp någon plats, de ritas ut på elementet.
* Konturer är inte alltid rektangulära. I Gecko/Firefox är de det. Internet Explorer försöker placera små konturer runt alla element och former som indikeras att ha en. Opera ritar ut en icke-rektangulär form runtom en konstruktion likt detta:

<strong style="color: green; outline: 1px dotted;">Web<span style="font-size: xx-large;">Platform</span>Docs</strong>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Ta bort kontur när man för musen över en länk
|Code=a:hover { outline: 0; }
}}{{Single Example
|Language=CSS
|Description=Vanlig användade av outline regeln
|Code=:focus { outline: solid; } /* outline-width och outline-color har sin standardiserade stil när outline-style inte är angiven */

:focus { outline: dashed red; } /* outline-style och outline-color */

:focus { outline: dashed 1px; } /* outline-style och outline-width */

:focus { outline: ridge thick violet; } /* outline-style, outline-width och outline-color */
}}
}}
{{Notes_Section
|Notes====Tänk på att...===
En kontur ändrar inte flödet på sidan på något sätt, oavsett hur stor den är. Konturen ritas på elementet, och ändrar inte storleken och positionen av elementet, eller andra element.
Denna enhet kräver att Windows Internet Explorer är i
IE8 Standards-läge.
|Import_Notes====Syntax===
<code>outline:  [ &lt;outline-width&gt; {{!}}{{!}} &lt;outline-style&gt; {{!}}{{!}} &lt;outline-color&gt; ] {{!}} inherit</code>

===Standards information===
*[http://www.w3.org/TR/CSS2/ui.html#dynamic-outlines CSS 2.1], Section 18.4
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
|Topic_clusters=Visuella Effekter
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}

{{Languages|css/properties/outline}}