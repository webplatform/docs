{{Page_Title|Grunderna i HTML}}
{{Flags
|High-level issues=Stub
|Content=Incomplete
|Checked_Out=Yes
}}
{{Byline}}
{{Summary_Section|I denna artikel kommer du lära dig grunderna i HTML för att få en uppfattning om strukturen och innehållet av ett HTML dokument.}}
{{Guide
|Content=== Introduktion ==

Denna artikel sammanfattar avsikten och strukturen av HTML på hög nivå. Den kommer bland annat att ta upp hur element fungerar samt vad de olika karaktärerna fyller för funktion i språket. Artiklarna som nedan följer kommer ge dig en detaljrik djupdykning i specifika delar av språket HTML.

== Vad HTML är ==

De flesta program som du använder vanligtvis på skrivbordet använder speciella filformat. Ett exempel, Microsoft Word använder ".doc" filer och Microsoft Excel använder ".xls". Dessa filer innehåller den information som programmet behöver för att åter visa dokumenten när du öppnar dem. Filen innehåller bland annat all information du lagt in, dess "metadata" och datumet dokumentet senast redigerades.

HTML ("Hypertext Markup Language") är ett så kallat sidbeskrivningsspråk. Det används för att ange innehållet av ett webbdokument. Språket använder ett speciellt syntax som har en typ av markörer (kallade "element") vilka sätts runtom text i dokumentet för att beskriva för användaragenter (t.ex. webbläsare) hur de skall tolka den delen av dokumentet.

En användaragent är en mjukvara som används för att åtkomma hemsidor å användarens vägnar. Det är viktigt att påpeka—alla typer av webbläsare för skrivbordet (Internet Explorer, Opera, Firefox, Safari, Chrome osv.) samt webbläsare för andra enheter (såsom Wii Internet Channel och mobila webbläsare som Opera Mini och WebKit för iPhone) är användaragenter, men alla användaragenter är inte webbläsarmjukvara. De automatiserade program som Google och Yahoo! använder för att indexera webben för sina sökmotorer är också användaragenter, men ingen människa kontrollerar dem.

== Hur HTML ser ut ==

HTML är helt enkelt bara en representativ text med innehåll och dess innebörd. Till exempel:

<syntaxhighlight lang="html5"><p id="exempel">Detta är en paragraf.</p></syntaxhighlight>

"<code>&lt;p&gt;</code>" i texten ovan är en markör (som vi kommer kalla en "tagg") som berättar att "det som följer skall tolkas som en paragraf". Eftersom taggen är i början av det innehåll som sedan följer, så kallas denna tagg en "starttagg". Vi behöver även en så kallad "sluttagg". Den ser ut såhär: "<code>&lt;p&gt;</code>". Taggarna och allt däremellan är vad vi kallar ett "element". Delen i den första taggen som lyder id="exempel" är ett attribut; du kommer få lära dig om dessa som småningom. Det finns många som använder termerna "tagg" och "element" som om det vore samma sak, vilket inte är helt korrekt.

I de flesta webbläsare finns en "Visa sidkälla", eller liknande, alternativ. Detta hittar du vanligtvis i "View" menyn. Testa denna funktion - gå till en sida du gillar, använd detta verktyg, och spendera lite tid och skumma igenom den HTML kod som uppgör strukturen för sidan.

== Strukturen av ett HTML dokument ==

Ett typiskt exempel av ett HTML dokument ser ut såhär:

<syntaxhighlight lang="html5"><!DOCTYPE html>
<html lang="sv">
	<head>
		<meta charset="utf-8">
		<title>Exempel sida</title>
	</head>
	<body>
		<h1>Hej världen</h1>
	</body>
</html>
</syntaxhighlight>

När du tittar på detta dokument i en webbläsare kommer det se ut såhär:

[[File:HTMLrender_sv.png]]

Början av dokumentet har ett dokumenttyp element, kallat doctype. Denna deklaration i dokumentet gör så att webbläsare renderar HTML i vad som kallas "standardläge", så att det fungerar korrekt. Den hjälper även validerings verktyg att se vilken version av HTML de skall validera emot. Oroa dig inte över vad allt detta har för mening för tillfället. Vi återkommer till det här senare. Det vi använder här är dokumenttypen HTML5.

Efter detta, så kan du se starttaggen till <code>html</code> elementet. Denna fungerar som en wrapper runt hela dokumentet. Sluttaggen till <code>html</code> elementet är det sista som skall finnas i varje HTML dokument. Elementet bär alltid ha ett <code>lang</code>-attribut. Detta anger det primära språket för sidan. Till exempel, <code>sv</code> betyder "Svenska", <code>en</code> betyder "Engelska". Det finns verktyg som hjälper dig hitta rätt språkkod, såsom Richard Ishidas [http://rishida.net/utils/subtags/ Language Subtag Lookup tool].
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Languages|guides/the_basics_of_html}}









{{API_Name}}


{{Examples_Section
|Not_required=Yes
|Examples=
}}

{{Related_Specifications_Section
|Specifications=
}}