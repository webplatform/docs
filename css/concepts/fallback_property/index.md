---
title: fallback property
uri: 'css/concepts/fallback property'

---
Supplying a CSS *fallback property* is a common technique to ensure cross-browser compatibility. In the example below, the first [**background-image**](/css/properties/background-image) specifies an image file, which all browsers are able to render. The additional ones after that specify the more recent [**linear-gradient()**](/css/functions/linear-gradient) function, which all browsers may not support. The browser uses those values only if it is able to interpret them, otherwise reverting to the image file value as a fallback.

    div {
        background-image: url(img/gradient.png);
        background-image: -webkit-linear-gradient(to bottom, #dddddd, #aaaaaa);
        background-image: -moz-linear-gradient(to bottom, #dddddd, #aaaaaa);
        background-image: linear-gradient(to bottom, #dddddd, #aaaaaa);
    }

Note here that you can use this fallback technique to apply a mix of standardized or vendor-prefixed properties, whichever works.
