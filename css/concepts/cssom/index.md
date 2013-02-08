The CSSOM API offers a programmatic interface to various CSS
features. A CSSOM ''property name'' corresponds to property names that
appear in style sheets, but uses an alternate camelCase syntax. For
example, the [[css/properties/font-size|'''font-size''']] property is
represented in CSSOM as '''fontSize''', and scripts can directly
assign a value to '''element.style.fontSize'''. (Experimental or
otherwise not fully standardized properties would be represented in
style sheets using [[concepts/vendor_prefix|vendor prefixes]] such as
'''-webkit-font-size''' and '''-moz-font-size''', in which case
corresponding CSSOM prefixes would be '''WebkitFontSize''' and
'''MozFontSize'''.)
Refer to [http://www.w3.org/TR/cssom/ http://www.w3.org/TR/cssom/] for a list of the names.