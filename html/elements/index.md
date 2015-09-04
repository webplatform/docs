---
title: elements
tags:
  - API
  - Listings
  - DOM
  - HTML
standardization_status: 'W3C Working Draft'
notes:
  - 'Make sure that all child element pages are ready before setting a status'
summary: 'Index page for HTML elements.'
uri: html/elements
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - SGML
    - XML
    - webpage
    - 'Document Type Definition'
    - HTML
    - Serialization
    - 'Markup language'
    - 'html/Quirks mode'
    - html/elements/frameset
    - html/elements/noScript
    - html/elements/nextid
    - html/elements/nobr
    - html/elements/spacer
    - html/elements/bgsound
    - html/elements/math
    - html/elements/noframes
    - html/elements/noembed
    - html/elements/plaintext
    - html/elements/svg
    - html/elements/summary
    - html/elements/command
    - html/elements/c
    - html/elements/isindex
    - html/training
    - 'html/new html5 elements'

---
# HTML Elements

## Summary

Index page for HTML elements.

API Name
:   Summary
[!DOCTYPE](/html/elements/!DOCTYPE)
:   A **Document Type Declaration**, or **DOCTYPE**, is an instruction that associates a particular [SGML](/w/index.php?title=SGML&action=edit&redlink=1) or [XML](/w/index.php?title=XML&action=edit&redlink=1) document (for example, a [webpage](/w/index.php?title=webpage&action=edit&redlink=1)) with a [Document Type Definition](/w/index.php?title=Document_Type_Definition&action=edit&redlink=1) (DTD) (for example, the formal definition of a particular version of [HTML](/w/index.php?title=HTML&action=edit&redlink=1)). In the [serialized](/w/index.php?title=Serialization&action=edit&redlink=1) form of the document, it manifests as a short string of [markup](/w/index.php?title=Markup_language&action=edit&redlink=1) that conforms to a particular syntax. Not including \<!DOCTYPE\> may trigger [Quirks mode](/w/index.php?title=html/Quirks_mode&action=edit&redlink=1).
[a](/html/elements/a)
:   Defines a hyperlink, a destination of hyperlink, or both.
[acronym](/html/elements/acronym)
:   This element is **deprecated** in HTML5, in favor of the [abbr](/html/elements/abbr) element. It should no longer be used.

    The `acronym` element indicated an abbreviation or a word formed by the initial letter or letters (or major parts) of a compound term, like NATO, radar or Interpol.

[address](/html/elements/address)
:   The **address** element (\<address\>) encloses contact information of the owner or the author of the document or the article.
[applet – obsolete](/html/elements/applet)
:   The **applet** element (\<applet\>) embeds a Java applet into a web page.
[area](/html/elements/area)
:   Represents either a hyperlink with some text and a corresponding area on an image map, or a dead area on an image map.
[article](/html/elements/article)
:   The **article** element (\<article\>) defines a self-contained composition within a page.
[aside](/html/elements/aside)
:   The **aside** element (\<aside\>) indicates content that is only tangentially related to the rest of the content.
[audio](/html/elements/audio)
:   The **audio** element (\<audio\>) is used for playing audio files and may display a minimal media player user interface.
[b](/html/elements/b)
:   The **b** element represents a span of text to be stylistically offset from the normal prose without conveying any extra importance.
[base](/html/elements/base)
:   The **base** element is used to specify a document's base URL and base target that is used for resolving URI references (relative URLs) within the document.
[basefont](/html/elements/basefont)
:   The `basefont` element (`<basefont>`) allows specifying a default `color` and `font-size` for text on the entire page.

    The `basefont` element was deprecated in HTML4 and should no longer be used.

[bdo](/html/elements/bdo)
:   The **bdo** element (\<bdo\>) allows you to specify the direction in which text is to be rendered on the page. ("BDO" stands for Bi-Directional Override.)
[bgSound](/html/elements/bgSound)
:   The **bgsound** element (`<bgsound>`) instructs the browser to load and play a sound file while the user is on that page. Don't use it. Use the [audio](/html/elements/audio) element instead.
[big](/html/elements/big)
:   The **big** element (\<big\>) indicates that the enclosed text should be display in a larger font size than surrounding text.

    This element is considered obsolete in HTML5. Use CSS instead.

