---
title: Fundamentos de la accesibilidad web
lang: es
notes:
  - 'Not in English.'
tags:
  - Basic
  - Pages
  - Accessibility
  - ARIA
  - Design
  - UI
  - Usability
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - concepts/accessibility/af
    - concepts/accessibility/ar
    - concepts/accessibility/ast
    - concepts/accessibility/az
    - concepts/accessibility/bcc
    - concepts/accessibility/bg
    - concepts/accessibility/br
    - concepts/accessibility/ca
    - concepts/accessibility/cs
    - concepts/accessibility/da
    - concepts/accessibility/de
    - concepts/accessibility/diq
    - concepts/accessibility/el
    - concepts/accessibility/eo
    - concepts/accessibility/fa
    - concepts/accessibility/fi
    - concepts/accessibility/fr
    - concepts/accessibility/gl
    - concepts/accessibility/gu
    - concepts/accessibility/he
    - concepts/accessibility/hu
    - concepts/accessibility/hy
    - concepts/accessibility/id
    - concepts/accessibility/it
    - concepts/accessibility/ka
    - concepts/accessibility/kk
    - concepts/accessibility/km
    - concepts/accessibility/ko
    - concepts/accessibility/ksh
    - concepts/accessibility/kw
    - concepts/accessibility/mk
    - concepts/accessibility/ml
    - concepts/accessibility/mr
    - concepts/accessibility/ms
    - concepts/accessibility/nl
    - concepts/accessibility/no
    - concepts/accessibility/oc
    - concepts/accessibility/pl
    - concepts/accessibility/pt
    - concepts/accessibility/pt-br
    - concepts/accessibility/ro
    - concepts/accessibility/ru
    - concepts/accessibility/si
    - concepts/accessibility/sk
    - concepts/accessibility/sl
    - concepts/accessibility/sq
    - concepts/accessibility/sr
    - concepts/accessibility/sv
    - concepts/accessibility/ta
    - concepts/accessibility/th
    - concepts/accessibility/tr
    - concepts/accessibility/uk
    - concepts/accessibility/vi
    - concepts/accessibility/yue
    - concepts/accessibility/zh
    - concepts/accessibility/zh-hans
    - concepts/accessibility/zh-hant
    - concepts/accessibility/zh-tw
translations:
  ja:
    text: 日本語
    href: /concepts/accessibility/ja
uri: concepts/accessibility/es

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Esta página brinda una introducción a la accesibilidad web y enlaza a recursos para mayor información. Te sugerimos que leas primero esta página completamente y luego regreses y visites los enlaces para aprender más.

## <span>Resumen</span>

La accesibilidad está haciendo que la Web funcione para las personas con una amplia gama de habilidades. La accesibilidad es esencial para los desarrolladores y las organizaciones que desean crear sitios y herramientas web de alta calidad sin excluir a algunas personas del uso de sus productos y servicios. La accesibilidad es fundamental para que las personas con discapacidad puedan participar por igual en la Web. Se trata de un requisito legal en algunos casos y de prácticas recomendadas en todos los casos.

Esta página brinda una introducción a la accesibilidad web y enlaza a recursos para mayor información. Te sugerimos que leas primero esta página completamente y luego regreses y visites los enlaces para aprender más.

## <span>La Web es para todas las personas</span>

La Web está fundamentalmente diseñada para que sirva a todas las personas, independientemente de su hardware, software, idioma, cultura, localización o su capacidad física o mental.

Cuando la Web cumple con este objetivo, es accesible a las personas con una diversa gama de capacidades auditivas, motoras, visuales y cognitivas. Así, el impacto de la discapacidad cambia radicalmente en la Web porque la Web elimina barreras a la comunicación e interacción que muchas personas enfrentan en el mundo físico.

Sin embargo, cuando los sitios, tecnologías y herramientas web están mal diseñadas pueden crear barreras que excluyen a algunas personas del uso de la Web. Por ejemplo, un sitio web inaccesible podría:

-   Impedir que las personas sordas obtengan información de un podcast o video
-   Impedir que las personas con discapacidades cognitivas puedan leer el contenido por la presencia de imágenes en movimiento, parpadeantes o cambiantes
-   Impedir que las personas con discapacidades físicas completen una transacción porque no pueden usar un ratón.

