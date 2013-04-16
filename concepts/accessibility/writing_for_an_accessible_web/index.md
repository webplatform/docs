{{Page_Title|Writing for an Accessible Web}}
{{API_Name}}
{{Summary_Section|
Do you have a cool idea for a website that you want to share with everyone? Excellent! People with disabilities tend to feel left out of websites, so try following these tips to share your website with them, too.
}}
{{Concept_Page}}
With several browsers available and a continuing history of incompatibility between them, many website designers have been satisfied to produce robust websites that work in a certain selection of those browsers. Sometimes, website designers will choose a single browser and design the site to work with that one; sometimes, the designer will choose a selection of browsers (usually what the designer already has installed). With the amount of effort trying to design a website to work well in the browser or browsers the designer has selected, it feels like making the site accessible to people with disabilities is the straw that broke the camel's back.

Fortunately, making a website accessible to people with disabilities doesn't have to be difficult. Some basic principles apply and many of these principles make a site accessible and usable for people without disabilities, too.
==Who is my audience?==
There is a whole spectrum of people who may visit your website, regardless of what brought them there. This includes a wide range of "typical" people, people who have not been diagnosed with a disability, as well as people with [[concepts/accessibility/definitions/audio_impairment|audio]], [[concepts/accessibility/definitions/cognitive_impairment|cognitive]], [[concepts/accessibility/definitions/mobility_impairment|mobility]], and [[concepts/accessibility/definitions/visual_impairment|visual]] impairments. Many of the affordances made for people with disabilities actually underline sound web design and make a site easier to use for people without disabilities.
==How do I reach my audience?==
One of the first things to remember when designing a website that is intended to be accessible is that your site should not rely on JavaScript to operate. Since JavaScript is a core technology for AJAX (it's the J in AJAX), your site should not rely on AJAX, either. Does this mean your site cannot use JavaScript or AJAX? No! It means that your site should be just as usable without JavaScript and AJAX as it is with those technologies. It may not be as flashy, but people should be able to perform the same tasks with JavaScript turned off as they could with everything enabled and working.

Because the Web is predominantly a visual medium, [[concepts/accessibility/definitions/visual_impairment|visual impairments]] seem to require more accommodations than any other type of impairment. While [[concepts/accessibility/definitions/cognitive_impairment|cognitive impairments]] and the accommodations afforded them may also seem daunting, many of these accommodations are actually part of good usability design.
==What do I need to do?==
Yes, there are a lot of them, but here are some guidelines to follow when building websites.
===JavaScript & Plugins===
* Provide a <code>noscript</code> version of your website.
** This version should be as functional as the JavaScript-enabled version of your website. You will lose visitors (and not just people with disabilities) if your <code>noscript</code> version is entirely non-functional (''i.e.'', "You must enable JavaScript to view this page.").
** Screen readers can have trouble processing changes to the content of a page and some browsers do not support JavaScript.
** Changing content can also be perceived as "noise" and interfere with a person's ability to understand the content of your website.
* If a hyperlink fires a JavaScript function (''e.g.'', <code>href="javascript:doSomething()"</code>), use the text of the hyperlink or the <code>alt</code> tag of the image in the hyperlink to describe what the function does.
** A screen reader can understandably have difficulty trying to read the name of a JavaScript function. Just as the text of a hyperlink would ease the understanding of a typical browser, so the text of the hyperlink or <code>alt</code> text of the image ease the understanding of someone using a screen reader.
* Avoid making functionality dependent on events other than onLoad, onUnload, and onClick.
** Besides inconsistent implementation of certain events (''e.g.'', onChange), screen readers may never fire certain events. Events such as onMouseOver and onMouseOut may not be fired by someone who uses a screen reader or touch screen.
** If you decide to attach handlers to other events, make sure that the functionality is available through accessible means (''e.g.'', hyperlinks).
* Link to accessible sites for any plugins that are required to render your website properly.
** If you have anything other than plain text or simple web pages on your site, chances are that plugins are required to render your website properly. Don't make the browser search for an accessible site where the plugins are available; find the sites and provide the links yourself.
===Images===
* Provide text alternatives for any content images (''e.g.'', the <code>alt</code> attribute of the <code>img</code> tag) that are not simply placeholders. Set the <code>alt</code> attribute to an empty string for a placeholder image.
** Screen readers will use the <code>alt</code> text in an attempt to describe the import of your images.
* When providing a text alternative for an image with text in it, make sure the image text is reflected exactly in the text alternative, particularly if the image is used as a button or link. '''Example''': A green button with the text "Start" could use "Green Start button" as its <code>alt</code> text.
** Screen readers cannot read the text in the image itself. If written or spoken instructions refer to the text of the image, the person using a screen reader should be able to identify that image through the <code>alt</code> text.
* Whenever possible, use client-side image maps.
** A server-side image map hides the destination from the user and prevents a screen reader from seeing what areas of the image are active and where each area would direct the user.
* Provide textual alternatives to all image maps, particularly server-side image maps.
** Navigation should not rely on the ability to click on certain points in an image map. If necessary due to the number of links, you can provide this alternative on another page so long as it is clear how to get to that page.
** Every area in an image map should have <code>alt</code> text to assist someone using a screen reader.
* Avoid flickering images.
** People who suffer from epileptic seizures can be sensitive to flickering lights. If your website presents a flickering image, it may cause a seizure for someone prone to have them.
===Navigation===
* Provide text to explain the function of any frames in your website.
** Screen readers will use the <code>alt</code> text for a <code>frame</code> tag to describe the function of that frame.
* If you have navigation links, provide a link to skip to the main content of your website.
** Someone using a screen reader and already familiar with the navigation of your website can use this link to skip to the content without having to listen to the list of navigation links again.
* ''See the guidelines under "Images" regarding image maps.''
===Tables===
* Provide a summary and caption for any tables on your website.
** This will help someone using a screen reader get a quick grasp of the layout and content of your tables, much like a person without a visual disability will scan over a table to determine its layout and import before delving into the details of the content.
* Define row and column headers.
** Use the <code>scope</code> attribute for <code>th</code> elements to indicate when the header applies to a column, row, column group, or row group. This helps a screen reader associate the header with the appropriate data cells.
** Use the <code>id</code> attribute for <code>th</code> elements and <code>headers</code> attribute for <code>td</code> elements to associated data cells with the appropriate header cells. This also helps a screen reader associate the appropriate headers with their associated data cells.
===Forms===
* Break forms into semantically related input groups using the <code>fieldset</code> tag.
** Provide a caption for the <code>fieldset</code> that will make the form easier to understand. Some screen readers will read the <code>fieldset</code> caption with each form element contained therein. Used properly, fieldsets also break form elements into semantically related groups, aiding people with or without cognitive and visual disabilities.
* Active form elements must be explicitly labeled.
** Someone using a screen reader may not understand what to provide in a form element without having a label to describe it.
** Labels provide another landing point for the cursor, making it easier for someone to select the form element. This helps everyone, not just people with mobility or visual impairments.
** Use explicit labels for form elements. Some screen readers are unable to handle implicit labels properly. Explicit labels include the associated form element's <code>id</code> attribute as the label's <code>for</code> attribute and wrap only the text identifying the form element, not the form element itself. Implicit labels do not necessarily include the <code>for</code> attribute, but wrap the form element itself.
* If describing the purpose of an element might take too much space for a label, use the <code>title</code> attribute for that description.
** Screen readers may not support or otherwise have difficulty if the value of the element is originally used to describe its purpose. The <code>title</code> text will appear as a tooltip for most browsers.
===Media===
* Provide captioning for multimedia elements (''e.g.'', videos with audio) and transcripts for audio media (''e.g.'', podcasts).
** A multimedia presentation should include captioning, allowing someone with an audio impairment (or muted sound) to understand the video without hearing the audio.
** A transcript is sufficient for audio-only presentations.
===Colors & Styles===
* Color may be used to convey information, but do not rely on color alone.
** Color cannot translate well to some people with a visual impairment, like color blindness. Make sure that whatever information the color conveys (''e.g.'', valid or invalid) is also conveyed in another way (boldface, italics, descriptive context).
* Stylesheets may be used to organize information, but do not rely on stylesheets alone.
** Someone with a visual impairment may need to override the stylesheets of websites they visit with a personal stylesheet (''e.g.'', high-contrast) in order to read the content. Make sure your website is understandable when any stylesheets are disabled.
===General===
* If it is otherwise impossible or terribly intrusive to provide textual alternatives inline with non-textual elements, provide a text-only version of your website.
** It can be difficult to make a site "cool" and accessible at the same time, to be all things to all people at all times. If you decide to provide a text-only version, make sure that it is always current with the version that has dynamic or non-textual elements.
* If your website is time-sensitive, ''e.g.'', it logs the user out after a certain period of inactivity, give the user an opportunity to request more time.
** While you might think 15 minutes is plenty of time for someone to fill out a form, people for whom your site is in a non-native language or people with disabilities may need more time to complete it. This helps people who do not have disabilities, too. Make sure that someone can request more time without losing the work already completed.
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section|
External_links=http://www.access-board.gov/sec508/guide/}}
{{Topics|Accessibility}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}