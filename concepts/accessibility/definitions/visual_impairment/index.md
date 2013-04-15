{{Page_Title|Visual Impairment}}
{{API_Name}}
{{Summary_Section|
A visual impairment is a person's reduced ability to see and see clearly. This includes reduced sensitivity and reduced clarity.
}}
{{Concept_Page}}
A visual impairment tends to mean that a person is unable to react to visual stimuli the same as someone who does not have a visual impairment. This can be caused by a number of different impairments, such as blindness, achromatopsia (color-blindness), hyperopia (far-sightedness), myopia (near-sightedness), and scotoma (blind spots).

Visual impairments as they apply to websites are address by Section 508 [http://www.access-board.gov/sec508/guide/1194.22.htm| 1194.22], [http://www.access-board.gov/sec508/guide/1194.23.htm| 1194.23], and [http://www.access-board.gov/sec508/guide/1194.24.htm| 1194.24]. To summarize, all visual components should include a textual description or label so someone with a visual impairment can understand the visual component without being able to see it. Your website should never rely solely on pictures or colors to convey necessary or instructive information.

The Web is predominantly a visual medium and, because of that, there are more accommodations that must be made for people with visual impairments.
==Remember==
Disabilities are not mutually exclusive. Someone with a visual impairment may also have audio, cognitive, and mobility impairments.
{{Examples_Section
|Not_required=No
|Examples=
* Provide descriptive text in the <code>alt</code> attribute for all images. Use an empty <code>alt</code> attribute for placeholder images. This allows someone with low vision or blindness to grasp the import of an image.
* If using an image button, make sure the <code>alt</code> text matches the image text exactly. This allows someone with low vision or blindness to get support using your website.
* Provide labels for all form inputs. This allows a screen reader to define the meaning of each form input.
* Use fieldsets to group inputs that are semantically related, such as the different fields for a mailing address. This allows a screen reader to include the label of the group with the label of the individual field, reducing the redundancy of text on the screen without losing the association for a screen reader.
* Do not use color as the only means to distinguish between elements. This allows someone with color blindness, low vision, or blindness to distinguish between items (such as valid or invalid entries).
* Do not force your stylesheet on the user, particularly as it applies to colors and fonts. This allows someone with color blindness or low vision to use a personal stylesheet in addition to that provided by your website.
* Provide redundant text links for the active areas of image maps, particularly server-side image maps. This allows someone with a screen reader to effectively navigate your site without the use of the image map.
* Provide descriptive text in the <code>alt</code> attribute for all active areas in a client-side image map. This allows someone with a screen reader to effectively navigate the image map.
* Use the <code>scope</code> attribute for <code>th</code> elements to define the scope of table headers. Use the <code>headers</code> attribute for <code>td</code> elements to associate table cells with the appropriate headers. This allows someone with a screen reader to make the same association between data and headers as someone else would visually.
* Use the <code>summary</code> attribute of the <code>table</code> tag and include a <code>caption</code> tag within the table to provide a summary of the information in the table and its organization. This allows someone with a screen reader to quickly get a grasp of the contents of a table as someone else could visually.
* Use the <code>title</code> attribute of the <code>frame</code> tag to describe its function and content. Provide a "No Frames" link when possible. This allows someone with a screen reader to effectively navigate a frameset.
* Avoid causing the screen to flash, flicker, or blink (between 2 Hz and 55 Hz). This prevents your site from inducing headaches and seizures in people sensitive to such stimuli.
* Use descriptive text for hyperlinks, especially hyperlinks that execute JavaScript. Do not rely on the status bar to convey meaningful information. This allows someone with a screen reader to understand what will happen when clicking on a hyperlink.
* Avoid attaching handlers to double-click, mouse-down, mouse-up, blur, and focus events. This allows someone with a screen reader to interact with your page as well as someone else could.
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section|
External_links=http://www.access-board.gov/sec508/guide/
}}
{{Topics|Accessibility}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}