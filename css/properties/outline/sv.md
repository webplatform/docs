---
title: Kontur (outline)
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/).'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
lang: sv
notes:
  - 'Not in English'
standardization_status: 'W3C Recommendation'
summary: 'Enheten outline i CSS är en regel för att ställa in en eller fler individuella konturregler outline-style, outline-width och outline-color i en enda regel. I de flesta fall är det föredraget och mer passande att använda denna enhet.'
tags:
  - CSS
  - Selectors
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/properties/outline/af
    - css/properties/outline/ar
    - css/properties/outline/ast
    - css/properties/outline/az
    - css/properties/outline/bcc
    - css/properties/outline/bg
    - css/properties/outline/br
    - css/properties/outline/ca
    - css/properties/outline/cs
    - css/properties/outline/da
    - css/properties/outline/de
    - css/properties/outline/diq
    - css/properties/outline/el
    - css/properties/outline/eo
    - css/properties/outline/es
    - css/properties/outline/fa
    - css/properties/outline/fi
    - css/properties/outline/fr
    - css/properties/outline/gl
    - css/properties/outline/gu
    - css/properties/outline/he
    - css/properties/outline/hu
    - css/properties/outline/hy
    - css/properties/outline/id
    - css/properties/outline/it
    - css/properties/outline/ja
    - css/properties/outline/ka
    - css/properties/outline/kk
    - css/properties/outline/km
    - css/properties/outline/ko
    - css/properties/outline/ksh
    - css/properties/outline/kw
    - css/properties/outline/mk
    - css/properties/outline/ml
    - css/properties/outline/mr
    - css/properties/outline/ms
    - css/properties/outline/nl
    - css/properties/outline/no
    - css/properties/outline/oc
    - css/properties/outline/pl
    - css/properties/outline/pt
    - css/properties/outline/pt-br
    - css/properties/outline/ro
    - css/properties/outline/ru
    - css/properties/outline/si
    - css/properties/outline/sk
    - css/properties/outline/sl
    - css/properties/outline/sq
    - css/properties/outline/sr
    - css/properties/outline/ta
    - css/properties/outline/th
    - css/properties/outline/tr
    - css/properties/outline/uk
    - css/properties/outline/vi
    - css/properties/outline/yue
    - css/properties/outline/zh
    - css/properties/outline/zh-hans
    - css/properties/outline/zh-hant
    - css/properties/outline/zh-tw
uri: css/properties/outline/sv

---
## <span>Summary</span>

Enheten outline i CSS är en regel för att ställa in en eller fler individuella konturregler outline-style, outline-width och outline-color i en enda regel. I de flesta fall är det föredraget och mer passande att använda denna enhet.

 Konturer skiljer sig från [kanter (borders)](/css/properties/border) på följande sätt:

-   Konturer tar inte upp någon plats, de ritas ut på elementet.
-   Konturer är inte alltid rektangulära. I Gecko/Firefox är de det. Internet Explorer försöker placera små konturer runt alla element och former som indikeras att ha en. Opera ritar ut en icke-rektangulär form runtom en konstruktion likt detta:

**Web<span style="font-size: xx-large;">Platform</span>Docs**

## <span>Examples</span>

Ta bort kontur när man för musen över en länk

``` css
a:hover { outline: 0; }
```

Vanligt användade av outline regeln

``` css
:focus { outline: solid; } /* outline-width och outline-color har sin standardiserade stil när outline-style inte är angiven */

:focus { outline: dashed red; } /* outline-style och outline-color */

:focus { outline: dashed 1px; } /* outline-style och outline-width */

:focus { outline: ridge thick violet; } /* outline-style, outline-width och outline-color */
```

## <span>Notes</span>

### <span>Tänk på att...</span>

En kontur ändrar inte flödet på sidan på något sätt, oavsett hur stor den är. Konturen ritas på elementet, och ändrar inte storleken och positionen av elementet, eller andra element. Denna enhet kräver att Windows Internet Explorer är i IE8 Standards-läge.

### <span>Syntax</span>

`outline:  [ <outline-width> || <outline-style> || <outline-color> ] | inherit`

### <span>Standards information</span>

-   [CSS 2.1](http://www.w3.org/TR/CSS2/ui.html#dynamic-outlines), Section 18.4

<table class="nmbox languages" style>
<tr>
<th class="mbox-image" style>
**Språk:**

</th>
<td class="mbox-text">
**[English](/css/properties/outline)**  • <span lang="sv">**svenska**</span>

</td>
</tr>
</table>
