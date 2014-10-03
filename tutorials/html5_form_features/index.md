{{Page_Title|HTML5 form features}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|Content=Errors
}}
{{Byline
|Name=
|URL=
|Published=
}}
{{Summary_Section|In this tutorial we will take you through the new HTML5 form features.}}
{{Guide
|Content=== Introduction ==

HTML5 includes many new features that make web forms much easier to write, and more powerful and consistent across the Web. 
This article gives a brief overview of some of the new form controls and functionalities that have been introduced.

== Why did we need new form features? ==
 
Let's face it, HTML forms have always been a pain. They are not much fun to mark up and they can be fiddly to style &mdash; especially if you want 
them to be consistent across browsers and fit in with the overall look and feel of your site. And they can be frustrating for your end users to fill 
out, even if you create them with care and consideration to make them as usable and accessible as possible. Creating a good form is more about damage 
limitation than pleasurable user experiences.
 
Back when HTML 4.01 became a stable recommendation, the web was a mostly static place. Yes, there was the odd comment form or guest book script, but 
generally web sites were just there for visitors to read. Since then, the web has evolved. For many people, the browser has already become a window 
into a world of complex, web-based applications that bring them an almost desktop-like experience.
 
[[Image:html5formfig1.png|Some complicated non-native form controls, faked with JavaScript]]
 
''Figure 1: Some complicated non-native form controls, faked with JavaScript.''
 
To fill the need for the more sophisticated controls required for such applications, developers have been taking advantage of JavaScript libraries 
and frameworks such as jQueryUI and YUI. These solutions have certainly matured over the years, but essentially they're a workaround to compensate 
for the limited form controls available in HTML. They "fake" the more complex widgets like date pickers and sliders by layering additional 
(but not always semantic) markup and a lot of JavaScript on top of pages.
 
HTML5 aims to standardise some of the most common rich form controls, making them render natively in the browser and obviating the need for these 
script-heavy workarounds.

== Introducing our example ==
 
To illustrate some of the new features, this article builds a basic HTML5 forms example. It's not meant to represent a "real" form (as you'd be 
hard-pressed to find a situation where you need all the new features in a single form), but it should give you an idea of how the various new 
aspects look and behave.
 
Note: The look and feel of the new form controls and validation messages differs from brower to browser, so styling your forms to look reasonably 
consistent across browsers still needs careful consideration.

== New form controls ==
 
As forms are the main tool for data input in web applications, and as the data we want to collect has become more complex, it has been necessary 
to create an input element with more capabilities, to collect the data with more semantics and better definition, and to allow for easier, more 
effective validation and error management.
 
=== &lt;input type="number"&gt; ===
 
The first new input type we'll discuss is <code>type="number"</code>:
 
<syntaxhighlight lang="html5"><input type="number" ... ></syntaxhighlight>
 
This input type creates a special kind of input field for number entry &mdash; in most supporting browsers this appears as a text entry field with 
a "spinner" control, which allows you to increment and decrement its value.
 
[[Image:html5formfig2.png|A number input type]]
 
''Figure 2: A <code>number</code> input type.''

=== &lt;input type="range"&gt; ===
 
Creating a slider control to allow you to choose among a range of values used to be a complicated, semantically dubious proposition, 
but with HTML5 it is easy &mdash; you just use the <code>range</code> input type:
 
<syntaxhighlight lang="html5"><input type="range" ... ></syntaxhighlight>
 
[[Image:html5formfig3.png|A range input type]]
 
''Figure 3: A <code>range</code> input type.''
 
Note that, by default, this input does not generally show the currently selected value, or even the range of values it covers. Authors must 
provide these through other means; for instance, to display the current value, we could use an <code>&lt;output&gt;</code> element together 
with some JavaScript to update its display whenever the user interacts with the form:
 
<syntaxhighlight lang="html5"><form oninput="output.value = weight.value">
    <input type="range" id="weight">
    <output id="output"></output>
</form></syntaxhighlight>

=== &lt;input type="date"&gt; and other date/time controls ===
 
HTML5 has a number of different input types for creating complicated date/time pickers, like the kind of you see featured on most
flight/train booking sites. These used to be created using unsemantic kludges, so it is great that we now have standardized, easy ways 
to do this. For example:
 
<syntaxhighlight lang="html5"><input type="date" ... >
<input type="time" ... ></syntaxhighlight>
 
Respectively, these create a fully functioning date picker, and a text input containing a separator for hours, minutes, and seconds 
(depending on the <code>step</code> attribute specified) that only allows you to input a time value.
 
[[Image:html5formfig4.png|date and time input types]]
 
''Figure 4: <code>date</code> and <code>time</code> input types.''
 
But it doesn't end here &mdash; there are a number of other related input types available:
 
* <code>datetime</code>: combines the functionality of the two we looked at above, allowing you to choose a date and a time.
* <code>month</code>: allows you to choose a month, stored internally as a number between 1-12, although different browsers may provide you with more elaborate choosing mechanisms, like a scrolling list of the month names.
* <code>week</code>: allows you to choose a week, stored internally in the format 2010-W37 (week 37 of the year 2010), and chosen using a similar datepicker to the ones we have seen already.

=== &lt;input type="color"&gt; ===
 
This input type brings up a color picker. Opera's implementation allows the user to pick from a selection of colors, enter hexadecimal values 
directly in a text field, or invoke the operating system's native color picker.

[[Image:html5formfig5.png|a color input, and the native color pickers on Windows and OS X]]

''Figure 5: a <code>color</code> input, and the native color pickers on Windows and OS X.''

=== <input type="search"> ===
 
This input type is arguably nothing more than a differently-styled text input. Browsers are meant to style these inputs the same way as any 
OS-specific search functionality. Beyond this purely aesthetic consideration, though, it's still important to note that marking up search fields 
explicitly opens up the possibility for browsers, assistive technologies, or automated crawlers to do something clever with these inputs 
in the future. For instance, a browser could conceivably offer the user a choice to automatically create a custom search for a specific site.
 
[[Image:html5formfig6.png|A search input as it appears in Opera on OS X]]
 
''Figure 6: A <code>search</code> input as it appears in Opera on OS X.''

=== The &lt;datalist&gt; element and list attribute ===
 
So far we have been used to using <code>&lt;select&gt;</code> and <code>&lt;option&gt;</code> elements to create dropdown lists of options for our 
users to choose from. But what if we wanted to create a list that allowed users to choose from a list of suggested options, as well as being able to 
type in their own? That used to require a lot of fiddly scripting, but now you can simply use the <code>list</code> attribute to connect an ordinary 
input to a list of options, defined inside a <code>&lt;datalist&gt;</code> element.

<syntaxhighlight lang="html5"><input type="text" list="mydata" ... >
<datalist id="mydata">
    <option label="Mr" value="Mister">
    <option label="Mrs" value="Mistress">
    <option label="Ms" value="Miss">
</datalist></syntaxhighlight>
 
[[Image:html5formfig7.png|Creating an input element with preset options using datalist]]
 
''Figure 7: Creating an input element with suggestions using <code>datalist</code>.''

=== &lt;input type="tel"&gt;, &lt;input type="email"&gt; and &lt;input type="url"&gt; ===
 
As their names imply, these new input types relate to telephone numbers, email addresses, and URLs. Browsers will render these as normal text inputs, 
but explicitly stating what kind of text we're expecting in these fields plays an important role in client-side form validation. Additionally, on
certain mobile devices the browser will switch from its regular text entry on-screen keyboard to the more context-relevant variants. Again, it's
conceivable that in the future browsers will take further advantage of these explicitly marked-up inputs to offer additional functionality, such as
autocompleting email addresses and telephone numbers based on the user's contacts list or address book.

== New attributes ==
 
In addition to the explicit new input types, HTML5 defines a series of new attributes for form controls that help simplify some common tasks and
further specify the expected values for certain entry fields.
 
=== placeholder ===
 
A common usability trick in web forms is to have placeholder content in text entry fields &mdash; for instance, to give more information about the 
expected type of information we want the user to enter &mdash; which disappears when a user starts entering a value or when the form control gets 
focus. While this used to require some JavaScript (clearing the contents of the form field on focus and resetting it to the default text if the user 
left the field without entering anything), we can now simply use the <code>placeholder</code> attribute:
 
<syntaxhighlight lang="html5"><input type="text"... placeholder="John Doe"></syntaxhighlight>
 
[[Image:html5formfig8.png|A text input with placeholder text]]
 
''Figure 8: A text input with <code>placeholder</code> text.''

=== autofocus ===
 
Another common feature that previously had to rely on scripting is having a form field automatically focused when a page is loaded. This can now be 
achieved very simply with the <code>autofocus</code> attribute:
 
<syntaxhighlight lang="html5"><input type="text" autofocus ... ></syntaxhighlight>
 
Keep in mind that you shouldn't have more than one <code>autofocus</code> form control on a single page. You should also use this sort of 
functionality with caution, especially in situations where a form represents the main area of interest in a page. A search page is a good example 
&mdash; provided that there isn't a lot of content and explanatory text, it makes sense to set the focus automatically to the text input of the 
search form.
 
=== min and max ===
 
As their names suggest, this pair of attributes allows you to set a lower and upper bound for the values that can be entered into a numerical form 
field, like a number, range, time or date input types. Yes, you can even use it to set upper and lower bounds for dates &mdash; for instance, on a 
travel booking form you could limit the datepicker to only allow the user to select future dates. For <code>range</code> inputs, <code>min</code> 
and <code>max</code> are actually necessary to define what values are returned when the form is submitted. The code is pretty simple and 
self-explanatory:
 
<syntaxhighlight lang="html5"><input type="number" ... min="1" max="10"></syntaxhighlight>
 
=== step ===
 
The <code>step</code> attribute can be used with a numerical input value to dictate how granular the values you can input can be. 
For example, you might want users to enter a particular time, but only in 30 minute increments. In this case, we can use the <code>step</code> 
attribute, keeping in mind that for <code>time</code> inputs the value of the attribute is in seconds:
 
<syntaxhighlight lang="html5"><input type="time" ... step="1800"></syntaxhighlight>
 
== New output mechanisms ==
 
Beyond the new form controls that users can interact with, HTML5 defines a series of new elements specifically meant to display and visualise 
information to the user.
 
=== &lt;output&gt; ===
 
We already mentioned the <code>&lt;output&gt;</code> element when talking about the <code>range</code> input type &mdash; this element serves 
as a way to display the result of a calculation or, more generally, to provide an explicitly identified output of a script (rather than simply 
pushing some text into in a random <code>span</code> or <code>div</code>). To make it even more explicit what particular form controls the 
<code>&lt;output&gt;</code> relates to, we can (in a similar way to <code>&lt;label&gt;</code>) pass a list of <code>ID</code>s in the element's 
optional <code>for</code> attribute.
 
<syntaxhighlight lang="html5"><input type="range" id="rangeexample" ... >
<output onforminput="value=rangeexample.value" for="rangeexample"></output></syntaxhighlight>
 
=== &lt;progress&gt; and &lt;meter&gt; ===
 
These two new elements are very similar, both resulting in a gauge/bar being presented to the user. Their distinction is in their intended purpose. 
As the name suggests, <code>progress</code> is meant to represent a progress bar, to indicate the percentage of completion of a particular task, 
while meter is a more generic indicator of a scalar measurement or fractional value.
 
[[Image:html5formfig9.png|A progress indicator bar]]
 
''Figure 9: A progress indicator bar.''

== Validation ==
 
Form validation is very important on both client- and server-side, to help legitimate users avoid and correct mistakes, and to prevent malicious 
users from submitting data that could cause damage to the application. As browsers can now get an idea of what types of values are expected from 
the various form controls (be it their <code>type</code>, or any upper/lower bounds set on numerical values, dates and times), they can also offer 
native form validation &mdash; another tedious task that, up to now, required authors to write reams of JavaScript or use some ready-made 
validation script or library.
 
Note: For form controls to be validated, they must have a <code>name</code> attribute, as without it they wouldn't be submitted as part of the 
form anyway.
 
=== required ===
 
One of the most common aspects of form validation is the enforcement of required fields &mdash; not allowing a form to be submitted until certain 
pieces of information have been entered. This can now simply be achieved by adding the <code>required</code> attribute to an <code>input</code>, 
<code>select</code> or <code>textarea</code> element.
 
<syntaxhighlight lang="html5"><input type="text" ... required></syntaxhighlight>
 
[[Image:html5formfig10.png|Opera's client-side validation in action, showing an error for a required field that was left empty]]

''Figure 10: Opera's client-side validation in action, showing an error for a required field that was left empty.''

=== type and pattern ===
 
As we've seen, authors can now specify the kinds of entries they expect from their form fields. Rather than simply defining text inputs, 
authors can explicitly create inputs for things like numbers, email addresses, and URLs. As part of their client-side validation, browsers can now 
check that what the user entered in these more specific fields matches the expected structure. In essence, browsers can evaluate the input values 
against a built-in pattern that defines what valid entries in those types of inputs look like, and can warn a user when their entry doesn't meet 
the criteria.
 
[[Image:html5formfig11.png|Opera's error message for invalid email addresses in an email input]]
 
''Figure 11: Opera's error message for invalid email addresses in an <code>email</code> input.''
 
For other text entry fields that nonetheless need to follow a certain structure (for instance, login forms where the usernames can only contain a
specific sequence of lowercase letters and numbers), authors can use the <code>pattern</code> attribute to specify their own custom regular 
expression.
 
<syntaxhighlight lang="html5"><input type="text" ... pattern="[a-z]{3}[0-9]{3}"></syntaxhighlight>

== Browser support ==
 
On the desktop, [[http://www.opera.com Opera]] currently has the most complete implementation of new input types and native client-side validation, 
but support is on the way for all other major browsers as well, so it won't be long before we can take advantage of these new powerful tools in our 
projects. But what about older browser versions?
 
By design, browsers that don't understand the new input types like <code>date</code> or <code>number</code> will simply fall back to treating 
them as standard text inputs &mdash; not as user-friendly as their advanced HTML5 counterparts, but at the very least they allow for a form to 
be filled in.

==Conclusion==
In this article, you've seen the new HTML5 form elements and attributes and learned how to use them. For a more general treatment of
standard HTML forms, please see the previous article [[guides/html_forms_basics|HTML forms basics]].
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=autofocus
|Chrome_supported=Yes
|Chrome_version=5.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.6
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.0
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=<datalist>
|Chrome_supported=Yes
|Chrome_version=20.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=<meter>
|Chrome_supported=Yes
|Chrome_version=8.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=15.0
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.2
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=min, max and step
|Chrome_supported=Yes
|Chrome_version=5.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.6
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=<output>
|Chrome_supported=Yes
|Chrome_version=13.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=6.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.2
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=pattern
|Chrome_supported=Yes
|Chrome_version=10
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.01
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=placeholder
|Chrome_supported=Yes
|Chrome_version=4.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.6
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=<progress>
|Chrome_supported=Yes
|Chrome_version=6.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=6.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.6
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.2
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=required
|Chrome_supported=Yes
|Chrome_version=6.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.6
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=type="color"
|Chrome_supported=Yes
|Chrome_version=20.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.0
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=type="date"
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=type="email"
|Chrome_supported=Yes
|Chrome_version=5.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.62
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=type="number"
|Chrome_supported=Yes
|Chrome_version=7.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=type="range"
|Chrome_supported=Yes
|Chrome_version=5.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=23
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.1
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=type="search"
|Chrome_supported=Yes
|Chrome_version=5.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.01
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=type="tel"
|Chrome_supported=Yes
|Chrome_version=5.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.01
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=type="url"
|Chrome_supported=Yes
|Chrome_version=5.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.62
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=autofocus
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=<datalist>
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=10.0
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=<meter>
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=11.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=min, max and step
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=<output>
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=4.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=5
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=pattern
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=placeholder
|Android_supported=Yes
|Android_version=3.2
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=2.1
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=<progress>
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=6.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=11
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=required
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=type="color"
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=type="date"
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=5.0
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=type="email"
|Android_supported=Yes
|Android_version=3.1
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.1
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=type="number"
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=type="range"
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=5.0
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=type="search"
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=type="tel"
|Android_supported=Yes
|Android_version=3.1
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.1
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=type="url"
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=12
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections==== Exercise Questions ===
 
* Why is it a good idea to mark up menus as lists?
* When you design a navigation menu, what do you need to plan for in the future?
* What are the benefits of using <code>&lt;select&gt;</code> elements for menus, and what are the problems?
* What do you define with <code>&lt;area&gt;</code> elements, and what is the <code>nohref</code> attribute of an area element for (this is not in here, you'd need to do some online research)
* What are the benefits of skip links?
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}