[blockquote](/html/elements/blockquote)
:   The **blockquote** element indicates an extended quotation.
[body](/html/elements/body)
:   The **body** element (\<body\>) represents the main content of the document.
[br](/html/elements/br)
:   The line break element, **br**, forces the current line of text to end and the text that follows it will being on a new line.
[button](/html/elements/button)
:   The **button** element represents a clickable button.
[canvas](/html/elements/canvas)
:   The **canvas** element (\<canvas\>) provides scripts with a resolution-dependent bitmap canvas, which can be used for rendering graphs, game graphics, or other visual images on the fly, by using the [associated canvas API](/apis/canvas).
[caption](/html/elements/caption)
:   The **caption** (\<caption\>) element represents the title of the table that is its parent.
[center](/html/elements/center)
:   The `<center>` element center-aligns text in an HTML page. The element is deprecated in HTML 4.01 and obsolete in HTML5. Use CSS instead.
[cite](/html/elements/cite)
:   The **cite** element represents a reference to a creative work.
[code](/html/elements/code)
:   The **code** element specifies a fragment of computer code.
[col](/html/elements/col)
:   The **col** element (\<col\>) specifies properties for each column within a [\<colgroup\>](/html/elements/colgroup) element in a [\<table\>](/html/elements/table).
[colgroup](/html/elements/colgroup)
:   The **colgroup** element (\<colgroup\>) specifies a group of one or more columns in a table for formatting.

    This element is useful for applying properties to entire columns, instead of repeating the properties for each cell, for each row.

[custom](/html/elements/custom)
:   Represents a user-defined HTML tag (nonstandard)
[datalist](/html/elements/datalist)
:   The **datalist** element (\<datalist\>) represents a set of [\<option\>](/html/elements/option) elements that represent predefined options for other controls. It may be associated with an [\<input\>](/html/elements/input) element by adding a list attribute to the input element.
[dd – description list data](/html/elements/dd)
:   The **dd** element represents the description, definition, or value, part of a term-description group in a definition list ([**dl**](/html/elements/dl)).

    A [**dt**](/html/elements/dt) (topic) is usually followed by one or more [**dd**](/html/elements/dd) (definition) elements. Several consecutive [**dt**](/html/elements/dt) are attributed to the [**dd**](/html/elements/dd) element that immediately follows the group.

[del](/html/elements/del)
:   The **del** element indicates text that has been deleted from the document.
[dfn](/html/elements/dfn)
:   The **dfn** element indicates the defining instance of a term.
[dir](/html/elements/dir)
:   The **dir** element `<dir>` is used to list directory titles.

    The **dir** element is deprecated in HTML 4.01, and obsolete in HTML5. Use CSS and the [**ul** element](/html/elements/ul) instead.

[div](/html/elements/div)
:   The **div** element (\<div\>) is a generic block-level container that has no semantic value other than the one that you give it via `id` or `class` attributes. It can be used for a variety of purposes including the styling of common elements, or for grouping elements with common attributes.
[dl – description list](/html/elements/dl)
:   The **dl** element is used to define a **description list**. The element encloses one or more **description terms**, enclosed in [**dt**](/html/elements/dt) elements, and **description definitions** (definitions of the terms), enclosed within [**dd**](/html/elements/dd) elements.
[dt – description list topic](/html/elements/dt)
:   The **dt** element indicates a definition term within a definition list ([**dl**](/html/elements/dl)).

    A [**dt**](/html/elements/dt) (topic) is usually followed by one or more [**dd**](/html/elements/dd) (definition) elements. Several consecutive [**dt**](/html/elements/dt) are attributed to the [**dd**](/html/elements/dd) element that immediately follows the group.

[em](/html/elements/em)
:   The **em** element indicates text that has emphasis.
[EMBED](/html/elements/embed)
:   The HTML \<embed\> Element represents an integration point for an external content- typically, non-HTML content such as an application or some other type of interactive content which involves use of a third-party plugin as a handler (rather than being natively supported by the UA).
[fieldset](/html/elements/fieldset)
:   The **fieldset** element is used to group related fields within a form.
[figcaption](/html/elements/figcaption)
:   The **figcaption** (\<figcaption\>) defines a caption or legend for a figure element.

    This element is new in HTML5.

