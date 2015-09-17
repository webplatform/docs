---
title: 'Visual Impairment'
summary: "\nA visual impairment is a person's reduced ability to see and see clearly. This includes reduced sensitivity and reduced clarity.\n"
tags:
  - Concept_Pages
  - Accessibility
uri: 'concepts/accessibility/definitions/visual impairment'

---
## Summary

A visual impairment is a person's reduced ability to see and see clearly. This includes reduced sensitivity and reduced clarity.

A visual impairment tends to mean that a person is unable to react to visual stimuli the same as someone who does not have a visual impairment. This can be caused by a number of different impairments, such as blindness, achromatopsia (color-blindness), hyperopia (far-sightedness), myopia (near-sightedness), and scotoma (blind spots).

Visual impairments as they apply to websites are address by Section 508 [1194.22](http://www.access-board.gov/sec508/guide/1194.22.htm%7C), [1194.23](http://www.access-board.gov/sec508/guide/1194.23.htm%7C), and [1194.24](http://www.access-board.gov/sec508/guide/1194.24.htm%7C). To summarize, all visual components should include a textual description or label so someone with a visual impairment can understand the visual component without being able to see it. Your website should never rely solely on pictures or colors to convey necessary or instructive information.

The Web is predominantly a visual medium and, because of that, there are more accommodations that must be made for people with visual impairments.

## Remember

Disabilities are not mutually exclusive. Someone with a visual impairment may also have audio, cognitive, and mobility impairments.

## Examples

-   Provide descriptive text in the `alt` attribute for all images. Use an empty `alt` attribute for placeholder images. This allows someone with low vision or blindness to grasp the import of an image.
-   If using an image button, make sure the `alt` text matches the image text exactly. This allows someone with low vision or blindness to get support using your website.
-   Provide labels for all form inputs. This allows a screen reader to define the meaning of each form input.
-   Use fieldsets to group inputs that are semantically related, such as the different fields for a mailing address. This allows a screen reader to include the label of the group with the label of the individual field, reducing the redundancy of text on the screen without losing the association for a screen reader.
-   Do not use color as the only means to distinguish between elements. This allows someone with color blindness, low vision, or blindness to distinguish between items (such as valid or invalid entries).
-   Do not force your stylesheet on the user, particularly as it applies to colors and fonts. This allows someone with color blindness or low vision to use a personal stylesheet in addition to that provided by your website.
-   Provide redundant text links for the active areas of image maps, particularly server-side image maps. This allows someone with a screen reader to effectively navigate your site without the use of the image map.
-   Provide descriptive text in the `alt` attribute for all active areas in a client-side image map. This allows someone with a screen reader to effectively navigate the image map.
-   Use the `scope` attribute for `th` elements to define the scope of table headers. Use the `headers` attribute for `td` elements to associate table cells with the appropriate headers. This allows someone with a screen reader to make the same association between data and headers as someone else would visually.
-   Use the `summary` attribute of the `table` tag and include a `caption` tag within the table to provide a summary of the information in the table and its organization. This allows someone with a screen reader to quickly get a grasp of the contents of a table as someone else could visually.
-   Use the `title` attribute of the `frame` tag to describe its function and content. Provide a "No Frames" link when possible. This allows someone with a screen reader to effectively navigate a frameset.
-   Avoid causing the screen to flash, flicker, or blink (between 2 Hz and 55 Hz). This prevents your site from inducing headaches and seizures in people sensitive to such stimuli.
-   Use descriptive text for hyperlinks, especially hyperlinks that execute JavaScript. Do not rely on the status bar to convey meaningful information. This allows someone with a screen reader to understand what will happen when clicking on a hyperlink.
-   Avoid attaching handlers to double-click, mouse-down, mouse-up, blur, and focus events. This allows someone with a screen reader to interact with your page as well as someone else could.

## See also

### External resources

<http://www.access-board.gov/sec508/guide/>
