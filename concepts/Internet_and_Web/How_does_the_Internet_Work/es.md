{{Page_Title|¿Cómo funciona el Internet?}}
{{Flags
|State=Unreviewed
|Editorial notes=
|Checked_Out=No
}}
{{Languages}}
{{API_Name}}
{{Summary_Section|Muy pocas veces te ofrecen una mirada tras bastidores a los engranajes y maquinarias de la acción. Hoy es tu día de suerte. En este artículo te daremos acceso detrás del escenario a una de las tecnologías más famosas, una con la cual ya debes estar familiarizado: el World Wide Web.

En este artículo cubriremos las tecnologías fundamentales que mueven el World Wide Web:

* Lenguaje de Hipertexto Marcado (HTML)
* Protocolo de Transferencia de Marcado (HTTP)
* Sistema de Nombres de Dominios (DNS)
* Servidores web y navegadores
* Contenido estático y dinámico

Aunque la mayoría de lo que será cubierto aquí no te ayudará a construir un mejor sitio web, si te dará el lenguaje apropiado a usar cuando hables con clientes u otras personas acerca de la Web. En este artículo se va a mirar brevemente cómo las computadoras se comunican. Luego los diferentes lenguajes que trabajan en equipo para crear las páginas que componen la Web.
}}
{{Concept_Page
|Content=== ¿Cómo se comunican las computadoras a través del Internet? ==

Afortunadamente, hemos mantenido las cosas simples para las computadoras. En el caso del World Wide Web, la gran mayoría de las páginas están escritas en el mismo lenguaje, HTML, el cual se mueve alrededor usando un protocolo común - HTTP. HTTP es el lenguaje común del Internet (dialecto o especificación). El mismo permite, por ejemplo, que una máquina Windows cante en harmonía con una máquina corriendo la última versión de Linux. A través del uso de un navegador (un software que interpreta HTTP y traduce HTML a una forma que el ser humano pueda leer), páginas web creadas en HTML en cualquier tipo de computadora pueden ser leídas en cualquier lugar, incluyendo teléfonos, PDAs e inclusive las populares consolas de juegos.

Aunque la variedad de dispositivos que pueden acceder la web usan el mismo idioma, debe haber reglas que les permita comunicarse entre unos y otros – es como aprender a levantar la mano en clase para hacer una pregunta. HTTP establece estas reglas para el Internet. Por causa del HTTP, una máquina cliente (como tu computadora) sabe que tiene que ser ella la que inicie la solicitud de una página web.  La computadora envía esta solicitud a un '''servidor'''. Un servidor es una computadora en donde residen los sitios web. Cuando escribes una dirección web en tu navegador, un servidor recibe tu solicitud, encuentra la página web que quieres y la envía de vuelta a tu computadora para que tu navegador la muestre.

=== Disección de un ciclo de solicitud/respuesta  ===

Ahora que hemos visto todas las partes que permiten que las computadoras puedan comunicarse a través del Internet, vamos a ver con más detalle el ciclo de solicitud/respuesta del protocolo HTTP. Debajo hay varios pasos detallados para así intentar demostrar más eficientemente algunos conceptos. 
# Todo ciclo de solicitud/respuesta comienza por escribir un URL (comúnmente conocido como dirección web) en la barra de dirección de tu navegador. Algo como http://www.apple.com. Abre tu navegador, escribe este URL y presiona Enter/Return (o sigue el enlace anterior) para ir a la página inicial de Apple. Ahora, algo que tal vez no sepas es que realmente los navegadores no utilizan los URL para solicitar páginas web a los servidores; ellos usan el '''Internet Protocol''' (protocolo de internet) o '''IP addresses''' (direcciones IP, las cuales funcionan como números de teléfono o direcciones postales, pero estas identifican servidores en vez de teléfonos o direcciones). Por ejemplo, la dirección IP de http://www.apple.com es 17.149.160.49
# Intenta abrir una nueva ventana o tab en tu navegador, escribe http://17.149.160.49 en la barra de direcciones y presiona Enter. Vas a ver la misma página web que viste en el paso 1. http://www.apple.com actúa básicamente como un alias para http://17.149.160.49. Pero,  ¿por qué? Y  ¿cómo? Esto es así porque las personas recuerdan mejor una palabra que largas secuencias de números. El sistema que lleva a cabo este trabajo se llama DNS, el cual es un directorio automático y exhaustivo de todas las maquinas conectadas al Internet. Cuando escribes  http://www.apple.com en tu barra de direcciones y presionas Enter, esa dirección es enviada a un servidor de nombres el cual intenta asociar la misma con su dirección IP. Hay literalmente millones de máquinas conectadas al Internet y cada servidor DNS no tiene una lista de cada máquina online, así que hay un sistema establecido de tal forma que si el primer servidor DNS no tiene la información requerida, la búsqueda es referida a otro servidor DNS. Así que el sistema DNS busca el sitio web de Apple, encuentra que el mismo está localizado en 17.149.160.49 y envía esta dirección IP a tu navegador. Tu máquina entonces envía una solicitud a la dirección IP especificada y espera por una respuesta de vuelta. Si todo va bien el servidor envía un corto mensaje de vuelta al cliente diciendo que todo está bien seguido por la página web. Este tipo de mensaje esta contenido en un '''HTTP Header''' (encabezamiento HTTP).

[[Image:article3.gif|center|ciclo de solicitud respuesta exitoso]]


Figura 1: En este caso, todo esta bien y el servidor devuelve la página correcta. Si algo sale mal, como por ejemplo escribir incorrectamente el URL, el servidor enviará como respuesta un '''HTTP error''' (error HTTP) al navegador – el infame error 404 “page not found” (página no encontrada) es el error con el que te encontrarás con más frecuencia.

* Intenta escribir la dirección ''http://www.joniscool.co.uk/jonlane/''. La página no existe, así que vas a recibir un error 404 de vuelta. Intenta buscar algunas direcciónes que no existan y recibirás una variedad de páginas de error de vuelta. Esto es así porque algunos desarrolladores web permiten que el servidor web devuelva las páginas de error que ya trae por defecto mientras que otros prefieren escribir sus propias páginas de error para que sean estas páginas las que sean devueltas en caso de algún error. Esta es una técnica avanzada que no vamos a cubrir en este curso, pero Stuart Colville tiene un buen articulo sobre el tema en [http://dev.opera.com/articles/view/adding-meaning-to-http-error-pages/ Adding meaning to your HTTP error pages!]. Por último, una nota acerca de los URL – usualmente el primer URL que usas cuando visitas un sitio web no contiene el nombre de un archivo al final del mismo (por ejemplo ''http://www.mysite.com/''), entonces la páginas subsiguientes a veces tienen otras y a veces no. Tu siempre estás accesando algún archivo pero el desarrollador web puede configurar el servidor para que no muestre los nombres de los archivos en el URL. Esta práctica generalmente ayuda a recordar fácilmente los URL y provee una mejor experiencia para el usuario. De nuevo, esto es algo avanzado, así que no cubriremos esta técnica en este curso pero si como subir archivos a un servidor y la estructura de los directorios de archivos en [http://dev.opera.com/articles/view/supplementary-getting-your-content-onli/ Getting your content online], por Craig Grannell.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}