[figure](/html/elements/figure)
:   The **figure** element (\<figure\>) represents self-contained content (such as an image), optionally with a caption, that can be referenced as a single unit from the main content of the document.
[font](/html/elements/font)
:   The **font** element is an obsolete tag that was used to specify the typeface, size, and color of the text it contained.
[footer](/html/elements/footer)
:   The **footer** element (\<footer\>) represents content of the end of the nearest ancestor sectioning content or sectioning root element.
[form](/html/elements/form)
:   The **form** element (\<form\>) defines an HTML form for user input, subsequently to be submitted to a website or service.
[frame](/html/elements/frame)
:   The **frame** element (\<frame\>) defines one particular window (frame) within a [\<frameSet\>](/w/index.php?title=html/elements/frameset&action=edit&redlink=1).

    The \<frame\> element is obsolete in HTML5.

[frameSet](/html/elements/frameSet)
:   The **frameset** element (\<frameset\>) defines a collection of frames.

    The \<frameset\> element holds one or more [\<frame\>](/html/elements/frame) elements. Each \<frame\> element can hold a separate document. The \<frameset\> tag is obsolete in HTML5.

[head](/html/elements/head)
:   The **head** element (\<head\>) represents a collection of metadata for the document.
[header](/html/elements/header)
:   The **header** element (\<header\>) represents the header of a section: a group of introductory or navigational aids.
[hgroup](/html/elements/hgroup)
:   (Obsolete) The **hgroup** element (\<hgroup\>) is typically used to group a set of one or more h1-h6 elements — to group, for example, a section title and an accompanying subtitle. The **hgroup** element (\<hgroup\>) element is obsolete in HTML5.
[hn](/html/elements/hn)
:   The **h1** through **h6** elements define levels of headings within a document.
[hr](/html/elements/hr)
:   The **hr** element represents a paragraph-level thematic break in text.

<!-- -->

    See more pages...

## See also

### Related articles

#### HTML

-   [user-modify](/css/properties/user-modify)

-   [HTMLAudioElement](/dom/HTMLAudioElement)

-   [textLength](/dom/HTMLTextAreaElement/textLength)

-   [value](/dom/HTMLTextAreaElement/value)

-   [accept](/html/attributes/accept)

-   [action](/html/attributes/action)

-   [alt](/html/attributes/alt)

-   [autocomplete](/html/attributes/autocomplete)

-   [autofocus](/html/attributes/autofocus)

-   [checked](/html/attributes/checked)

-   [crossorigin](/html/attributes/crossorigin)

-   [form](/html/attributes/form)

-   [formEnctype](/html/attributes/formEnctype)

-   [height](/html/attributes/height)

-   [list](/html/attributes/list)

-   [max (HTMLInputElement)](/html/attributes/max_(HTMLInputElement))

-   [maxLength](/html/attributes/maxLength)

-   [min](/html/attributes/min)

-   [multiple](/html/attributes/multiple)

-   [readonly](/html/attributes/readonly)

-   [size](/html/attributes/size)

-   [standby](/html/attributes/standby)

-   [step](/html/attributes/step)

-   **HTML Elements**

-   [!DOCTYPE](/html/elements/!DOCTYPE)

-   [!DOCTYPE](/html/elements/!DOCTYPE/ja)

-   [acronym](/html/elements/acronym)

-   [b](/html/elements/b)

-   [b](/html/elements/b/ja)

-   [br](/html/elements/br)

-   [br](/html/elements/br/ja)

-   [button](/html/elements/button)

-   [button](/html/elements/button/ja)

-   [caption](/html/elements/caption)

-   [cite](/html/elements/cite)

-   [code](/html/elements/code)

-   [col](/html/elements/col)

-   [colgroup](/html/elements/colgroup)

-   [datalist](/html/elements/datalist)

-   [del](/html/elements/del)

-   [dfn](/html/elements/dfn)

-   [div](/html/elements/div)

-   [em](/html/elements/em)

-   [EMBED](/html/elements/embed)

-   [fieldset](/html/elements/fieldset)

-   [font](/html/elements/font)

-   [footer](/html/elements/footer)

-   [head](/html/elements/head)

-   [hn](/html/elements/hn)

-   [hr](/html/elements/hr)

<!-- -->

    … further results

This is the list of HTML and related Elements from the past to the present.

## The root element

-   [html](/html/elements/html)

## Document metadata

-   [head](/html/elements/head)
-   [title](/html/elements/title)
-   [base](/html/elements/base)
-   [isIndex](/html/elements/isIndex)
-   [link](/html/elements/link)
-   [meta](/html/elements/meta)
-   [style](/html/elements/style)

