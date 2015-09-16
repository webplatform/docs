---
title: ¿Cómo funciona el Internet?
lang: es
summary: "Muy pocas veces te ofrecen una mirada tras bastidores a los engranajes y maquinarias de la acción. Hoy es tu día de suerte. En este artículo te daremos acceso detrás del escenario a una de las tecnologías más famosas, una con la cual ya debes estar familiarizado: el World Wide Web.\n"
tags:
  - Concept
  - Pages
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'concepts/Internet and Web/How does the Internet Work/af'
    - 'concepts/Internet and Web/How does the Internet Work/ar'
    - 'concepts/Internet and Web/How does the Internet Work/ast'
    - 'concepts/Internet and Web/How does the Internet Work/az'
    - 'concepts/Internet and Web/How does the Internet Work/bcc'
    - 'concepts/Internet and Web/How does the Internet Work/bg'
    - 'concepts/Internet and Web/How does the Internet Work/br'
    - 'concepts/Internet and Web/How does the Internet Work/ca'
    - 'concepts/Internet and Web/How does the Internet Work/cs'
    - 'concepts/Internet and Web/How does the Internet Work/da'
    - 'concepts/Internet and Web/How does the Internet Work/de'
    - 'concepts/Internet and Web/How does the Internet Work/diq'
    - 'concepts/Internet and Web/How does the Internet Work/el'
    - 'concepts/Internet and Web/How does the Internet Work/eo'
    - 'concepts/Internet and Web/How does the Internet Work/fa'
    - 'concepts/Internet and Web/How does the Internet Work/fi'
    - 'concepts/Internet and Web/How does the Internet Work/fr'
    - 'concepts/Internet and Web/How does the Internet Work/gl'
    - 'concepts/Internet and Web/How does the Internet Work/gu'
    - 'concepts/Internet and Web/How does the Internet Work/he'
    - 'concepts/Internet and Web/How does the Internet Work/hu'
    - 'concepts/Internet and Web/How does the Internet Work/hy'
    - 'concepts/Internet and Web/How does the Internet Work/id'
    - 'concepts/Internet and Web/How does the Internet Work/it'
    - 'concepts/Internet and Web/How does the Internet Work/ka'
    - 'concepts/Internet and Web/How does the Internet Work/kk'
    - 'concepts/Internet and Web/How does the Internet Work/km'
    - 'concepts/Internet and Web/How does the Internet Work/ko'
    - 'concepts/Internet and Web/How does the Internet Work/ksh'
    - 'concepts/Internet and Web/How does the Internet Work/kw'
    - 'concepts/Internet and Web/How does the Internet Work/mk'
    - 'concepts/Internet and Web/How does the Internet Work/ml'
    - 'concepts/Internet and Web/How does the Internet Work/mr'
    - 'concepts/Internet and Web/How does the Internet Work/ms'
    - 'concepts/Internet and Web/How does the Internet Work/nl'
    - 'concepts/Internet and Web/How does the Internet Work/no'
    - 'concepts/Internet and Web/How does the Internet Work/oc'
    - 'concepts/Internet and Web/How does the Internet Work/pl'
    - 'concepts/Internet and Web/How does the Internet Work/pt'
    - 'concepts/Internet and Web/How does the Internet Work/pt-br'
    - 'concepts/Internet and Web/How does the Internet Work/ro'
    - 'concepts/Internet and Web/How does the Internet Work/ru'
    - 'concepts/Internet and Web/How does the Internet Work/si'
    - 'concepts/Internet and Web/How does the Internet Work/sk'
    - 'concepts/Internet and Web/How does the Internet Work/sl'
    - 'concepts/Internet and Web/How does the Internet Work/sq'
    - 'concepts/Internet and Web/How does the Internet Work/sr'
    - 'concepts/Internet and Web/How does the Internet Work/sv'
    - 'concepts/Internet and Web/How does the Internet Work/ta'
    - 'concepts/Internet and Web/How does the Internet Work/th'
    - 'concepts/Internet and Web/How does the Internet Work/tr'
    - 'concepts/Internet and Web/How does the Internet Work/uk'
    - 'concepts/Internet and Web/How does the Internet Work/vi'
    - 'concepts/Internet and Web/How does the Internet Work/yue'
    - 'concepts/Internet and Web/How does the Internet Work/zh'
    - 'concepts/Internet and Web/How does the Internet Work/zh-hans'
    - 'concepts/Internet and Web/How does the Internet Work/zh-hant'
    - 'concepts/Internet and Web/How does the Internet Work/zh-tw'