### <span>¿Qué es la accesibilidad web?</span>

Accesibilidad Web significa que las personas con discapacidad puedan utilizar la Web. Más específicamente, esto significa que las personas con discapacidad puedan percibir, entender, navegar e interactuar con la Web y que puedan contribuir a la Web. Para una introducción a **por qué** - el argumento de la accesibilidad web, **qué** - ejemplos de accesibilidad web y **cómo** hacer tus sitios y herramientas web accesibles , visita [Accesibilidad - W3C](http://www.w3.org/standards/webdesign/accessibility) [inglés].

La accesibilidad web abarca todas las discapacidades que afectan el acceso a la Web, incluidas las personas con discapacidad auditiva, cognitiva, neurológica, física, del habla y visual. La accesibilidad incluye a las personas con discapacidad debido al envejecimiento.

Aunque la accesibilidad se centra en las personas con discapacidad, también beneficia a otras, como las personas que utilizan dispositivos móviles y personas en situaciones limitantes (por ejemplo, un ambiente ruidoso donde no pueden escuchar el audio). **La accesibilidad apoya la inclusión social** para las personas con discapacidad, las personas mayores, los usuarios móviles, las personas en zonas rurales, las personas con conexiones de bajo ancho de banda, las personas con bajo nivel de alfabetización, etc. Encontrarás más información en las secciones [la web móvil](#La_web_m.C3.B3vil) y [usuarios mayores](#Usuarios_mayores) más adelante, así como en [Beneficios de la accesibilidad web las personas con y sin discapacidad](http://www.w3.org/WAI/bcase/soc.html#groups) [inglés].

### <span>La accesibilidad web es esencial para la igualdad de oportunidades</span>

La Web es cada vez más un recurso esencial para muchos aspectos de la vida: educación, empleo, gobierno, comercio, salud, recreación, interacción social y más. La Web se utiliza no sólo para recibir información, sino también para proporcionar información e interactuar con la sociedad. Por lo tanto, es esencial que la Web sea accesible con el fin de proporcionar un acceso equitativo e igualdad de oportunidades para las personas con discapacidad. De hecho, las Naciones Unidas reconocen a la accesibilidad web como un derecho humano básico. Más información en [La accesibilidad web es un asunto social](http://www.w3.org/WAI/bcase/soc#social) [inglés] en la página de factores sociales.

## <span>Entender como las personas usan la web</span>

Historias sobre personas que utilizan la Web ayudan a ilustrar las necesidades cotidianas de las personas con discapacidad. Por ejemplo:

-   La Sra. Olsen asiste a la escuela secundaria y le gusta de manera particular su clase de literatura. Ella sufre del trastorno de déficit de atención e hiperactividad (TDAH) y dislexia, una combinación que da lugar a dificultades importantes en la lectura.
-   La Sra. Laitinen es el jefe de contabilidad en una compañía de seguros que utiliza documentos y formularios web en una intranet corporativa. Ella es ciega y, al igual que muchas otras personas que son ciegas, ella no lee braille.
-   El Sr. Yunus tiene 85 años y comenzó a utilizar la Web hace varios años para mantenerse en contacto con sus familiares y amigos, además de para leer sobre historia del arte. El sufre de visión reducida, temblor en las manos y pérdida leve de la memoria de corto plazo debido al envejecimiento.

Más detalles acerca de cómo estas y otras personas con discapacidad utilizan la Web en [Historias de usuarios de la Web](http://www.w3.org/WAI/intro/people-use-web/stories) [inglés].

La gente tiene una gran variedad de habilidades que afectan la forma en que utilizan la Web. Algunas personas tienen impedimentos temporales, algunos tienen discapacidades relacionadas con la edad, algunos tienen discapacidades desde el nacimiento, algunos desarrollan discapacidades por lesiones o problemas de salud y algunos tienen múltiples discapacidades. Las habilidades de algunas personas cambian dependiendo de la fatiga, inflamación, medicamentos, etc. Para conocer más acerca de la diversidad de capacidades y los tipos de barreras de accesibilidad web que la gente comúnmente enfrenta en los sitios y herramientas web mal diseñados, visita [Diversidad de usuarios de la Web](http://www.w3.org/WAI/intro/people-use-web/diversity) [inglés].

Las personas con discapacidad acceden y navegan la Web de diferentes maneras. A veces la gente configura el software y el hardware estándar de acuerdo a sus necesidades y a veces la gente utiliza software o hardware especializado que les ayuda a realizar ciertas tareas. Para más información sobre las técnicas y herramientas que las personas con discapacidad utilizan para interactuar con la Web, tales como la configuración del navegador, conversores de texto a voz y reconocimiento de voz, visita [Diversidad en el uso de la Web](http://www.w3.org/WAI/intro/people-use-web/browsing) [inglés].

## <span>Requisitos de accesibilidad</span>

Para que las personas con discapacidad puedan utilizar la Web hay ciertas cosas que los sitios y herramientas web tienen que hacer. Estos requisitos de accesibilidad cumplen cuatro principios fundamentales:

1.  Información e interfaz de usuario **Perceptible**.
    Los requerimienos de accesibilidad incluyen: proporcionar texto alternativo para las imágenes, proporcionar subtítulos o transcripciones de vídeo y audio y proporcionae suficiente contraste de color entre el texto y el fondo.
2.  Interfaz de usuario y navegación **Operable**.
    Los requerimientos de accesibilidad incluyen: habilitar la navegación mediante uso exclusivo del teclado, proporcionar enlaces con significado y permitir suficiente tiempo para que los usuarios completen una tarea.
3.  Información e interfaz de usuario **Comprensible**.
    Los requerimientos de accesibilidad incluyen: hacer el contenido fácil de leer, proporcionar funcionalidades predecibles y ayudar a los usuarios a evitar y corregir errores.
4.  Contenido **Robusto** e interpretación confiable.
    Los requerimientos de accesibilidad incluyen: maximizar la compatibilidad con las herramientas actuales y futuras (navegadores web, ayudas técnicas, etc.)

**Para conocer más acerca de estos principios y requerimientos de accesibilidad web, visita [Principios de Accesibilidad](http://www.w3.org/WAI/intro/people-use-web/principles)** [inglés].

Para una corta introducción a tres problemas de accesibilidad web (texto alternativo para imágenes, introducción de datos mediante teclado y transcripciones), visita [Qué: Ejemplos de Accesibilidad Web](http://www.w3.org/standards/webdesign/accessibility#examples) [inglés].

## <span>ARIA</span>

"WAI-ARIA describe cómo añadir semántica y otros metadatos al contenido HTML con el fin de hacer los controles de interfaz de usuario y el contenido dinámico más accesible. Por ejemplo, con WAI-ARIA es posible identificar una lista de enlaces como un menú de navegación e indicar si está expandido o contraído ".

Para mayor información, dirígete a [en.wikipedia.org/wiki/WAI-ARIA](http://en.wikipedia.org/wiki/WAI-ARIA)

Para una introducción a los retos y soluciones de accesibilidad para las Aplicaciones Enriquecidas de Internet (RIAs, por sus iniciales en inglés), visita [Cartilla fundamental de WAI-ARIA 1.0](http://www.w3.org/TR/wai-aria-primer/).

## <span>Los componentes de la accesibilidad web</span>

Los principios de accesibilidad se aplican a los componentes presentados a continuación. Es esencial que los componentes de desarrollo web e interacción trabajen juntos para que la Web sea accesible a las personas con discapacidad. La Iniciativa de Accesibilidad Web del W3C (WAI, por sus iniciales en inglés) proporciona las pautas que cubren los requerimientos de accesibilidad de los componentes técnicos.

### <span>Contenido web</span>

El contenido es la información disponible en una página o **aplicación** web incluyendo: información natural como texto, imágenes y sonidos, el código de etiquetado que define la estructura, presentación, interacción, etc. Los requerimientos de contenido se tratan en las Pautas de Accesibilidad para el Contenido Web (**WCAG**, por sus iniciales en inglés).

Los documentos de las WCAG explican cómo hacer el contenido web (incluyendo las aplicaciones web) más accesible a las personas con discapacidad. Para aprender más acerca de cómo están estructuradas las WCAG y acerca de los documentos de apoyo que ofrecen consejos prácticos para cumplir con los requermientos de accesibilidad, consulta la **[Información general de las WCAG](http://www.w3.org/WAI/intro/wcag.php)** [inglés].

### <span>Herramientas</span>

Las herramientas que utilizamos para crear y usar el contenido web pueden ayudar o dificultar la accesibildad web.

-   Las **herramientas de creación** son software y servicios que se utilizan para crear y editar sitios web, por ejemplo, los sistemas de gestión de contenidos (CMS, por sus iniciales en inglés), editores de HTML, sitios web que permiten a los usuarios agregar contenido (como las redes sociales) y otras herramientas. Las herramientas deben apoyar a las personas en hacer sus contenidos web accesibles y las herramientas, en sí, deben ser accesibles para que las personas con discapacidad puedan utilizarlas. Esto se trata en las Pautas de Accesibilidad para Herramientas de Creación (ATAG, por sus iniciales en inglés), consulta la **[Información general de ATAG](http://www.w3.org/WAI/intro/atag.php)** [inglés].
-   Las **Herramientas de evaluación** ayudan a verificar si los sitios web cumplen con las normas. (La información relevante se encuentra en [Seleccionar herramientas de evaluación de accesibilidad web](http://www.w3.org/WAI/eval/selectingtools.html) [inglés]).
-   Los **Navegadores web**, reproductores de medios y otros "agentes de usuario" que acceden a contenidos web se tratan en las Pautas de Accesibilidad para Agentes de Usuario (UAAG, por sus iniciales en inglés), consulta la **[Información general de UAAG](http://www.w3.org/WAI/intro/uaag.php)** [inglés].
-   Las **ayudas técnicas** son software o hardware que las personas con discapacidad utilizan para mejorar su interacción con la Web, por ejemplo, los lectores de pantalla que leen en voz alta las páginas web, software de reconocimiento de voz, teclados alternativos, etc (Introducidas en [Herramientas|Técnicas |Diversidad en el uso de la web](http://www.w3.org/WAI/intro/people-use-web/browsing.html)) [inglés].

### <span>Personas - autores de contenido web y usuarios web</span>

Además del contenido web y las herramientas, las personas son un componente importante de la accesibilidad web.

Las **personas que crean contenidos** deben entender y poner en práctica la accesibilidad. Esto incluye a desarrolladores, diseñadores, escritores, directores, etc. Cualquier persona que esté involucrada en el desarrollo de contenidos (incluidas las aplicaciones), herramientas de creación, herramientas de evaluación, navegadores y otros agentes de usuario.

Las **personas que utilizan la Web** tienen diferentes conocimientos, experiencias y niveles de habilidad que afectan la accesibilidad, por ejemplo, qué tan bien una persona sabe utilizar las ayudas técnicas o estrategias de adaptación y si pueden obtener herramientas para satisfacer sus necesidades.

Para obtener más información sobre estos componentes de contenidos web, herramientas y personas, consulta la [Presentación "Componentes de la accesibilidad web"](http://www.w3.org/WAI/presentations/components/Overview.php) [inglés] o [Componentes esenciales de la accesibilidad web](http://www.w3.org/WAI/intro/components.php) [inglés].

## <span>Argumento de Negocios</span>

Para que las organizaciones estén dispuestas a hacer la inversión inicial en accesibilidad muchos necesitan comprender los beneficios financieros de la accesibilidad web. Para una introducción al tema, consulta la [Presentación "La acesibilidad web es negocio inteligente"](http://www.w3.org/WAI/presentations/bcase/Overview.php) [inglés].

Para aprender más acerca de los factores sociales, técnicos, financieros, legales y de políticas, visita [Desarrollando un argumento de negocios para la accesibilidad web en tu organización](http://www.w3.org/WAI/bcase/Overview.html) [inglés]. Este conjunto de páginas presenta diferentes aspectos de la accesibilidad web junto con una orientación en el desarrollo de un argumento de negocios personalizado.

Por ejemplo, uno de los aspectos del argumento de negocios es alcanzar a más usuarios, incluidos los usuarios de más edad y los usuarios móviles.

### <span>Usuarios mayores</span>

Los usuarios de Internet de edad avanzada son un segmento de mercado cada vez mayor y un grupo objetivo importante para muchas empresas gobiernos y otras organizaciones. Muchas personas mayores tienen discapacidades relacionadas con la edad que pueden afectar la forma en que utilizan la Web, como disminución de la visión, capacidad física, la audición y la capacidad cognitiva. Estos problemas coinciden con las necesidades de accesibilidad de las personas con discapacidad. Por lo tanto, los sitios y herramientas web que son accesibles a las personas con discapacidad también son más accesibles a los usuarios mayores. Para obtener más información, visita [Accesibilidad web y personas de edad avanzada: Satisfacer las necesidades de usuarios web que envejecen](http://www.w3.org/WAI/older-users/Overview.php) [inglés].

### <span>La web móvil</span>

Con el uso mundial de la telefonía móvil en su punto más alto, se ha producido un aumento del interés en el desarrollo de sitios web que son accesibles desde un dispositivo móvil. Los usuarios de dispositivos móviles y las personas con discapacidad se enfrentan a barreras similares al interactuar con el contenido web. Los sitios web pueden alcanzar más eficientemente ambos objetivos cuando los desarrolladores entienden la importante superposición entre hacer un sitio web accesible para un dispositivo móvil y para las personas con discapacidad. Para obtener más información, consulta [Accesibilidad del contenido web y la web móvil: Hacer un sitio web accesible tanto para las personas con discapacidad como para los dispositivos móviles](http://www.w3.org/WAI/mobile/) [inglés].

## <span>Aprende más en la WAI del W3C</span>

La Iniciativa de Accesibilidad Web del W3C (WAI) reúne a personas de la industria, organizaciones sobre discapacidad, gobiernos y laboratorios de investigación de todo el mundo para desarrollar pautas y recursos que ayuden a hacer la Web accesible para las personas con discapacidad. Te recomendamos revisar el [sitio web de la WAI](http://www.w3.org/WAI/) [Inglés] y buscar más información que te sea útil. Lee [Encontrando tu ruta hacia nuevos recursos de accesibilidad web](http://www.w3.org/WAI/yourWAI) [inglés].

## <span>Referencias y reconocimientos</span>

Referencias de esta información: La mayor parte del texto de esta página procede de otros documentos que están enlazados dentro de cada sección. Para referencias, por favor, utiliza el documento de origen. (Consulta [Usando el material de la WAI: Permisos de uso con Reconocimiento](http://www.w3.org/WAI/about/usingWAImaterial.html) [Inglés]).

## <span>Consulta también</span>

-   [Esta página se encuentra originalmente en W3C WAI](http://www.w3.org/WAI/EO/wiki/Web_Accessibility_Basics) [Inglés]
-   [Mejorando la accesibilidad usando caracteristicas de HTML5](http://www.w3.org/WAI/GL/wiki/Techniques/HTML5) [Inglés]
-   [Mejorando la accesibilidad usando características de ARIA](http://www.w3.org/WAI/GL/wiki/Techniques/ARIA) [Inglés] -- por favor, colocar una pequeña explicación de lo que \*es\* ARIA
-   [Técnicas de HTML y CSS para cumplir con los criterios de cumplimiento de las WCAG](http://www.w3.org/TR/WCAG20-TECHS/) [Inglés]
-   [Hacer accesibles las aplicaciones de Windows Store usando JavaScript y HTML](http://msdn.microsoft.com/en-us/library/windows/apps/hh452681.aspx) [Inglés]

## <span>Notes</span>

There should be an explanation of what ARIA \*is\* which is not clear from this page nor the link. Even to a professional web developer. Wikpedia article ([WAI-ARIA](http://en.wikipedia.org/wiki/WAI-ARIA)) was much clearer and better written as an introduction.

Should be overhauled: there are entire books and careers dedicated to Accessibility: what are the web programming techniques? How to make documents accessible? What disabilities are there and how does that affect e-accessibility? There are also a ton of resources out there that aid accessibility, either through audits or through web navigation.