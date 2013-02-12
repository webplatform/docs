{{Page_Title|Internationalization (Ecma 402 standard)}}
{{Flags}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The ECMAScript Internationalization API provides key language-sensitive functionality as a complement to the ECMAScript Language Specification, 5.1 edition or successor. Its functionality has been selected from that of well-established internationalization APIs such as those of the Internationalization Components for Unicode (ICU) library, of the .NET framework, or of the Java platform.}}
{{API_Listing|Use_page_title=Yes
|List_all_subpages=Yes
}}
{{Concept_Listing
|Query=[[Category:Internationalization]][[Category:API_Objects]]
|Use_page_title=No
|List_all_subpages=No
}}
{{Notes_Section
|Usage=The ECMAScript Internationalization API is designed to complement the ECMAScript Language Specification by providing key language-sensitive functionality. The API can be added to an implementation of the ECMAScript Language Specification, 5.1 edition or successor.

The ECMAScript Internationalization API provides three key pieces of language-sensitive functionality that are required in most applications: String comparison (collation), number formatting, and date and time formatting. While the ECMAScript Language Specification provides functions for this basic functionality (String.prototype.localeCompare, Number.prototype.toLocaleString, Date.prototype.toLocaleString, Date.prototype.toLocaleDateString, and Date.prototype.toLocaleTimeString), it leaves the actual behaviour of these functions largely up to implementations to define. The Internationalization API Specification provides additional functionality, control over the language and over details of the behaviour to be used, and a more complete specification of required functionality.

Applications can use the API in two ways:

Directly, by using the constructors Intl.Collator, Intl.NumberFormat, or Intl.DateTimeFormat to construct an object, specifying a list of preferred languages and options to configure the behaviour of the resulting object. The object then provides a main function (compare or format), which can be called repeatedly. It also provides a resolvedOptions function, which the application can use to find out the exact configuration of the object.
Indirectly, by using the functions of the ECMAScript Language Specification mentioned above, which are respecified in this specification to accept the same arguments as the Collator, NumberFormat, and DateTimeFormat constructors and produce the same results as their compare or format methods.
The Intl object is used to package all functionality defined in the ECMAScript Internationalization API to avoid name collisions.
|Notes=The API was developed by an ad-hoc group established by Ecma TC 39 in September 2010 based on a proposal by Nebojša Ćirić and Jungshik Shin.

Internationalization of software is never complete. We expect significant enhancements in future editions of this specification.

Editor

Norbert Lindenberg

Contributors

Eric Albright

Nebojša Ćirić

Peter Constable

Mark Davis

Richard Gillam

Steven Loomis

Mihai Nita

Addison Phillips

Roozbeh Pournader

Jungshik Shin

Shawn Steele

Allen Wirfs-Brock

Feedback provided by Erik Arvidsson, John J. Barton, Zbigniew Braniecki, Marcos Cáceres, Brendan Eich, John Emmons, Gordon P. Hemsley, David Herman, Luke Hoban, Oliver Hunt, Suresh Jayabalan, Yehuda Katz, Mark S. Miller, Andrew Paprocki, Adam Peller, Axel Rauschmayer, Andreas Rossberg, Alex Russell, Markus Scherer, Dmitry Soshnikov, Yusuke Suzuki, John Tamplin, Rick Waldron, Anton Yatsenko, Nicholas Zakas.

This Ecma Standard has been adopted by the General Assembly of December 2012.
}}
{{See_Also_Section}}
{{Topics|Internationalization, JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}