---
title: @page
tags:
  - CSS
  - At
  - Rules
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Empty "Main Content" section, see @import for notes for improvement suggestion. Remarks section seems to contain all elaboration on the @page rule. By having detail further down it does make for easy quick reference when landing on the page, but can also be confusing to first-time viewers as it differs from the structure of the other rules.'
summary: 'Specifies properties of a page box, such as its dimensions, orientation, and margins. This is used for paged media, such as the printed page.'
uri: css/atrules/@page

---
# @page

## Summary

Specifies properties of a page box, such as its dimensions, orientation, and margins. This is used for paged media, such as the printed page.

## Examples

The following are examples of page selectors (declaration block intentionally left blank).

    @page { ... }
    @page :left { ... }
    @page :right { ... }
    @page LandscapeTable { ... }
    @page CompanyLetterHead:first { ... } /*  identifier and pseudo page. */
    @page:first { ... };

The following are examples of margin boxes where the declaration blocks are intentionally left blank.

    @page {
        @top-left { ... /* document name */ }
        @bottom-center { ... /* page number */}
    }

    @page :left {
        @left-middle { ... /* page number in left margin */ }
    }

    @page :right{
        @right-middle { ... /* page number in right margins of right pages */}
    }

    @page :left {
        @bottom-left-corner { ... /* left page numbers */ }
    }

    @page :right {
        @bottom-right-corner { ... /* right page numbers */ }
    }

    @page :first {
        @bottom-left-corner { ... /* empty footer on 1st page */ }
        @bottom-right-corner { ... /* empty footer */ }
    }

## Notes

### Remarks

#### Page Boxes

In the page model, the document is transferred into one or more page boxes. The page box is a specialized Cascading Style Sheets (CSS) box that maps to a rectangular print media surface. It is roughly analogous to the viewport. As for other boxes, a page box consists of margin, border, padding, and content areas. The content and margin areas of a page box have special functions:

-   The content area of a page box is called the page area. The content of the document is flowed into the page area. The edges of the page area on the first page establish the rectangle that is the initial containing block of the document.
-   The margin area of a page box is divided into 16 margin boxes. Each margin box has its own margin, border, padding and content areas. Margin boxed are typically used to display running headers and footers.

The properties of a page box are determined by properties established within the page context, which is the rule set of the **@page** rule. Page boxes differ from other boxes in that the [**width**](/css/properties/width) and [**height**](/css/properties/height) properties do not apply to a page box. The size of the page box is specified using the **size** property in the page context. When printing double-sided documents, the page boxes on left and right pages may be different. This can be expressed through CSS pseudo-classes defined in the page context. All pages are automatically classified by user agents into either the **:left** or **:right** pseudo-class. A page that will be on the left if it is part of a pair of facing pages as typically laid out. Page layouts for documents using a left-to-right major writing direction have the earlier of the facing pages on the left. Rules for the left page can be specified using the **:left** page selector. A page that will be on the right if it is part of a pair of facing pages as typically laid out. Page layouts for documents using a right-to-left major writing direction have the earlier of the facing pages on the right. Rules for the right page can be specified using the **:right** page selector. The first page is generally printed on the front side of a medium. Rules for the first page can be specified using the **:first** page selector. A first page can be either a left page or a right page, but rules defined for a first page are applied in preference to those defined on a left page or a right page.

#### Margin Boxes

Margin boxes can be used to create page headers and footers, which are portions of the page set aside for supplementary information such as the page number or document title. The location of page headers and footer is one of the many graphic design choices a document's author makes. Typically, a page header is located at the top of the page in documents with a predominately horizontal writing direction and on the side opposite the binding edge for documents with a predominately vertical writing direction. One possible design of page headers for horizontally written documents uses the **top-left-corner**, **top-left**, **top-center**, **top-right**, and **top-right-corner** margin boxes. Another design, for vertically written documents, could use the **right-top**, **right-middle**, and **right-bottom** margin boxes for right facing pages and **left-top**, **left-middle**, and **left-bottom** for left facing pages. However, there are no constraints placed on the use of margin boxes for page headers. Typically, the page footer is at the opposite end of the page from the page header. For example, the design of a horizontally written document with a page header at the top of the page could use the **bottom-left-corner**, **bottom-left**, **bottom-center**, **bottom-right** and **bottom-right-corner** margin boxes as the page footer. The design of a vertically written document could use the margin boxes of the binding edge of the page for the page footer. However, there are no constraints placed on the use of margin boxes for page footers. Please note that the margin boxes are oriented with respect to the content and are independent of page orientation, for example the top margin boxes are above the page box in both portrait and landscape orientation.

### Syntax

`@page page_selector? { [ page_declaration | margin_ruleset ];* }` **page\_selector**: `pageName?'[:left|:right|:first]'?` **margin\_ruleset**: `marginBox { margin_declaration+ }`

### Parameters

The page name and page pseudo-class constitutes the page selector. The page selector specifies for which pages the declarations apply. In CSS3, page selectors may designate the first page of a document, all left pages, all right pages, or pages with specific names.

