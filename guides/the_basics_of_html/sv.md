---
title: sv
tags:
  - Guides
  - HTML
summary: 'I denna artikel kommer du lära dig grunderna i HTML för att få en uppfattning om strukturen och innehållet av ett HTML dokument.'
uri: 'guides/the basics of html/sv'
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'guides/the basics of html/af'
    - 'guides/the basics of html/ar'
    - 'guides/the basics of html/ast'
    - 'guides/the basics of html/az'
    - 'guides/the basics of html/bcc'
    - 'guides/the basics of html/bg'
    - 'guides/the basics of html/br'
    - 'guides/the basics of html/ca'
    - 'guides/the basics of html/cs'
    - 'guides/the basics of html/da'
    - 'guides/the basics of html/de'
    - 'guides/the basics of html/diq'
    - 'guides/the basics of html/el'
    - 'guides/the basics of html/eo'
    - 'guides/the basics of html/fa'
    - 'guides/the basics of html/fi'
    - 'guides/the basics of html/fr'
    - 'guides/the basics of html/gl'
    - 'guides/the basics of html/gu'
    - 'guides/the basics of html/he'
    - 'guides/the basics of html/hu'
    - 'guides/the basics of html/hy'
    - 'guides/the basics of html/id'
    - 'guides/the basics of html/it'
    - 'guides/the basics of html/ka'
    - 'guides/the basics of html/kk'
    - 'guides/the basics of html/km'
    - 'guides/the basics of html/ksh'
    - 'guides/the basics of html/kw'
    - 'guides/the basics of html/mk'
    - 'guides/the basics of html/ml'
    - 'guides/the basics of html/mr'
    - 'guides/the basics of html/ms'
    - 'guides/the basics of html/nl'
    - 'guides/the basics of html/no'
    - 'guides/the basics of html/oc'
    - 'guides/the basics of html/pl'
    - 'guides/the basics of html/pt'
    - 'guides/the basics of html/pt-br'
    - 'guides/the basics of html/ro'
    - 'guides/the basics of html/ru'
    - 'guides/the basics of html/si'
    - 'guides/the basics of html/sk'
    - 'guides/the basics of html/sl'
    - 'guides/the basics of html/sq'
    - 'guides/the basics of html/sr'
    - 'guides/the basics of html/ta'
    - 'guides/the basics of html/th'
    - 'guides/the basics of html/tr'
    - 'guides/the basics of html/uk'
    - 'guides/the basics of html/vi'
    - 'guides/the basics of html/yue'
    - 'guides/the basics of html/zh'
    - 'guides/the basics of html/zh-hans'
    - 'guides/the basics of html/zh-hant'
    - 'guides/the basics of html/zh-tw'

---
# Grunderna i HTML

## Summary

I denna artikel kommer du lära dig grunderna i HTML för att få en uppfattning om strukturen och innehållet av ett HTML dokument.

## Introduktion

Denna artikel sammanfattar avsikten och strukturen av HTML på hög nivå. Den kommer bland annat att ta upp hur element fungerar samt vad de olika karaktärerna fyller för funktion i språket. Artiklarna som nedan följer kommer ge dig en detaljrik djupdykning i specifika delar av språket HTML.

## Vad HTML är

De flesta program som du använder vanligtvis på skrivbordet använder speciella filformat. Ett exempel, Microsoft Word använder ".doc" filer och Microsoft Excel använder ".xls". Dessa filer innehåller den information som programmet behöver för att åter visa dokumenten när du öppnar dem. Filen innehåller bland annat all information du lagt in, dess "metadata" och datumet dokumentet senast redigerades.

HTML ("Hypertext Markup Language") är ett så kallat sidbeskrivningsspråk. Det används för att ange innehållet av ett webbdokument. Språket använder ett speciellt syntax som har en typ av markörer (kallade "element") vilka sätts runtom text i dokumentet för att beskriva för användaragenter (t.ex. webbläsare) hur de skall tolka den delen av dokumentet.

En användaragent är en mjukvara som används för att åtkomma hemsidor å användarens vägnar. Det är viktigt att påpeka—alla typer av webbläsare för skrivbordet (Internet Explorer, Opera, Firefox, Safari, Chrome osv.) samt webbläsare för andra enheter (såsom Wii Internet Channel och mobila webbläsare som Opera Mini och WebKit för iPhone) är användaragenter, men alla användaragenter är inte webbläsarmjukvara. De automatiserade program som Google och Yahoo! använder för att indexera webben för sina sökmotorer är också användaragenter, men ingen människa kontrollerar dem.

## Hur HTML ser ut

HTML är helt enkelt bara en representativ text med innehåll och dess innebörd. Till exempel:

``` {.html}
<p id="exempel">Detta är en paragraf.</p>
```

 "`<p>`" i texten ovan är en markör (som vi kommer kalla en "tagg") som berättar att "det som följer skall tolkas som en paragraf". Eftersom taggen är i början av det innehåll som sedan följer, så kallas denna tagg en "starttagg". Vi behöver även en så kallad "sluttagg". Den ser ut såhär: "`<p>`". Taggarna och allt däremellan är vad vi kallar ett "element". Delen i den första taggen som lyder id="exempel" är ett attribut; du kommer få lära dig om dessa som småningom. Det finns många som använder termerna "tagg" och "element" som om det vore samma sak, vilket inte är helt korrekt.

I de flesta webbläsare finns en "Visa sidkälla", eller liknande, alternativ. Detta hittar du vanligtvis i "View" menyn. Testa denna funktion - gå till en sida du gillar, använd detta verktyg, och spendera lite tid och skumma igenom den HTML kod som uppgör strukturen för sidan.

## Strukturen av ett HTML dokument

Ett typiskt exempel av ett HTML dokument ser ut såhär:

``` {.html}
<!DOCTYPE html>
<html lang="sv">
    <head>
        <meta charset="utf-8">
        <title>Exempel sida</title>
    </head>
    <body>
        <h1>Hej världen</h1>
    </body>
</html>
```

 När du tittar på detta dokument i en webbläsare kommer det se ut såhär:

![HTMLrender sv.png](/assets/public/e/e2/HTMLrender_sv.png)

Början av dokumentet har ett dokumenttyp element, kallat doctype. Denna deklaration i dokumentet gör så att webbläsare renderar HTML i vad som kallas "standardläge", så att det fungerar korrekt. Den hjälper även validerings verktyg att se vilken version av HTML de skall validera emot. Oroa dig inte över vad allt detta har för mening för tillfället. Vi återkommer till det här senare. Det vi använder här är dokumenttypen HTML5.

Efter detta, så kan du se starttaggen till `html` elementet. Denna fungerar som en wrapper runt hela dokumentet. Sluttaggen till `html` elementet är det sista som skall finnas i varje HTML dokument. Elementet bär alltid ha ett `lang`-attribut. Detta anger det primära språket för sidan. Till exempel, `sv` betyder "Svenska", `en` betyder "Engelska". Det finns verktyg som hjälper dig hitta rätt språkkod, såsom Richard Ishidas [Language Subtag Lookup tool](http://rishida.net/utils/subtags/).

**Språk:**
:   **[English](/guides/the_basics_of_html)**  • <span lang="es">[español](/guides/the_basics_of_html/es)</span> • <span lang="ja">[日本語](/guides/the_basics_of_html/ja)</span> • <span lang="ko">[한국어](/guides/the_basics_of_html/ko)</span> • <span lang="sv">**svenska**</span>

