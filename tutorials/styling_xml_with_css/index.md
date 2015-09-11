---
title: Styling XML data with CSS
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/XML_data)'
readiness: 'Ready to Use'
summary: 'This article shows how you can use CSS to style XML data.'
tags:
  - Tutorials
  - CSS
uri: 'tutorials/styling xml with css'

---
## <span>Summary</span>

This article shows how you can use CSS to style XML data.

### <span>Information: XML data</span>

**XML** (eXtensible Markup Language) is a general-purpose language for any kind of structured data.

By default, your Mozilla browser displays XML in a format very similar to the original data in the XML file. You see the actual tags that define the data's structure.

But by linking a CSS stylesheet with the XML document, you can define other ways to display it. To do this, your stylesheet uses rules that map tags in the XML document to the display types used by HTML.

#### <span>Example</span>

For example, you have data in an XML document uses `<INFO>` tags. You want the document's INFO elements to be displayed like HTML paragraphs.

In the document's stylesheet, you specify how the `<INFO>` elements are to be displayed:

```
INFO {
  display: block;
  margin: 1em 0;
}
```

The most common values for the `display` property are:

||
|`block`|Displayed like HTML's DIV (for headings, paragraphs)|
|`inline`|Displayed like HTML's SPAN (for emphasis within text)|

Add your own style rules that specify the font, spacing and other details in the same way as for HTML. Other values of `display` display the element like a list item, or like a component of a table.

For the full list of display types, see [the display property](/css/properties/display). Using CSS alone, the structure of the display must be the same as the structure of the document. Other technologies can modify the structure of the display—for example, XBL can add content, and JavaScript can modify the DOM.

### <span>Action: An XML demonstration</span>

1.  Make a new XML file, `doc9.xml`. Copy and paste the content from here, making sure that you scroll to get all of it:

    ```
    <?xml version="1.0"?>
    <!-- XML demonstration -->

    <?xml-stylesheet type="text/css" href="style9.css"?>

    <!DOCTYPE planet>
    <planet>

    <ocean>
    <name>Arctic</name>
    <area>13,000</area>
    <depth>1,200</depth>
    </ocean>

    <ocean>
    <name>Atlantic</name>
    <area>87,000</area>
    <depth>3,900</depth>
    </ocean>

    <ocean>
    <name>Pacific</name>
    <area>180,000</area>
    <depth>4,000</depth>
    </ocean>

    <ocean>
    <name>Indian</name>
    <area>75,000</area>
    <depth>3,900</depth>
    </ocean>

    <ocean>
    <name>Southern</name>
    <area>20,000</area>
    <depth>4,500</depth>
    </ocean>

    </planet>
    ```

2.  Make a new CSS file, `style9.css`. Copy and paste the content from here, making sure that you scroll to get all of it:

    ```
    /*** XML demonstration ***/

    planet:before {
      display: block;
      width: 8em;
      font-weight: bold;
      font-size: 200%;
      content: "Oceans";
      margin: -.75em 0px .25em -.25em;
      padding: .1em .25em;
      background-color: #cdf;
      }

    planet {
      display: block;
      margin: 2em 1em;
      border: 4px solid #cdf;
      padding: 0px 1em;
      background-color: white;
      }

    ocean {
      display: block;
      margin-bottom: 1em;
      }

    name {
      display: block;
      font-weight: bold;
      font-size: 150%;
      }

    area {
      display: block;
      }

    area:before {
      content: "Area: ";
      }

    area:after {
      content: " million km\B2";
      }

    depth {
      display: block;
      }

    depth:before {
      content: "Mean depth: ";
      }

    depth:after {
      content: " m";
    }
    ```

3.  Open the document in your browser:

-   The superscript 2 (in "million km²") a Unicode character, coded as `\B2` in the CSS file.
-   The heading, "Oceans", has a negative top margin, moving it up so it is displayed on top of the border.

## <span>See also</span>

## <span>Exercise question</span>

Change the stylesheet so that it displays the document as a table.