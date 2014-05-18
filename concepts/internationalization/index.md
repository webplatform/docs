{{Page_Title|Internationalization and Localization}}
{{Flags}}
{{Summary_Section|Terminology and best practices}}
{{Basic Page}}
==Terminology==
'''Internationalization''' (abbreviated '''i18n''', where 18 is the number of left out characters) is the design and development of a product, application or document content that enables easy localization for target audiences that vary in culture, region, or language.

'''Localization''' (abbreviated '''l10n''', where 10 is the number of left out characters) is the adaptation of a product, application or document content for a specific target audience. This includes language related aspects (translations, different characters and scripts), cultural aspects (different units, currencies, time and date formats, meaning of colors and symbols, suitability of images), and legal requirements.

Example: Internationalization is ''constructing'' a car in a way to make it possible to build in the steering wheel on either side. Localization is ''building'' cars with steering wheels on the right-hand side for a market with right-hand traffic.

Further reading: [http://www.w3.org/International/questions/qa-i18n Localization vs. Internationalization]

==Best Practices==
Use UTF-8 as character encoding. In each part of your system (data base, web pages). This allows you to use each Unicode character without escaping. [http://www.w3.org/International/questions/qa-escapes#not When not to use escapes]

Use language negotiation on multilingual Web sites. [http://www.w3.org/International/questions/qa-when-lang-neg When to use language negotiation]

Declare the language of your content with the lang attribute. This is useful for spell checkers, screen readers, automatic hyphenation, … [http://www.w3.org/International/questions/qa-lang-why Why use the language attribute?]

Further reading: [http://www.w3.org/International/quicktips/Overview Internationalization Quick Tips for the Web]

{{Notes_Section}}
{{Topics|Internationalization}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}