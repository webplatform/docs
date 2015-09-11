---
title: Accessibility testing
tags:
  - Tutorials
  - WSC
uri: 'Accessibility testing'

---
## <span>Introduction</span>

Web accessibility testing is a subset of usability testing where the users under consideration have disabilities that affect how they use the web. The end goal, in both usability and accessibility, is to discover how easily people can use a web site and feed that information back into improving future designs and implementations.

Accessibility evaluation is more formalized than usability testing generally. Laws and public opinion frown upon discriminating against people with disabilities. In order to be fair to all, governments and other organizations try to adhere to various web accessibility standards, such as the US federal government’s [Section 508 legislation](http://dev.opera.com/articles/view/25-accessibility-basics/#section508).

However, it is important to distinguish between complying with a standard and maximizing the accessibility of a web site. Ideally, the two would be the same, but any given standard may fail to:

-   address the needs of people with all disabilities.
-   balance the needs of people with differing disabilities.
-   match those needs to optimal techniques.
-   use clear language to express needs or techniques.

Such weaknesses can lead those with good intentions astray and may be exploited by those seeking to rubberstamp inaccessible products.

Moreover, web accessibility is a goal, not a yes/no setting. It is a nexus of human needs and technology. As our understanding of human needs evolves and as technology adapts to those needs, accessibility requirements will change as well and current standards will be outdated. Different websites, and different webs, serve different needs with different technology. Voice chat like Skype is great for the blind, whereas [video chat is a boon for sign language users](http://developer.yahoo.net/blog/archives/2008/05/yahoo_live_empo.html).

Disabilities pose special challenges when working out how easy a product is to use, because they can introduce additional experience gaps between users and evaluators. Accessibility evaluation must take account of what it is like to experience the web with different senses and cognitive abilities and of the various unusual configuration options and specialist software that enable web access to people with particular disabilities.

If you are trying to evaluate the usability or accessibility of your web site, putting yourself in the place of a film-loving teenager or a 50-year old bank manager using your site is difficult, even before disabilities are considered. But what if the film-loving teenager is deaf and needs captions for the films she watches? What if the 50-year old bank manager is blind and uses special technology (like a screen reader) which is unfamiliar to the evaluator in order to interact with his desktop environment and web browser?

Accessibility guidelines and tools help bridge these experience gaps. However, they are a supplement, not a replacement, for empathic imagination, technical ingenuity, and talking to users.

In this article of the [Web Standards Curriculum](http://www.w3.org/wiki/Web_Standards_Curriculum), I will discuss approaches to evaluating web accessibility, both from the perspective of establishing formal compliance and from the perspective of maximizing accessibility.

## <span>When should testing be done?</span>

“Test early, test often” is an old software engineering saying. Tacking on testing at the end of the development process has two risks:

1.  Projects tend to run over-time and over-budget. Testing is often rushed, omitted, or ignored thanks to such pressures.
2.  It is more work to fix problems discovered late in a process than to do things right from the start.

So to ensure quality and save time and money, accessibility evaluations should start right at the beginning of product design and be included in subsequent development iterations through to final delivery.

## <span>Understanding your requirements</span>

Before you begin to evaluate a project for accessibility, you need to determine what the key requirements are for that project, given its environment, intended audience, and resources. Some requirements will be set by third parties like governments and clients; some you may be able to choose for yourself.

### <span>External requirements</span>

Often requirements come from external sources, such as:

-   **Governments**. This typically takes the form of general legislation against discriminating against people with disabilities, rather than mandating a particular standard or enumerating precise conformance requirements. An important exception is when legislation enforces a particular standard for public sector. For example, [Section 508](http://www.section508.gov/) is a piece of US federal legislation, which mandates that websites produced for federal agencies must conform to at least a specific set of defined requirements. WAI’s [Policies Relating to Web Accessibility](http://www.w3.org/WAI/Policy/) page provides a partial list of similar legislation. But to get an authoritative statement of the obligations in your jurisdiction, consult a lawyer.
-   **Customer policies**. For example, [Shell currently try to ensure their websites conform to the "Double-A" conformance level of WCAG 1.0](http://www.shell.com/home/content/footer/accessibility/statement/), so if you were developing a website for Shell you would need to meet (at least) the same standard.
-   **Marketing utility**. Compliance with a particular standard, such as Section 508, might help sell a project to clients concerned about accessibility.
-   **Internal accessibility policies at your organization**. For example, projects produced by the BBC need to comply with the [BBC's Accessibility Guidelines v1.3](http://www.bbc.co.uk/guidelines/futuremedia/accessibility/).

### <span>The details of conformance</span>

It is important to get as much clarity about external requirements as possible. Some accessibility standards have more than one possible level or type of conformance, so it is particularly important to nail down which is required. For example, WCAG 1.0 has three conformance levels:

1.  People with some disabilities “will find it impossible to access information” in a document that does not pass level “A”.
2.  People with some disabilities “will find it difficult to access information” in a document that does not pass level “Double-A”.
3.  People with some disabilities “will find it somewhat difficult to access information” in a document that does not pass level “Triple-A”.

Draft WCAG 2.0 has three levels too, but the conformance possibilities are more complicated. Where a resource is part of a series of resources presenting a process (eg product discovery, selection, checkout, and purchase confirmation for an online store), the conformance level for all resources in the series is that of the resource with the lowest level.

Conformance claims must be based on “accessibility-supported” content technology. To be an accessibility-supported content technology, a technology must:

-   Have been demonstrated to work with users’ assistive technology.
-   Have user agents (browsers, plugins, etc.) that work with the users' assistive technology and are available to users with disabilities at no cost above that for a user without a disability.

Note that within an intranet setting, you might be able to guarantee that such user agents would be available to users whereas you cannot guarantee the same thing on the World Wide Web. For example, an application might be usable without any commercial technology, but only be accessible to screen readers with a commercial plugin for which the organization has a site licence. That application could conform to WCAG 2.0 when deployed on the organization’s intranet, but not when deployed on the public Web.

WCAG 2.0 also allows more limited statements of conformance. An inaccessible resource can conform if an accessible alternative is provided. Publishers can make a statement of partial conformance where content is aggregated from other sources.

### <span>Exceeding expectations</span>

Determining external requirements should only be the beginning of the process; they should be treated as a minimum set of requirements to which further goals should be added to maximize accessibility. As the person evaluating accessibility, it is your role to raise additional accessibility concerns, as you are the subject expert.

You may need to distinguish the two when delivering a final report. For example, a customer brief for an online supermarket might mention that they want a store accessible to blind users. Given the intended audience, you should also evaluate whether the store is accessible to users with other disabilities.

Note that external requirements for compliance with a particular standard do not necessarily prevent best practice guidelines from other standards being applied. For example, you might be evaluating a website for a web federal agency intended for use by senior citizens and be required to comply with Section 508. Section 508 stipulates that:

> § 1194.22 (c) Web pages shall be designed so that all information conveyed with color is also available without color, for example from context or markup.

This provision helps users who know how to customize the presentation of web content, but doesn’t maximize the accessibility of the default presentation of that content to the target audience by ensuring that there is sufficient contrast between suggested colors. Fortunately, there’s nothing stopping a web site from fulfilling this requirement but also meeting the following Level provisions from the Web Content Accessibility Guidelines 2.0 draft:

> 1.4.3 Contrast (Minimum): Text and images of text have a contrast ratio of at least 5:1, except for the following: (Level AA)
>
> -   Large Print: Large-scale text and large-scale images of text have a contrast ratio of at least 3:1;
> -   Incidental: Text or images of text that are part of an inactive user interface component, that are pure decoration, that are incidental text in an image, or that are not visible to anyone, have no minimum contrast requirement.
>
> Note: Success Criteria 1.4.3 and 1.4.6 can be met via a contrast control available on or from the page.

> 1.4.6 Contrast (Enhanced): Text and images of text have a contrast ratio of at least 7:1, except for the following: (Level AAA)
>
> -   Large Print: Large-scale text and large-scale images of text have a contrast ratio of at least 5:1;
> -   Incidental: Text or images of text that are part of an inactive user interface component, that are pure decoration, that are incidental text in an image, or that are not visible to anyone, have no minimum contrast requirement.
>
> Note: Success Criteria 1.4.3 and 1.4.6 can be met via a contrast control available on or from the page.

By contrast control, the criteria means that you should provide a way of changing the colours to a high-contrast variation. To test the contrast of colour schemes, you can use the [colour contrast analyser from Juicystudio](http://juicystudio.com/services/luminositycontrastratio.php).

WCAG 2.0 is being designed to have a high degree of backwards compatibility with other standards, especially WCAG 1.0 and Section 508.

### <span>The importance of the user interface</span>

Consider the special importance of making the user interface of a web site accessible. Even if content is not available in a suitable form, an accessible user interface may help users identify content of interest and seek external help in converting it to a form they can use. For example, a hard-of-hearing individual might be pointed to a video of a talk on a video-sharing site without captions. Because the URL uniquely identifies that video and because they can still use the player to see the video however they could submit it to a third party, such as the free [Project readOn](http://www.projectreadon.com/) service, for captioning.

### <span>Personas with disabilities</span>

An ideal approach is to build key disabilities for your project right into your other [user personas](http://www.usability.gov/analyze/personas.html): fictional users that act as archetypes for how particular types of users would use a web site. Let us say you are evaluating prototypes for a video sharing site and your personas include:

-   23-year-old James Smith, who is football-mad and especially wants to share sporting highlights with friends.
-   34-year-old Sarah Maddison is a working mom who might not normally have time for a video sharing site. But her three-year old daughter is really keen on watching videos, and Sarah wants to sit and help her find suitable videos she wants to watch.

You can take these personas and incorporate disabilities including (for example):

-   Impaired vision.
-   Colorblindness.
-   Blindness.
-   Deafness.
-   Hard-of-hearing.
-   Deafblindness.
-   Epilepsy.
-   Dyslexia.

For example, you might decide that James is also deaf and wants commentary on match videos to be captioned, and Sarah has poor eyesight and struggles to read fancy fonts and tiny text. These personas guide your rejection of prototypes that fail to include the facility for closed captions in the video player, or use elaborate text headings that would require images.

The WAI’s [How People with Disablities Use the Web](http://www.w3.org/WAI/EO/Drafts/PWD-Use-Web/) and Shawn Lawton Henry’s [Just Ask: Integrating Accessibility Throughout Design](http://www.uiaccess.com/accessucd/personas.html) contain some more example disability-inflected personas to get you started.

It shouldn’t need saying, but don’t assume people with disabilities are interchangeable. Disability is an incredibly varied phenomenon, and on top of that people with disabilities have all the variety that people without disabilities have, differing (for example) in gender, age, interests, values, and skills (perhaps most relevantly, in their computing expertise).

Again, comparing products against accessibility guidelines can help fill in the gaps that your personas do not cover. For example, perhaps you’re following WCAG 2.0 with the video sharing site, but your personas don’t include a user with epilepsy. Nonetheless, you read Guideline 2.3 (“Seizures: Do not design content in a way that is known to cause seizures”) and decide that the system needs to be able to screen uploaded videos for flashing before displaying them.

### <span>Choosing an accessibility standard</span>

If you need to choose an accessibility standard in order to manage web accessibility concerns across a team or in simply to guide you while testing, I’d advise looking at WCAG 2.0 because it:

-   is designed around core human needs that are applicable to technologies other than HTML and CSS (such as Flash).
-   carefully documents the reasoning for each conformance criterion.
-   suggests practical techniques for meeting conformance criteria using current technologies.
-   ensures each provision is testable.
-   incorporates more recent research than current alternatives.
-   is designed to be broadly compatible with existing accessibility standards.
-   will be an international standard.

You can cite compliance with a specific draft of WCAG 2.0; for marketing purposes however it is best to also seek compliance with finished standards like Section 508 and WCAG 1.0 as well as that draft.

### <span>The spirit of the law</span>

When testing against guidelines, it’s important to keep in mind the underlying rationale for any specific technical guidance: to comply with the spirit, not just the letter, of the law.

Here’s a cautionary tale. Section 508 (§ 1194.22) includes a requirement that says: “A text equivalent for every non-text element shall be provided (eg, via `alt`, `longdesc` or in element content).” Likewise WCAG 1.0 includes a checkpoint that reads:

Provide a text equivalent for every non-text element (eg, via `alt`, `longdesc`, or in element content). This includes: images, graphical representations of text (including symbols), image map regions, animations (eg, animated GIFs), applets and programmatic objects, ascii art, frames, scripts, images used as list bullets, spacers, graphical buttons, sounds (played with or without user interaction), stand-alone audio files, audio tracks of video, and video.

Unfortunately, many people reading such guidance misunderstand what a genuine text equivalent for a spacer and decorative elements should be, and produce markup like this:

    <img alt="fancy border" src="fancy-border.gif" border="0">

In fact, since these images convey no new information and have no functionality, the right text equivalent for those images would be an empty string (`alt=""`), which causes the screenreader to just skip over the alt attribute and not read it out. It is very annoying for a screenreader user to have to listen to text such as "fancy border" read out over and over again, when it does not provide them with any useful information.

WCAG 2.0 tries to be clearer. The [equivalent guideline](http://www.w3.org/TR/WCAG20/#text-equiv) says: “All non-text content has a text alternative that presents equivalent information, except for the situations listed below”. One of those situations is: “Decoration, Formatting, Invisible: If it is pure decoration, or used only for visual formatting, or if it is not presented to users, then it is implemented in a way that it can be ignored by assistive technology.” Equally importantly, WCAG 2.0 tries to detail the reasoning behind the [guideline](http://www.w3.org/TR/2007/WD-UNDERSTANDING-WCAG20-20071211/text-equiv.html#text-equiv):

> The purpose of this guideline is to ensure that all non-text content is also available in text. “Text” refers to electronic text, not an image of text. Electronic text has the unique advantage that it is presentation neutral. That is, it can be rendered visually, auditorily, tactilely, or by any combination. As a result, information rendered in electronic text can be presented in whatever form best meets the needs of the user. It can also be easily enlarged, spoken in a voice that is easy to understand, or rendered in whatever tactile form best meets the needs of a user.

## <span>Who should test?</span>

There are basically two groups who conduct testing: experts and users.

Expert testing is important because experts understand how the underlying web technologies interact, can act as a clearing house for knowledge about different user groups, and have the inclination to learn dedicated testing tools.

User testing is crucial because users are the real experts in their own abilities and their own assistive technology. User testing can also reveal usability gaps between more and less technical users, and between people who are familiar with the web site in question (such as the expert testers themselves) and people who aren’t (new users).

A web developer who knows how to use a screen reader is unlikely to explore a site the same as a regular screen reader user; screen reader users who program their own scripts are unlikely to explore the site using the same strategies as screen reader users who just do ordinary computing tasks like writing emails.

Knowledge gained in user testing is fed back into the expert testing process the next time testing is performed (either in another testing iteration on the same project, or a different project entirely). User testing also has a more subtle advantage. By humanizing accessibility and bringing developers together with end users, it can increase the motivation to build accessible websites.

## <span>Expert testing</span>

There are four components to expert testing:

-   Tool-guided evaluation: where a tool looks for accessibility problems and presents them to the evaluator (this would include accessibility checkers and code linters).
-   Screening: where the expert simulates an end-user experience of the web site. Often you don’t need to look very far to find accessibility problems. You might do no more than load the page in your browser and notice the text is very hard to read.
-   Tool-based inspection: where the evaluator uses a tool to probe how the various bits of a web site are working together.
-   Code review: where the evaluator looks directly at the code and assets of a web site to scour for problems.

While beginners may be especially dependent on tool-guided evaluation, evaluators of all levels of experience can benefit from each component. Even beginners can spot `img` elements without text equivalents in HTML markup, and as you get more experienced, you will get quicker at spotting problems before you progress to more rigorous testing. For experts on larger projects, it may not be feasible to manually review all client-side code or inspect all parts of a website, but a tool-guided evaluation can find areas of particular trouble that deserve a closer look. Also, human evaluators may overlook things that a machine evaluation would have caught.

Unfortunately, although there are lots of accessibility tools, most of them are flawed in one way or another. For example, one tool that lists headings in HTML documents makes the error of not including `alt` text from `img` elements. Just as you should keep the spirit of the law in mind with standards compliance, so you should keep it in mind when using tools. Before complaining to someone about an accessibility problem, make sure it is a genuine issue not a tool error.

### <span>Semi-automated accessibility checkers</span>

Once the first-glance problems have been fixed, a good next step is to throw the page at a semi-automated accessibility checker tool. If you are evaluating compliance with a particular standard, you will probably want to pick one that is designed for use with that standard.

If you’re evaluating compliance with Section 508 or WCAG 1.0, [Cynthia Says](http://www.cynthiasays.com/) is a reasonable choice. If you're testing against German BITV 1.0 Level 2, the Italian Stanca Act, or the WCAG 2.0 draft, the only current option is the experimental [ATRC Web Accessibility Checker](http://checker.atrc.utoronto.ca/index.html).

Such tools have significant limitations. There is no such thing as fully automated accessibility testing. For example, given the primitive nature of current artificial intelligence, a computer program cannot have the final say in whether some text is a genuine equivalent for a photograph in context. Even with areas that can theoretically be fully automated, checker programmers may err in their interpretation of accessibility guidelines and lose the spirit of the law amongst its letters.

Good tools inspect the page for accessibility problems and produce a list of things they judge to be errors and other things they judge worth human investigation. For example, if Cynthia Says finds an `img` element with `alt=""`, it will issue a warning (not an error!) instructing the user to “verify that this image is only used for spacing or design and has no meaning.” If the correct text equivalent for that image is an empty string, you should move on to the next error or warning.

Perhaps the biggest advantage of accessibility checkers is that if you choose one, such as [TAW 3](http://www.tawdis.net/), which can be run against multiple URLs, you can find pages in large collections that are likely to require closer inspection.

### <span>Structural inspectors</span>

Many inspection tools are designed to probe structures of web content. Structures, in simple terms, define what the components of a web site are and how they relate to one another. For example, in the HTML document object model (DOM), text can be designated as a label for a form field using the `label` element. Browsers parse the HTML into a document object model. The browser associates various behaviour with particular components. For example, if you click the label of a checkbox, it will normally get checked.

Desktop environments and applications support interactivity with screen readers, speech recognition software, and other assistive technology by providing a similar structure that represents the content and functionality available in the visual presentation. On Windows, the main structural system is called Microsoft Active Accessibility (MSAA), or [UI Automation on Vista](http://msdn.microsoft.com/en-us/library/ms788733.aspx). For example, a dialog has a series of related children, such as its title, its fields, its buttons, and their labels.

Typical assistive technology mostly deals with the browsers’ and plugins’ representation of web content in terms of these structural systems rather than processing web document object models directly.

There are inspectors for both desktop-level structures and web-level object models. On the desktop-level side of things, OS X comes with [Accessibility Inspector](http://developer.apple.com/documentation/Accessibility/Conceptual/AccessibilityMacOSX/OSXAXTesting/chapter_5_section_2.html) and [Accessibility Verifier](http://developer.apple.com/documentation/Accessibility/Conceptual/AccessibilityMacOSX/OSXAXTesting/chapter_5_section_3.html). Microsoft provides inspector tools for [Microsoft Active Accessibility 2.0](http://www.microsoft.com/downloads/details.aspx?familyid=3755582A-A707-460A-BF21-1373316E13F0&displaylang=en) and [Microsoft Active Accessibility 1.3](http://www.microsoft.com/downloads/details.aspx?familyid=4179742F-1F3D-4115-A8BA-2F7A6022B533&displaylang=en). [Accerciser](http://live.gnome.org/Accerciser) is available for the GNOME assistive technology-SPI API.

Tools for poking at the (X)HTML document object model include DOM Inspectors as seen in [Opera Dragonfly](http://www.opera.com/products/dragonfly/) and [Firebug](http://www.getfirebug.com/) and accessibility tool bundles like the [Web Accessibility Toolbar for Internet Explorer and Opera](http://www.wat-c.org/tools/index.html) and the [ICITA Firefox Accessibility Toolbar](http://firefox.cita.uiuc.edu/).

DOM inspectors show you the tree of elements and attributes and text constructed out of the (X)HTML serialization, whereas web accessibility inspectors abstract particular components or relationships and list them. For example, they might list all fields with their labels or all headings or all links.

Digging into the accessibility model should not normally be necessary for (X)HTML, though you might also want to investigate that layer if you think a browser is representing a correct (X)HTML structure incorrectly to assistive technology. Instead, you will normally be checking (X)HTML structures directly.

Not all content can be inspected with DOM or web accessibility inspectors. Inspecting what is exposed to the desktop-level accessibility structures is important for checking what plugin content (media players, Flash content, and Java applets) is being exposed to assistive technology that uses those accessibility models.

In general, you should check that all controls are exposed in the model with the appropriate role (eg text boxes are text boxes, buttons are buttons), and the necessary properties.

### <span>Screening and using end-user assistive technology</span>

Screening involves emulating the experiences of people with disabilities while testing. This might take the form of using assistive technology to interact with a site or attempting to restrict one's abilities in some manner. For example:

-   Using a mouthstick to press keys while testing keyboard accessibility.
-   Viewing a page with the Vischeck simulator, which attempts to present the page, images included, as people with different forms of colorblindness see it.
-   Turning off a monitor while using a screen reader in conjunction with a browser.

Screening can help build developer appreciation for the needs of people with disabilities and can reveal fundamental design flaws. Use of assistive technology can clear up certain misconceptions about how they do and don’t support and interact with web standards. For example, popular screen readers do not use styles suggested for the `aural` or `braille` CSS media types, instead attempting to represent the `screen` type presented by the visual browsers with which they interact.

Using assistive technology is not a task to be taken lightly, since a good understanding of how to use such systems may require a degree of immersion and training. There’s a serious risk of creating new misconceptions. Developers might struggle to do something with a screen reader and assume that reflects a failing in the screen reader, when it really reflects their inexpertise with the tool. They might try to use the tool the wrong way, for example trying to read a page in sequence where a real screen reader user would hop around it using headings and other elements looking for points of interest. Or alternatively, they might fail to read the screen properly. Reading through a page you can see or know well with a screen reader is very different from exploring a brand new site you cannot see.

Use of assistive technology needs to be accompanied by experience of how everyday users employ the technology and conclusions drawn from such use should ideally be confirmed with expert users. On the whole, beginners are better off leaving use of assistive technology to user testers.

### <span>Detailed inspection</span>

Once all genuine problems identified by your chosen checker tool have been fixed, you can move on to manual testing, probing, and review of the project.

WCAG 2.0 splits its best practice criterion into four principles. Content and functionality must be:

-   Perceivable (for example, images should have text equivalents).
-   Operable (for example, it should be possible to interact with a web site without a mouse and navigate it with a screen reader).
-   Understandable (for example, copy should not be more complicated than it needs to be and the web site should operate in a predictable manner).
-   Robust (for example, web sites should work interoperably with different user agents and navigation should be consistent).

In this section, I shall present some examples of how expert testers can evaluate how far content matches up to these principles. Please note this section is not intended as a substitute for a review of WCAG and its techniques.

#### <span>Perceivability</span>

One subset of perceivability problems revolves around the provision of alternative media of various types. You can test for text equivalents by turning off images and multimedia in your browser and looking at the page. But you’ll need to take special care with the `img` and `input` elements. Normally, you are advised to give all purely decorative images blank `alt` attributes (`alt=""`) so that the screenreader will just skip them. However, in the case of:

-   Images that are the sole content of links
-   Form buttons

When these elements are given `alt=""` attributes, screen readers will commonly treat the image or button as if the `alt=""` attribute is missing, and attempt to provide one (for example, by reading out the URL of the image).

Therefore in these particular circumstances you must ensure that images inside links or buttons have an `alt` attribute that describes the link destination or button action, even though this is slightly repetitive.

Testing for equivalents synchronized with multimedia, such as captions and audio descriptions, can be done by digging into the preferences for your media player to turn on accessibility settings.

Another group of perceivability problems concerns the styling of the page. There are three areas to investigate here:

-   Is the suggested presentation of the page reasonably accessible? For example, is there sufficient color contrast? Is the text comfortably large? In addition to squinting at the page yourself, you can use a tool such as [Juicy Studio CSS Analyser](http://juicystudio.com/services/csstest.php) to check background and foreground color combinations against formulae that purport to measure legibility.
-   Can publisher suggestions for presentation be safely mixed with common user preferences aimed at making content more legible, like increased font size, zoom, and different default colors? Try increasing the text size by about 2–5 steps; don’t worry if the results are not pixel perfect but do worry if the layout is so broken it renders the content hard to read. Try changing your color preferences and see what happens. If publisher CSS sets colors, it should explicitly set background and foreground together to ensure that the combination of unusual preferences and publisher styles do not result in unreadable or invisible text. Popular browsers allow users to enforce their own color preferences and turn off CSS background images. When you try this yourself, it can reveal misconceived CSS image replacement techniques that hide text off-screen, since the image will not be loaded but the text will still be invisible.
-   If publisher suggestions for presentation are discarded, is all the information communicated by such suggestions preserved in the web content for use by the default stylings of the user agent or user styling? Try turning off CSS and inspecting the document object model to check that headings are marked as headings and tables are used for tabulated data not layout.

#### <span>Operability</span>

Health and safety is a crucial, though rarely considered, part of making a website operable. But flashing content risks triggering fits in photosensitive epileptics. You can take a screen capture of your website in use and feed it into the [Trace Center Photosensitive Epilepsy Analysis Tool (PEAT)](http://trace.wisc.edu/peat/) to test if it has flashing content likely to pose a danger to your users. Obviously, this is an especially big concern if you are creating a video sharing website. At the product design stage, you might look at including an automated screening process for uploads.

Beyond that, a good way to test the operability of websites is simply to try to see if you can access all essential content and functionality with different devices:

-   Try using your site with just the keyboard. Is current focus always clearly indicated? Can all functionality be accessed by keyboard?
-   Try using your site with a touchscreen device.
-   Try navigating your webpage with voice commands using Opera for Windows and its Voice add-on, or Windows Vista Speech Recognition and Internet Explorer. (Note: dictation-quality commercial speech recognition has recently been introduced to Mac OS X in the form of MacSpeech Dictate, but there is currently no equivalent on the free \*nix platforms.)

Screen readers and other assistive technology can make use of the semantic structure of (X)HTML to correctly associate content and to enable navigation of content. For example, screen readers can allow users to jump to the next occurrence of headings or other element type, or they can list all occurrences of a certain type. Correct use of `label` and `legend` elements allows assistive technology to associate labels with the correct form fields; correct use of `th` elements and `header`, `scope`, and `axis` attributes allows it to associate table headings with table data cells. Semantic structure may be evaluated with a document object model (DOM) inspector like the one found in Opera Dragonfly. Accessibility inspection tools like the Firefox Accessibility Extension can make such tasks easier by, for example, listing the headings on the page, or listing the attributes of form fields (quickly showing which ones are missing associated labels). See Figure 1 for an example.

![Screenshot of Firefox Accessibility Extensions forms information window with the new BBC homepage](/assets/public/b/b1/firefox-.gif)

Figure 1: Screenshot of Firefox Accessibility Extension’s forms information window with the new BBC homepage.

#### <span>Understandability</span>

Assessing comprehensibility is even more subjective that testing legibility. Unless an evaluator is new to a project or is a professional editor, they are probably not the best person to evaluate whether copy is as understandable as possible. You can however use [Juicy Studio’s Readability Test tool](http://juicystudio.com/services/readability.php) to get a rough idea of how simple your site's copy is.

Some aspects are highly objectively testable however, such as whether content has language metadata that allows (for example) screen readers and voice browsers to read content with the correct pronunciation. With HTML, you could use a DOM inspector to check for the presence of a `lang` attribute for the document and each change of language.

Keep an eye out for inconsistencies in web sites, both in terms of internal consistency and predictability from common web conventions. Screen magnifier users who only see part of a page at a time rely heavily on such consistency in order to know where to look to find given content and functionality.

#### <span>Robustness</span>

Testing whether content is robust involves checking that technologies are being correctly used. At a very basic level, you can run markup and code through linters such as:

-   [WDG HTML Validator with warnings enabled](http://htmlhelp.com/tools/validator/)
-   [W3C CSS Validator](http://jigsaw.w3.org/css-validator/)
-   [JSLint JavaScript linter](http://www.jslint.com/)

Next, you can review code in depth to check that features are used correctly. For example, you can check that HTML native controls are used rather than faking controls with meaningless elements and JavaScript, and that JavaScript uses [feature detection rather than browser sniffing where possible](http://www.jibbering.com/faq/faq_notes/not_browser_detect.html).

Then you can test in multiple user agents and assistive technologies, checking the site is perceivable, operable, and understandable whatever combination of publisher CSS, JavaScript, and plugins are enabled or disabled.

The most common problem is probably obtrusive JavaScript, like anchors and buttons that are in the unscripted markup of the page but depend on JavaScript to actually do anything. But there are more subtle problems that arise from overly close coupling of JavaScript with other layers in the technology stack. For example, JavaScript might apply CSS `display: none;` to hide content, but what happens when publisher CSS is not applied?

Another example is multimedia controls. Often, when plugin content is included, the plugin’s native user interface is disabled and the plugin is instead controlled by scripted HTML widgets. When the plugin content is only added via JavaScript after JavaScript-based plugin detection, this is fine. But sometimes plugin content is included in the pre-scripted state of the page. In such cases, it is worth checking not only that a fallback has been included in case a handling plugin is not available, but also that the native user interface of the plugin is not disabled unless JavaScript is available. If the former is not the case, then users will not see the fallback content at all; if the latter is not true then users will see the plugin but not be able to control it.

## <span>User testing</span>

No amount of developer inspection and screening can substitute for the raw clash between a user and a web site. Given the difficulties of understanding all the subtle interactions between web content and assistive technology and the difficulties of approximating the experience of users with disabilities, this goes double for users with disabilities. If at all possible, you should test your site with real users with disabilities. This can be done on a large and expensive scale, but do not underestimate the benefits of doing even small-scale user testing.

### <span>Recruiting testers</span>

Testers can be found in the same way as you find candidates for usability testing generally (eg through advertising and recruitment agencies). Your local disability organizations should be able to suggest appropriate forums for recruiting test subjects.

Testing is real work and should ideally be compensated as such. A rate of around 70 USD for an hour’s testing is fairly common for user testing.

Having said that you may be able to find people who will test smaller projects for free. There will be people with disabilities among your friends, relatives, and colleagues. In addition, there are online discussion groups dedicated to software accessibility issues, such as:

-   [WebAIM Accessibility Discussion List](http://www.webaim.org/discussion/).
-   [Web Accessibility Initative Interest Group Mailing List](http://www.w3.org/WAI/IG/Overview.html): a forum for discussion of issues relating to Web accessibility.
-   [British Computer Association of the Blind mailing list](http://www.bcab.org.uk/mailing-list.html): for discussing Information Communication Technologies (ICT) for visually impaired people.
-   [Magnifiers Yahoo! Group](http://tech.groups.yahoo.com/group/magnifiers/).
-   [jfw@freelists.org](http://www.freelists.org/archives/jfw/): A mailing list for users of the JAWS screen reader.
-   [GW-Info](http://www.gwmicro.com/Support/Email_Lists/): A mailing list for users of the GW Micro Window-Eyes screen reader.
-   [Dolphin software users Yahoo! Group](http://tech.groups.yahoo.com/group/dolphinusers/).
-   [NVDA users mailing list](http://www.freelists.org/list/nvda).
-   [Thunder users mailing list](http://www.freelists.org/list/thunder).
-   [discuss@macvisionaries.com](http://macvisionaries.com/mailman/listinfo/discuss_macvisionaries.com): A list about use of OS X by the blind.
-   [macvoiceover@freelists.org](http://www.freelists.org/list/macvoiceover): Apple VoiceOver users.
-   [Blinux-list](https://www.redhat.com/mailman/listinfo/blinux-list): A list about the use of Linux by people who are blind and visually impaired.
-   [GNOME Orca users](http://mail.gnome.org/mailman/listinfo/orca-list).
-   [Ai Squared Forums](http://www.aisquared.com/forums/index.php): Including users of the popular ZoomText magnifier.
-   [Deaf-Macs Yahoo! Group](http://tech.groups.yahoo.com/group/Deaf-Macs/): For deaf, hard-of-hearing, and Usher or deafblind Mac Users.
-   [deaf-uk-technology Yahoo! Group](http://groups.yahoo.com/group/deaf-uk-technology/): Deaf-related technology discussion.

Such groups typically welcome questions from web developers about the accessibility of their sites or particular techniques.

### <span>Practical considerations</span>

Remember that the test environment itself needs to be accessible. For example, if you are preparing written test materials, you need to be prepared to offer these in alternative forms. The logistics of replicating the user’s browsing environment at your normal testing location are complicated, so it may be more realistic to test at the user’s home. Failing that, even completely remote testing can be valuable.

One particular consideration that is probably even more important for users with disabilities than other users is what technology they are familiar with. Assistive technology can add many layers of complexities to their computing experience, creating a big divide between novice computer users and old-hands, and dividing users into communities who might be very adept with their own setup but highly disorientated by unfamiliar technology. (Think of how hard users without disabilities that affect their use of computers find it to switch between Mac and PC!)

If you take a longtime user of the Window-Eyes screen reader, sit him in front of an unfamiliar machine with the JAWS screen reader installed and ask him to test a website, it’s going to be very difficult to distinguish his problems with JAWS from his problems with your website. Given the significant differences between versions and given how users often customize their setup, it may be difficult even if you provide Window-Eyes! For this reason, unless you are specifically testing how well your website’s accessibility will hold up in unfamiliar settings (eg in libraries or friends’ computers), it is best to allow users to test with their own setup or something as close as possible to it.

Likewise, unless you specifically want to test novice users or expert users, you should aim to select users who have around a year’s familiarity with using their current setup to access the web. Both assistive technology and the conventions of the web itself are non-trivial to learn. With novice users you will not know whether problems arise from your site or are intrinsic to the learning process, and experts may have tricks up their sleeves that others don’t.

### <span>Choosing tasks</span>

It’s incredibly instructive even to observe users simply exploring a website. As with any other user testing:

-   Try setting the users some specific tasks to accomplish.
-   Ask them what they think and listen to what they say.
-   Pay attention to what they do, because that may differ from what they say: stated preference is a poor guide to performance.

When you design a site, you need to focus on the transactions users want to make with your site rather than the particular controls they need to use. Likewise, when accessibility testing, the tasks you set should (at least initially) reflect the real goals of a visitor using the site, rather than being focused on their interactions with particular controls. These transactions will typically be similar for people with and without disabilities.

For example, if you are testing a video sharing site for accessibility, do not begin by asking them if they can use particular controls (“That’s the volume slider. Can you adjust the volume?”). Instead, give them scenarios and ask them to achieve key user tasks. For example:

-   Browse videos and choose one to play.
-   Search for a video.
-   Upload a video.
-   Pause the video, play the video, mute the video, unmute the video, rewind the video and play it again.
-   Rate a video.
-   Share a video with a friend.

This way, you are likely to uncover lots of problems you had not anticipated. For example, a screen reader user might not be able to find the search box or the controls for the video. Conversely, users might have navigational strategies for dealing with the web you do not even know about.

### <span>Interpreting the results</span>

In an ideal world, we could test every possible combination and get feedback from everybody. But in reality, time and money will limit user testing. Given this, feedback can be a double-edged sword. While it can teach you an enormous amount, there is a real danger of attaching too much weight to one person’s view, which may not be representative of the greater target audience. For example, some screen reader users tend to be looking for an experience streamlined for blind users; others are keen to know everything about the site that their sighted friends and colleagues see.

This is where accessibility standards like WCAG really come into their own. By following such guidelines, you can increase your chances of getting a foundation of accessibility even for user groups you are not able to test.

When you do observe a problem, analyse its causes. For example, your video sharing site includes a page showing popular videos in a data table, with columns including a still, a title, uploaded date, last played date, and overall rating, and arranged in row groups by category of video. In user testing, a screen reader user has trouble using the data table. This could reflect:

-   A problem with the site code. For example, maybe the developers constructed a data table from meaningless `div` elements rather than using proper data table markup. Here the appropriate action would be to recode the table.
-   Inexpertise on the part of the user. For example, a JAWS user might be unfamiliar with JAWS’s features for navigating and reading data tables. Here an appropriate action might be to provide additional documentation or hints for less expert users. If expert users do not make ideal test subjects, they make great consultants on points such as this.
-   A problem with the user agent. For example, Safari exposes data tables to the Apple accessibility model as a series of layout boxes rather than as a set of data relationships. Here appropriate actions would include reporting the bug to the user agent vendor or developers, researching a technique that does work in the user agent, or noting the limitation in documentation and suggesting alternative user agents that do work with your web site.
-   A problem with the screen reader. For example, the developers might have shortened long table headers using the `abbr` attribute, but the screen reader might not provide a user interface for reading the shortened version. Here appropriate actions would include reporting the bug to the screen reader vendor or developers, and might be to find a technique that does work in the screen reader, or to note the limitation in documentation and suggest an alternative tool or navigation strategy that does work.

## <span>Communicating the results of accessibility testing</span>

When communicating the results of accessibility evaluation, document precisely what was evaluated. If you tested conformance with a particular standard, be specific about exactly where conformance has succeeded and failed. Whenever raising a problem, make sure to put it in real, human terms and explain how the problem might adversely affect users. Describe how to reproduce the problem and test for its resolution. Suggest practical techniques for achieving conformance or improving accessibility.

For example, you might report a problem with the video sharing website like this:

-   ***Problem**: The dropdown menu cannot be opened without using a mouse to hover over top menu items, and the keyboard focus disappears off-screen as you tab through the menu.*
-   ***How to reproduce**: Open the page in your browser and attempt to reach a subitem of the menu using the keyboard alone.*
-   ***Explanation**: Web navigation should be device-independent, so that users using devices other than mice—such as blind users or users with motor disabilities—can access content and functionality. Currently, such users can not access the items in submenus and sighted users using the keyboard may be confused when the focus indicator disappears.*
-   ***Conformance implications**: Keyboard operability is a requirement for WCAG 1.0 and WCAG 2.0 Level “A” compliance (see WCAG 1.0 Guideline 9 and WCAG 2.0 Guideline 2.1).*
-   ***Suggested remedies**: When JavaScript is not available, use a simple list of links to subpages for each sublist of navigation. On sub pages, present the main navigation followed by the sublist. When JavaScript is available, remove the sublist from the DOM and add sublists for each menu item on the `click` event, which can be triggered by keyboards, mice, speech recognition, and touch screens alike.*

## <span>Summary</span>

Not every webpage will receive an accessibility evaluation by experts and a suite of paid test subjects. But any web developer can learn the principles of accessibility, attempt to implement those principles in their code, and submit the results of their labours to user mailing lists to learn of further problems, and so feed new knowledge back into future development.

## <span>Exercise questions</span>

-   Try navigating a complex site of your choice without using the mouse. What difficulties do you encounter? How could the developers of the site help you?
-   Turn off CSS and do your normal browsing for a day. What problems do you encounter?
-   Turn off JavaScript and do your normal browsing for a day. What problems do you encounter?
-   Pick a favourite site, design some personas for the site, then evaluate its conformance with WCAG 1.0 and general accessibility as an expert tester. Design a user testing plan for a site, and include recruit requirements and tasks to test. Write up a report on how it could improve its accessibility.

Note: This material was originally published as part of the Opera Web Standards Curriculum, available as [26: Accessibility testing](http://dev.opera.com/articles/view/26-accessibility-testing/), written by Benjamin Hawkes-Lewis. Like the original, it is published under the [Creative Commons Attribution, Non Commercial - Share Alike 2.5](http://creativecommons.org/licenses/by-nc-sa/2.5/) license.