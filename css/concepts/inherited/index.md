---
title: 'inherited'
uri: css/concepts/inherited

---
Many CSS properties *inherit* (or *cascade*) their values from their parent element. For example, a block **div** element may specify one [**font-size**](/css/properties/font-size) value, which one of its child **p** elements may override with another. Applying the built-in **inherited** keyword as a value for this **p** element would then reapply the value inherited from the parent. (Alternately, applying the **inherited** keyword to non-inherited properties yields the [initial value](/css/concepts/initial_value).)