translations:
  ja:
    text: 日本語
    href: /concepts/Internet_and_Web/How_does_the_Internet_Work/ja
uri: 'concepts/Internet and Web/How does the Internet Work/es'

---
## Summary

Muy pocas veces te ofrecen una mirada tras bastidores a los engranajes y maquinarias de la acción. Hoy es tu día de suerte. En este artículo te daremos acceso detrás del escenario a una de las tecnologías más famosas, una con la cual ya debes estar familiarizado: el World Wide Web.

En este artículo cubriremos las tecnologías fundamentales que mueven el World Wide Web:

-   Lenguaje de Hipertexto Marcado (HTML)
-   Protocolo de Transferencia de Marcado (HTTP)
-   Sistema de Nombres de Dominios (DNS)
-   Servidores web y navegadores
-   Contenido estático y dinámico

Aunque la mayoría de lo que será cubierto aquí no te ayudará a construir un mejor sitio web, si te dará el lenguaje apropiado a usar cuando hables con clientes u otras personas acerca de la Web. En este artículo se va a mirar brevemente cómo las computadoras se comunican. Luego los diferentes lenguajes que trabajan en equipo para crear las páginas que componen la Web.

## ¿Cómo se comunican las computadoras a través del Internet?

Afortunadamente, hemos mantenido las cosas simples para las computadoras. En el caso del World Wide Web, la gran mayoría de las páginas están escritas en el mismo lenguaje, HTML, el cual se mueve alrededor usando un protocolo común - HTTP. HTTP es el lenguaje común del Internet (dialecto o especificación). El mismo permite, por ejemplo, que una máquina Windows cante en harmonía con una máquina corriendo la última versión de Linux. A través del uso de un navegador (un software que interpreta HTTP y traduce HTML a una forma que el ser humano pueda leer), páginas web creadas en HTML en cualquier tipo de computadora pueden ser leídas en cualquier lugar, incluyendo teléfonos, PDAs e inclusive las populares consolas de juegos.

Aunque la variedad de dispositivos que pueden acceder la web usan el mismo idioma, debe haber reglas que les permita comunicarse entre unos y otros – es como aprender a levantar la mano en clase para hacer una pregunta. HTTP establece estas reglas para el Internet. Por causa del HTTP, una máquina cliente (como tu computadora) sabe que tiene que ser ella la que inicie la solicitud de una página web. La computadora envía esta solicitud a un **servidor**. Un servidor es una computadora en donde residen los sitios web. Cuando escribes una dirección web en tu navegador, un servidor recibe tu solicitud, encuentra la página web que quieres y la envía de vuelta a tu computadora para que tu navegador la muestre.

### Disección de un ciclo de solicitud/respuesta

Ahora que hemos visto todas las partes que permiten que las computadoras puedan comunicarse a través del Internet, vamos a ver con más detalle el ciclo de solicitud/respuesta del protocolo HTTP. Debajo hay varios pasos detallados para así intentar demostrar más eficientemente algunos conceptos.

