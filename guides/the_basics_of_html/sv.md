== Introduktion ==

Denna artikel sammanfattar avsikten och strukturen av HTML på hög nivå. Den kommer bland annat att ta upp hur element fungerar samt vad de olika karaktärerna fyller för funktion i språket. Artiklarna som nedan följer kommer ge dig en detaljrik djupdykning i specifika delar av språket HTML.

== Vad HTML är ==

De flesta program som du använder vanligtvis på skrivbordet använder speciella filformat. Ett exempel, Microsoft Word använder “.doc” filer och Microsoft Excel använder “.xls”. Dessa filer innehåller den information som programmet behöver för att åter visa dokumenten när du öppnar dem. Filen innehåller bland annat all information du lagt in, dess "metadata" och datumet dokumentet senast redigerades.

HTML (“Hypertext Markup Language”) är ett så kallat sidbeskrivningsspråk. Det används för att ange innehållet av ett webbdokument. Språket använder ett speciellt syntax som har en typ av markörer (kallade “element”) vilka sätts runtom text i dokumentet för att beskriva för användaragenter (t.ex. webbläsare) hur de skall tolka den delen av dokumentet.

En användaragent är en mjukvara som används för att åtkomma hemsidor å användarens vägnar. Det är viktigt att påpeka—alla typer av webbläsare för skrivbordet (Internet Explorer, Opera, Firefox, Safari, Chrome osv.) samt webbläsare för andra enheter (såsom Wii Internet Channel och mobila webbläsare som Opera Mini och WebKit för iPhone) är användaragenter, men alla användaragenter är inte webbläsarmjukvara. De automatiserade program som Google och Yahoo! använder för att indexera webben för sina sökmotorer är också användaragenter, men ingen människa kontrollerar dem.

== Hur HTML ser ut ==

HTML är helt enkelt bara en representativ text med innehåll och dess innebörd. Till exempel:

<syntaxhighlight lang="html5"><p id="exempel">Detta är en paragraf.</p></syntaxhighlight>

“<code>&lt;p&gt;</code>” i texten ovan är en markör (som vi kommer kalla en “tagg”) som berättar att “det som följer skall tolkas som en paragraf”. Eftersom taggen är i början av det innehåll som sedan följer så behöver vi en så kallad “sluttagg”. Detta är “<code>&lt;p&gt;</code>”. Taggarna och allt däremellan är vad vi kallar ett “element”. Delen i den första taggen som lyder id="exempel" är ett attribut; du kommer få lära dig om dessa som småningom. Det finns många som använder termerna “tagg” och “element” som om det vore samma sak, vilket inte är helt korrekt.

I de flesta webbläsare finns en “Visa sidkälla”, eller liknande, alternativ. Detta hittar du vanligtvis i “View” menyn. Testa denna funktion - gå till en sida du gillar, använd detta verktyg, och spendera lite tid och skumma igenom den HTML kod som uppgör strukturen för sidan.