=HTML5=

==Summary==

HTML5 is the newest revision of the HyperText Markup Language. It updates and replaces HTML 4.01 and XHTML 1.1. It is being standardized at W3C, and jointly developed by W3C and WHATWG. It is currently in W3C's [[Standards/W3C_Process#Candidate_Recommendation|Candidate Recommendation]] phase, and is expected to be finalized as a [[Standards/W3C_Process#Recommendation|Recommendation]] in 2014.

For more information, there is a developer-friendly version of the spec, [http://www.w3.org/TR/html-markup/ HTML: The Markup Language], and a [http://www.w3.org/TR/html5-diff/ HTML5 differences from HTML4] document to find out what's changed.

To get started using HTML5, you can read our [[HTML tutorials]].

Here is a summary of which features are new, changed, or even obsolete in HTML5.

==Elements==
===New Elements=== 
There are 47 new elements in HTML5:
* '''[[html/elements/article|article]]:''' article
* '''[[html/elements/aside|aside]]:''' tangential content
* '''[[html/elements/audio|audio]]:''' audio stream
* '''[[html/elements/bdi|bdi]]:''' BiDi isolate
* '''[[html/elements/canvas|canvas]]:''' canvas for dynamic graphics
* '''[[html/elements/command type=checkbox|command type=checkbox]]:''' state or option that can be toggled
* '''[[html/elements/command type=command|command type=command]]:''' command with an associated action
* '''[[html/elements/command type=radio|command type=radio]]:''' selection of one item from a list of items
* '''[[html/elements/command|command]]:''' command
* '''[[html/elements/datalist|datalist]]:''' predefined options for other controls
* '''[[html/elements/details|details]]:''' control for additional on-demand information
* '''[[html/elements/embed|embed]]:''' integration point for plugins
* '''[[html/elements/figcaption|figcaption]]:''' figure caption
* '''[[html/elements/figure|figure]]:''' figure with optional caption
* '''[[html/elements/footer|footer]]:''' footer
* '''[[html/elements/header|header]]:''' header
* '''[[html/elements/hgroup|hgroup]]:''' heading group
* '''[[html/elements/input type=color|input type=color]]:''' color-well control
* '''[[html/elements/input type=datetime-local|input type=datetime-local]]:''' local date-and-time input control
* '''[[html/elements/input type=datetime|input type=datetime]]:''' global date-and-time input control
* '''[[html/elements/input type=date|input type=date]]:''' date input control
* '''[[html/elements/input type=email|input type=email]]:''' e-mail address input control
* '''[[html/elements/input type=month|input type=month]]:''' year-and-month input control
* '''[[html/elements/input type=number|input type=number]]:''' number input control
* '''[[html/elements/input type=range|input type=range]]:''' imprecise number-input control
* '''[[html/elements/input type=search|input type=search]]:''' search field
* '''[[html/elements/input type=tel|input type=tel]]:''' telephone-number-input field
* '''[[html/elements/input type=time|input type=time]]:''' time input control
* '''[[html/elements/input type=url|input type=url]]:''' URL input control
* '''[[html/elements/input type=week|input type=week]]:''' year-and-week input control
* '''[[html/elements/keygen|keygen]]:''' key-pair generator/input control
* '''[[html/elements/mark|mark]]:''' marked (highlighted) text
* '''[[html/elements/meta charset|meta charset]]:''' document character-encoding declaration
* '''[[html/elements/meter|meter]]:''' scalar gauge
* '''[[html/elements/nav|nav]]:''' group of navigational links
* '''[[html/elements/output|output]]:''' result of a calculation in a form
* '''[[html/elements/progress|progress]]:''' progress indicator
* '''[[html/elements/rp|rp]]:''' ruby parenthesis
* '''[[html/elements/rt|rt]]:''' ruby text
* '''[[html/elements/ruby|ruby]]:''' ruby annotation
* '''[[html/elements/section|section]]:''' section
* '''[[html/elements/source|source]]:''' media source
* '''[[html/elements/summary|summary]]:''' summary, caption, or legend for a details control
* '''[[html/elements/time|time]]:''' date and/or time
* '''[[html/elements/track|track]]:''' supplementary media track
* '''[[html/elements/video|video]]:''' video
* '''[[html/elements/wbr|wbr]]:''' line-break opportunity

===Changed Elements=== 
There are 11 elements that were changed in HTML5:
* '''[[html/elements/a|a]]:''' hyperlink
* '''[[html/elements/b|b]]:''' offset text conventionally styled in bold
* '''[[html/elements/cite|cite]]:''' cited title of a work
* '''[[html/elements/hr|hr]]:''' thematic break
* '''[[html/elements/input|input]]:''' input control
* '''[[html/elements/i|i]]:''' offset text conventionally styled in italic
* '''[[html/elements/menu|menu]]:''' list of commands
* '''[[html/elements/meta|meta]]:''' metadata
* '''[[html/elements/small|small]]:''' small print
* '''[[html/elements/s|s]]:''' struck text
* '''[[html/elements/u|u]]:''' offset text conventionally styled with an underline

===Obsolete Elements=== 
Several existing elements were declared obsolete in HTML5, though for the sake of completeness and handling legacy content, they are still defined in the specification. However, authors should not use these elements.

There are different reasons for these elements being made obsolete: 
# they are purely presentational, and CSS should be used instead
# they harm usability and accessibility
# they are confusing, duplicative, or rarely used

There are 13 elements made obsolete in HTML5:
* '''[[html/elements/acronym|acronym]]:'''  ''duplicate''. Use [[html/elements/abbr|abbr]] for abbreviations instead
* '''[[html/elements/applet|applet]]:'''  ''duplicate''. Use [[html/elements/object|object]] instead
* '''[[html/elements/basefont|basefont]]:''' ''presentational''. Use [[css|CSS]] instead
* '''[[html/elements/big|big]]:''' ''presentational''. Use [[css/properties/font-size|CSS font-size]] instead 
* '''[[html/elements/center|center]]:''' ''presentational''. Use [[css/properties/align|CSS align]] instead 
* '''[[html/elements/dir|dir]]:'''  ''duplicate''. Use [[html/elements/ul|ul]] instead
* '''[[html/elements/font|font]]:''' ''presentational''. Use [[css/properties/font-family|CSS font-family]] instead 
* '''[[html/elements/frameset|frameset]]:''' ''harmful'' 
* '''[[html/elements/frame|frame]]:''' ''harmful''  
* '''[[html/elements/isindex|isindex]]:'''  ''duplicate''. Use form controls instead
* '''[[html/elements/noframes|noframes]]:''' ''harmful''  
* '''[[html/elements/strike|strike]]:''' ''presentational''. Use [[css|CSS]] instead  
* '''[[html/elements/tt|tt]]:''' ''presentational''. Use [[css|CSS]] instead 

===Existing Elements=== 
There are 84 unchanged elements in HTML5:
* '''[[html/elements/abbr|abbr]]:''' abbreviation
* '''[[html/elements/address|address]]:''' contact information
* '''[[html/elements/area|area]]:''' image-map hyperlink
* '''[[html/elements/base|base]]:''' base URL
* '''[[html/elements/bdo|bdo]]:''' BiDi override
* '''[[html/elements/blockquote|blockquote]]:''' block quotation
* '''[[html/elements/body|body]]:''' document body
* '''[[html/elements/br|br]]:''' line break
* '''[[html/elements/button type=button|button type=button]]:''' button with no additional semantics
* '''[[html/elements/button type=reset|button type=reset]]:''' reset button
* '''[[html/elements/button type=submit|button type=submit]]:''' submit button
* '''[[html/elements/button|button]]:''' button
* '''[[html/elements/caption|caption]]:''' table title
* '''[[html/elements/code|code]]:''' code fragment
* '''[[html/elements/colgroup|colgroup]]:''' table column group
* '''[[html/elements/col|col]]:''' table column
* '''[[html/elements/dd|dd]]:''' description or value
* '''[[html/elements/del|del]]:''' deleted text
* '''[[html/elements/dfn|dfn]]:''' defining instance
* '''[[html/elements/div|div]]:''' generic flow container
* '''[[html/elements/dl|dl]]:''' description list
* '''[[html/elements/dt|dt]]:''' term or name
* '''[[html/elements/em|em]]:''' emphatic stress
* '''[[html/elements/fieldset|fieldset]]:''' set of related form controls
* '''[[html/elements/form|form]]:''' user-submittable form
* '''[[html/elements/h1|h1]]:''' heading
* '''[[html/elements/h2|h2]]:''' heading
* '''[[html/elements/h3|h3]]:''' heading
* '''[[html/elements/h4|h4]]:''' heading
* '''[[html/elements/h5|h5]]:''' heading
* '''[[html/elements/h6|h6]]:''' heading
* '''[[html/elements/head|head]]:''' document metadata container
* '''[[html/elements/html|html]]:''' root element
* '''[[html/elements/iframe|iframe]]:''' nested browsing context (inline frame)
* '''[[html/elements/img|img]]:''' image
* '''[[html/elements/input type=button|input type=button]]:''' button
* '''[[html/elements/input type=checkbox|input type=checkbox]]:''' checkbox
* '''[[html/elements/input type=file|input type=file]]:''' file upload control
* '''[[html/elements/input type=hidden|input type=hidden]]:''' hidden input control
* '''[[html/elements/input type=image|input type=image]]:''' image-coordinates input control
* '''[[html/elements/input type=password|input type=password]]:''' password-input field
* '''[[html/elements/input type=radio|input type=radio]]:''' radio button
* '''[[html/elements/input type=reset|input type=reset]]:''' reset button
* '''[[html/elements/input type=submit|input type=submit]]:''' submit button
* '''[[html/elements/input type=text|input type=text]]:''' text-input field
* '''[[html/elements/ins|ins]]:''' inserted text
* '''[[html/elements/kbd|kbd]]:''' user input
* '''[[html/elements/label|label]]:''' caption for a form control
* '''[[html/elements/legend|legend]]:''' title or explanatory caption
* '''[[html/elements/link|link]]:''' inter-document relationship metadata
* '''[[html/elements/li|li]]:''' list item
* '''[[html/elements/map|map]]:''' image-map definition
* '''[[html/elements/meta http-equiv=content-type|meta http-equiv=content-type]]:''' document character-encoding declaration
* '''[[html/elements/meta http-equiv=default-style|meta http-equiv=default-style]]:''' “preferred stylesheet” pragma directive
* '''[[html/elements/meta http-equiv=refresh|meta http-equiv=refresh]]:''' “refresh” pragma directive
* '''[[html/elements/meta name|meta name]]:''' name-value metadata
* '''[[html/elements/noscript|noscript]]:''' fallback content for script
* '''[[html/elements/object|object]]:''' generic external content
* '''[[html/elements/ol|ol]]:''' ordered list
* '''[[html/elements/optgroup|optgroup]]:''' group of options
* '''[[html/elements/option|option]]:''' option
* '''[[html/elements/param|param]]:''' initialization parameters for plugins
* '''[[html/elements/pre|pre]]:''' preformatted text
* '''[[html/elements/p|p]]:''' paragraph
* '''[[html/elements/q|q]]:''' quoted text
* '''[[html/elements/samp|samp]]:''' (sample) output
* '''[[html/elements/script|script]]:''' embedded script
* '''[[html/elements/select|select]]:''' option-selection form control
* '''[[html/elements/span|span]]:''' generic span
* '''[[html/elements/strong|strong]]:''' strong importance
* '''[[html/elements/style|style]]:''' style (presentation) information
* '''[[html/elements/sub|sub]]:''' subscript
* '''[[html/elements/sup|sup]]:''' superscript
* '''[[html/elements/table|table]]:''' table
* '''[[html/elements/tbody|tbody]]:''' table row group
* '''[[html/elements/td|td]]:''' table cell
* '''[[html/elements/textarea|textarea]]:''' text input area
* '''[[html/elements/tfoot|tfoot]]:''' table footer row group
* '''[[html/elements/thead|thead]]:''' table heading group
* '''[[html/elements/th|th]]:''' table header cell
* '''[[html/elements/title|title]]:''' document title
* '''[[html/elements/tr|tr]]:''' table row
* '''[[html/elements/ul|ul]]:''' unordered list
* '''[[html/elements/var|var]]:''' variable or placeholder text

==Attributes==
===New Attributes===
===Changed Attributes===
===Obsolete Attributes===
===Existing Attributes===

==APIs==
===New APIs===