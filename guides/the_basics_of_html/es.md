---
title: 'the basics of html'
lang: es
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'The HTML head element'
uri: 'guides/the basics of html/es'

---
## Introdución

En este artículo se resume el propósito y la estructura de HTML, incluyendo cómo funcionan los elementos, así como lo que caracteres de referencia son. Los artículos que siguen profundizarán con mucho más detalles en partes específicas del Lenguaje HTML.

## ¿Qué es HTML

La mayoría de las aplicaciones de escritorio que leen y escriben archivos, usan un formato de Archivo especial. Por ejemplo, Microsoft Word entiende archivos “.doc” y Microsoft Excel entiende “.xls”. Estos archivos contienen las instrucciones sobre cómo reconstruir los documentos la próxima vez que se abran, lo que contiene el documento y “metadatos” acerca del artículo tales como el autor, la fecha de la última vez que el documento fue modificado, incluso cosas como una lista de los cambios realizados para que pueda ir y venir entre versiones.

    HTML (“HyperText Markup Language”) Es un lenguaje para describir el contenido de los documentos web. Utiliza una sintaxis que contiene marcadores (llamados “elementos”), que se envuelven alrededor del texto dentro del documento para indicar al agente de usuario (ej. web browsers) como debería interpretar esa porción del documento.

    Un agente de usuario es cualquier software que es utilizado para acceder a páginas web en nombre de los usuarios. Hay una importante distinción que debe hacerse aquí —Todos los tipos de navegadores de escritorio (Internet Explorer, Opera, Firefox, Safari, Chrome etc.) y los navegadores alternativos para otros dispositivos(tales como el canal de internet de Wii, el navegador de un dispositivo móvil como Opera Mini y WebKit en el Iphone) son agentes de usuario, pero no todos los agente de usuario son web browsers. Los programas automáticos que Google y Yahoo! utilizan para indexar la web en sus motores de búsqueda, también son agentes de usuario, pero ningún ser humano lo está controlando directamente

## ¿Qué aspecto tiene HTML?

    HTML is sólo una representación sin formato del contenido y su significado general. Por ejemplo

``` html
<p id="ejemplo">Esto es un parrafo.</p>
```

 El “`<p>`” es un marcador(Nos referimos a un“tag” o “etiqueta”) que significa que “lo que sigue debe considerarse como un párrafo. Debido a que se encuentre al principio del contenido que está afectando, esta particular etiqueta es una “etiqueta de apertura”. El“`</p>`” es una etiqueta que indica donde termina el párrafo, nos referimos a este tag como “etiqueta de cierre”. La etiqueta de apertura, la etiqueta de cierre y todo lo que está entre las etiquetas es llamado un “elemento”. Esto es un atributo `id="example"`; aprenderás más de esto más adelante. Muchas personas usan el término elemento y etiqueta indistintamente, sin embargo eso no es correcto.

En la mayoría de los navegadores hay una opción "Código fuente" o "Ver código fuente", comúnmente se encuentra en el menú “Ver”. Inténtalo ahora - Ve a tu sitio web favorito, y pasa un tiempo echándole un vistazo al HTML que compone la estructura de una página web.

## La estructura de un documento HTML

Un ejemplo típico de un documento HTML se parece a esto:

``` html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Example page</title>
  </head>
  <body>
    <h1>Hello world</h1>
  </body>
</html>
```

 El código de arriba cuando se muestra en el navegador se parece a esto:

![HTMLrender.png](//static.webplatform.org/a/ab/HTMLrender.png)

El documento empieza con el elemento “\<!DOCTYPE html\>”. Esto sirve sobre todo para que el navegador muestre el HTML en el llamado “modo estándar”, para que funcione correctamente. También le permite al software de validación saber con qué versión de HTML validar tu código. No te preocupes mucho acerca de lo que esto significa por ahora. Volveremos a esto más adelante. Lo que puedes ver aquí es el doctype de HTML5.

Después de esto puedes ver la apertura del etiqueta `html` Esto se envuelve alrededor del documento entero. La etiqueta de cierre `html` es la última cosa en cualquiera documento HTML. El elemento HTML debería siempre tener el atributo`lang`. Este atributo especifica el lenguaje principal para la página. Por ejemplo: `es` significa “Español” `en` significa "Inglés", `fr` significa "Francés". Hay herramientas disponibles que te ayudarán a encontrar la etiqueta de idioma adecuada como Richard Ishida's [Language Subtag Lookup tool](http://rishida.net/utils/subtags/).

Dentro del elemento `html` hay un elemento `head` Este es un contenedor para contener la información acerca del documento (los metadatos). Esto está descrito con más detalles en[The HTML head element](/w/index.php?title=The_HTML_head_element&action=edit&redlink=1). Dentro de head está el elemento título`title` , Que define el título en la barra de menú “Example page”. Tú elemento `head` siempre debe contener el elemento`meta` con el atributo `charset` que identifica la codificación de caracteres de la página.(La única excepción es cuando la página está codificada en UTF-16, pero de todos modos se debe evitar que la codificación quede vacía. Debes utilizar UTF-8 siempre que sea posible. Lee más acerca de [character encodings](http://www.w3.org/International/getting-started/characters).

Después del elemento `head` ha un elemento body `body` que contiene el contenido actual de la página —en este caso el elemento título de nivel 1 (`h1`) que contiene el texto “Hello world.”

Y ese es nuestro documento completo.