*pageName*
:   Specifies that the declarations in *PageContextRules* applies to pages with this name. The values "auto" may not be used.
`:left`
:   Specifies that the declarations in *PageContextRules* applies to left pages.
`:right`
:   Specifies that the declarations in *PageContextRules* applies to right pages.
`:first`
:   Specifies that the declarations in *PageContextRules* applies to the first page.

The *page box* contains portions of the document flow destined for rendering on a page sheet. The margins of the page box are divided into *margin boxes* that act as containing boxes for header/footer content. The area of the page box within its margins form the content area of the page, called the *page area*.

<dl>
<dt>
`marginBox`

</dt>
<dd>
Specifies the marginal area that margin declarations apply to. The following marginal areas are defined.

<dl>
<dt>
Value

</dt>
<dd>
Meaning

</dd>
<dt>
<dl>
<dt>
@top-left-corner

</dt>
</dl>
</dt>
<dd>
a fixed-size box filling the area defined by the intersection of the top and left margins of the page box

</dd>
<dt>
<dl>
<dt>
@top-left

</dt>
</dl>
</dt>
<dd>
a variable-width box within the area defined by the top margin and adjoining the top-left-corner margin box

</dd>
<dt>
<dl>
<dt>
@top-center

</dt>
</dl>
</dt>
<dd>
a variable-width box within the area defined by the top margin, centered on the page area, and between the top-left and top-right margin boxes

</dd>
<dt>
<dl>
<dt>
@top-right

</dt>
</dl>
</dt>
<dd>
a variable-width box within the area defined by the top margin and adjoining the top-right-corner margin box

</dd>
<dt>
<dl>
<dt>
@top-right-corner

</dt>
</dl>
</dt>
<dd>
a box filling the area defined by the intersection of the top and right margins of the page box

</dd>
<dt>
<dl>
<dt>
@left-top

</dt>
</dl>
</dt>
<dd>
a variable-height box within the area defined by the left margin and adjacent to the bottom of the top-left-corner

</dd>
<dt>
<dl>
<dt>
@left-middle

</dt>
</dl>
</dt>
<dd>
a variable-height box in the area defined by the left margin, centered on the page area, and between the left-top and left-bottom margin boxes

</dd>
<dt>
<dl>
<dt>
@left-bottom

</dt>
</dl>
</dt>
<dd>
a variable-height box within the area defined by the left margin and adjacent to the top of the bottom-left-corner

</dd>
<dt>
<dl>
<dt>
@right-top

</dt>
</dl>
</dt>
<dd>
a variable-height box within the area defined by the right margin and adjacent to the bottom of the top-right-corner

</dd>
<dt>
<dl>
<dt>
@right-middle

</dt>
</dl>
</dt>
<dd>
a variable-height box in the area defined by the right margin, centered on the page area, and between the right-top and right-bottom margin boxes

</dd>
<dt>
<dl>
<dt>
@right-bottom

</dt>
</dl>
</dt>
<dd>
a variable-height box within the area defined by the right margin and adjacent to the top of the bottom-right-corner

</dd>
<dt>
<dl>
<dt>
@bottom-left-corner

</dt>
</dl>
</dt>
<dd>
a box filling the area defined by the intersection of the bottom and left margins of the page box

</dd>
<dt>
<dl>
<dt>
@bottom-left

</dt>
</dl>
</dt>
<dd>
a variable-width box within the area defined by the bottom margin and adjoining the bottom-left-corner margin box

</dd>
<dt>
<dl>
<dt>
@bottom-center

</dt>
</dl>
</dt>
<dd>
a variable-width box within the area defined by the bottom margin, centered on the page area, and between the bottom-left and bottom-right margin boxes

</dd>
<dt>
<dl>
<dt>
@bottom-right

</dt>
</dl>
</dt>
<dd>
a variable-width box within the area defined by the bottom margin and adjoining the bottom-right corner margin box

</dd>
<dt>
<dl>
<dt>
@bottom-right-corner

</dt>
</dl>
</dt>
<dd>
a box filling the area defined by the intersection of the bottom and right margins of the page box

</dd>
</dl>
�

</dd>
<dt>
*margin\_declaration*

</dt>
<dd>
A CSS property declaration applicable to a margin box.

</dd>
<dt>
*page\_declaration*

</dt>
<dd>
A CSS property declaration applicable to the page area.

</dd>
</dl>
## Related specifications

Specification
:   Status
[CSS Paged Media Module Level 3](http://www.w3.org/TR/css3-page/#at-page-rule)
:   W3C Working Draft

## See also

### Related articles

#### Paged Media

-   **@page**

-   [widows](/css/properties/widows)

#### Syntax

-   [@charset](/css/atrules/@charset)

-   [@font-face](/css/atrules/@font-face)

-   [@import](/css/atrules/@import)

-   [@keyframes](/css/atrules/@keyframes)

-   [@namespace](/css/atrules/@namespace)

-   **@page**

-   [@supports](/css/atrules/@supports)

-   [CSS reference](/css/reference)

-   [Alphabetical list of CSS reference](/css/reference/alphabetical)

-   [!important](/css/syntax/!important)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