## Scripting

-   [script](/html/elements/script)
-   [noscript](/w/index.php?title=html/elements/noScript&action=edit&redlink=1)

## Sections

-   [body](/html/elements/body)
-   [section](/html/elements/section)
-   [nav](/html/elements/nav)
-   [article](/html/elements/article)
-   [aside](/html/elements/aside)
-   [h1, h2, h3, h4, h5, and h6](/html/elements/hn)
-   [hgroup](/html/elements/hgroup)
-   [header](/html/elements/header)
-   [footer](/html/elements/footer)
-   [address](/html/elements/address)

## Grouping content

-   [p](/html/elements/p)
-   [hr](/html/elements/hr)
-   [pre](/html/elements/pre)
-   [blockquote](/html/elements/blockquote)
-   [ol](/html/elements/ol)
-   [ul](/html/elements/ul)
-   [li](/html/elements/li)
-   [dl](/html/elements/dl)
-   [dt](/html/elements/dt)
-   [dd](/html/elements/dd)
-   [figure](/html/elements/figure)
-   [figcaption](/html/elements/figcaption)
-   [div](/html/elements/div)
-   [main](/html/elements/main)
-   [center](/html/elements/center)

## Text-level semantics

-   [a](/html/elements/a)
-   [abbr](/html/elements/abbr)
-   [acronym](/html/elements/acronym)
-   [b](/html/elements/b)
-   [basefont](/html/elements/basefont)
-   [bdo](/html/elements/bdo)
-   [big](/html/elements/big)
-   [blink](/html/elements/blink)
-   [br](/html/elements/br)
-   [cite](/html/elements/cite)
-   [code](/html/elements/code)
-   [dfn](/html/elements/dfn)
-   [em](/html/elements/em)
-   [font](/html/elements/font)
-   [i](/html/elements/i)
-   [kbd](/html/elements/kbd)
-   [listing](/html/elements/listing)
-   [mark](/html/elements/mark)
-   [marquee](/html/elements/marquee)
-   [nextid](/w/index.php?title=html/elements/nextid&action=edit&redlink=1)
-   [nobr](/w/index.php?title=html/elements/nobr&action=edit&redlink=1)
-   [q](/html/elements/q)
-   [rp](/html/elements/rp)
-   [rt](/html/elements/rt)
-   [ruby](/html/elements/ruby)
-   [s](/html/elements/s)
-   [samp](/html/elements/samp)
-   [small](/html/elements/small)
-   [spacer](/w/index.php?title=html/elements/spacer&action=edit&redlink=1)
-   [span](/html/elements/span)
-   [strike](/html/elements/strike)
-   [strong](/html/elements/strong)
-   [sub](/html/elements/sub), [sup](/html/elements/sup)
-   [time](/html/elements/time)
-   [tt](/html/elements/tt)
-   [u](/html/elements/u)
-   [var](/html/elements/var)
-   [wbr](/html/elements/wbr)
-   [xmp](/html/elements/xmp)

## Edits

-   [ins](/html/elements/ins)
-   [del](/html/elements/del)

## Embedded content

-   [applet](/html/elements/applet)
-   [area](/html/elements/area)
-   [audio](/html/elements/audio)
-   [bgsound](/w/index.php?title=html/elements/bgsound&action=edit&redlink=1)
-   [canvas](/html/elements/canvas)
-   [embed](/html/elements/embed)
-   [frame](/html/elements/frame)
-   [frameset](/w/index.php?title=html/elements/frameset&action=edit&redlink=1)
-   [img](/html/elements/img)
-   [iframe](/html/elements/iframe)
-   [map](/html/elements/map)
-   [math](/w/index.php?title=html/elements/math&action=edit&redlink=1)
-   [noframes](/w/index.php?title=html/elements/noframes&action=edit&redlink=1)
-   [noembed](/w/index.php?title=html/elements/noembed&action=edit&redlink=1)
-   [object](/html/elements/object)
-   [param](/html/elements/param)
-   [picture](/html/elements/picture)
-   [plaintext](/w/index.php?title=html/elements/plaintext&action=edit&redlink=1)
-   [source](/html/elements/source)
-   [svg](/w/index.php?title=html/elements/svg&action=edit&redlink=1)
-   [track](/html/elements/track)
-   [video](/html/elements/video)