1.  Todo ciclo de solicitud/respuesta comienza por escribir un URL (comúnmente conocido como dirección web) en la barra de dirección de tu navegador. Algo como <http://www.apple.com>. Abre tu navegador, escribe este URL y presiona Enter/Return (o sigue el enlace anterior) para ir a la página inicial de Apple. Ahora, algo que tal vez no sepas es que realmente los navegadores no utilizan los URL para solicitar páginas web a los servidores; ellos usan el **Internet Protocol** (protocolo de internet) o **IP addresses** (direcciones IP, las cuales funcionan como números de teléfono o direcciones postales, pero estas identifican servidores en vez de teléfonos o direcciones). Por ejemplo, la dirección IP de <http://www.apple.com> es 17.149.160.49
2.  Intenta abrir una nueva ventana o tab en tu navegador, escribe <http://17.149.160.49> en la barra de direcciones y presiona Enter. Vas a ver la misma página web que viste en el paso 1. <http://www.apple.com> actúa básicamente como un alias para <http://17.149.160.49>. Pero, ¿por qué? Y ¿cómo? Esto es así porque las personas recuerdan mejor una palabra que largas secuencias de números. El sistema que lleva a cabo este trabajo se llama DNS, el cual es un directorio automático y exhaustivo de todas las maquinas conectadas al Internet. Cuando escribes <http://www.apple.com> en tu barra de direcciones y presionas Enter, esa dirección es enviada a un servidor de nombres el cual intenta asociar la misma con su dirección IP. Hay literalmente millones de máquinas conectadas al Internet y cada servidor DNS no tiene una lista de cada máquina online, así que hay un sistema establecido de tal forma que si el primer servidor DNS no tiene la información requerida, la búsqueda es referida a otro servidor DNS. Así que el sistema DNS busca el sitio web de Apple, encuentra que el mismo está localizado en 17.149.160.49 y envía esta dirección IP a tu navegador. Tu máquina entonces envía una solicitud a la dirección IP especificada y espera por una respuesta de vuelta. Si todo va bien el servidor envía un corto mensaje de vuelta al cliente diciendo que todo está bien seguido por la página web. Este tipo de mensaje esta contenido en un **HTTP Header** (encabezamiento HTTP).

![ciclo de solicitud respuesta exitoso](/assets/public/6/62/article3.gif)

 Figura 1: En este caso, todo esta bien y el servidor devuelve la página correcta. Si algo sale mal, como por ejemplo escribir incorrectamente el URL, el servidor enviará como respuesta un **HTTP error** (error HTTP) al navegador – el infame error 404 “page not found” (página no encontrada) es el error con el que te encontrarás con más frecuencia.

-   Intenta escribir la dirección *<http://www.joniscool.co.uk/jonlane/>*. La página no existe, así que vas a recibir un error 404 de vuelta. Intenta buscar algunas direcciónes que no existan y recibirás una variedad de páginas de error de vuelta. Esto es así porque algunos desarrolladores web permiten que el servidor web devuelva las páginas de error que ya trae por defecto mientras que otros prefieren escribir sus propias páginas de error para que sean estas páginas las que sean devueltas en caso de algún error. Esta es una técnica avanzada que no vamos a cubrir en este curso, pero Stuart Colville tiene un buen articulo sobre el tema en [Adding meaning to your HTTP error pages!](http://dev.opera.com/articles/view/adding-meaning-to-http-error-pages/). Por último, una nota acerca de los URL – usualmente el primer URL que usas cuando visitas un sitio web no contiene el nombre de un archivo al final del mismo (por ejemplo *<http://www.mysite.com/>*), entonces la páginas subsiguientes a veces tienen otras y a veces no. Tu siempre estás accesando algún archivo pero el desarrollador web puede configurar el servidor para que no muestre los nombres de los archivos en el URL. Esta práctica generalmente ayuda a recordar fácilmente los URL y provee una mejor experiencia para el usuario. De nuevo, esto es algo avanzado, así que no cubriremos esta técnica en este curso pero si como subir archivos a un servidor y la estructura de los directorios de archivos en [Getting your content online](http://dev.opera.com/articles/view/supplementary-getting-your-content-onli/), por Craig Grannell.