## Tables

-   [table](/html/elements/table)
-   [caption](/html/elements/caption)
-   [colgroup](/html/elements/colgroup)
-   [col](/html/elements/col)
-   [tbody](/html/elements/tbody)
-   [thead](/html/elements/thead)
-   [tfoot](/html/elements/tfoot)
-   [tr](/html/elements/tr)
-   [td](/html/elements/td)
-   [th](/html/elements/th)

## Forms

-   [form](/html/elements/form)
-   [fieldset](/html/elements/fieldset)
-   [legend](/html/elements/legend)
-   [label](/html/elements/label)
-   [input](/html/elements/input)
-   [button](/html/elements/button)
-   [select](/html/elements/select)
-   [datalist](/html/elements/datalist)
-   [optgroup](/html/elements/optgroup)
-   [option](/html/elements/option)
-   [textarea](/html/elements/textarea)
-   [keygen](/html/elements/keygen)
-   [output](/html/elements/output)
-   [progress](/html/elements/progress)
-   [meter](/html/elements/meter)

## Interactive

-   [details](/html/elements/details)
-   [summary](/w/index.php?title=html/elements/summary&action=edit&redlink=1)
-   [command](/w/index.php?title=html/elements/command&action=edit&redlink=1)
-   [menu](/html/elements/menu)

## Previous HTML Elements

-   [acronym](/html/elements/acronym)
-   [applet](/html/elements/applet) (deprecated in [HTML 4.01](http://www.w3.org/TR/html401/), non conformant in [HTML5](http://www.w3.org/TR/html5))
-   [basefont](/html/elements/basefont) (deprecated in [HTML 4.01](http://www.w3.org/TR/html401/), non conformant in [HTML5](http://www.w3.org/TR/html5))
-   [bgsound](/w/index.php?title=html/elements/bgsound&action=edit&redlink=1)
-   [big](/html/elements/big)
-   [blink](/html/elements/blink)
-   [c](/w/index.php?title=html/elements/c&action=edit&redlink=1) (never deployed, was a proposal before [span](/html/elements/span))
-   [center](/html/elements/center) (deprecated in [HTML 4.01](http://www.w3.org/TR/html401/), non conformant in [HTML5](http://www.w3.org/TR/html5))
-   [font](/html/elements/font) (deprecated in [HTML 4.01](http://www.w3.org/TR/html401/), non conformant in [HTML5](http://www.w3.org/TR/html5))
-   [frame](/html/elements/frame)
-   [frameset](/w/index.php?title=html/elements/frameset&action=edit&redlink=1)
-   [isindex](/w/index.php?title=html/elements/isindex&action=edit&redlink=1) (deprecated in [HTML 4.01](http://www.w3.org/TR/html401/), non conformant in [HTML5](http://www.w3.org/TR/html5))
-   [listing](/html/elements/listing)
-   [marquee](/html/elements/marquee)
-   [nextid](/w/index.php?title=html/elements/nextid&action=edit&redlink=1)
-   [nobr](/w/index.php?title=html/elements/nobr&action=edit&redlink=1)
-   [noembed](/w/index.php?title=html/elements/noembed&action=edit&redlink=1)
-   [noframes](/w/index.php?title=html/elements/noframes&action=edit&redlink=1)
-   [plaintext](/w/index.php?title=html/elements/plaintext&action=edit&redlink=1)
-   [spacer](/w/index.php?title=html/elements/spacer&action=edit&redlink=1)
-   [strike](/html/elements/strike) (deprecated in [HTML 4.01](http://www.w3.org/TR/html401/), non conformant in [HTML5](http://www.w3.org/TR/html5))
-   [tt](/html/elements/tt)
-   [u](/html/elements/u) (deprecated in [HTML 4.01](http://www.w3.org/TR/html401/), non conformant in [HTML5](http://www.w3.org/TR/html5))
-   [xmp](/html/elements/xmp)

## See also

-   [HTML: The Markup Language Reference](http://www.w3.org/TR/html-markup/)
-   [HTML Educational material for beginners](/w/index.php?title=html/training&action=edit&redlink=1)
-   [New HTML5 Elements](/w/index.php?title=html/new_html5_elements&action=edit&redlink=1)
-   [HTML5](http://www.w3.org/TR/html5)
-   [List of MathML Elements](/mathml/elements)
-   [List of SVG Elements](/svg/elements)
