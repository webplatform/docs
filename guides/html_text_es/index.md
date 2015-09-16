---
title: Texto en HTML
uri: 'guides/html text es'

---
**Nota: Este artículo no se ha revisado.**

## Introducción

En este apartado explicaremos los conceptos básicos del uso de HTML para describir el significado del contenido dentro del cuerpo de vuestro documento.

Veremos elementos estructurales generales como los títulos y los párrafos y la incrustación de citas y código. Después también veremos el contenido en línea, como por ejemplo las citas cortas y el énfasis, y acabaremos con un análisis rápido del contenido presentacional anticuado.

## El espacio: la última frontera

Una cuestión muy importante que queremos tratar antes de empezar a hablar sobre el texto es la del espacio, y concretamente la del espacio entre palabras. Cuando se escribe el HTML, el documento fuente contendrá lo que se conoce como "espacios en blanco", que son los caracteres del archivo que sirven para separar el texto. El carácter de espacio más habitual es el que se obtiene al pulsar la barra espaciadora, pero hay otros, como el tabulador y la marca entre dos líneas independientes de un documento (conocido como retorno o línea nueva).

En el HTML, cuando un carácter de éstos aparece varias veces seguidas, se considera (casi) siempre como un único carácter de espacio.

Por ejemplo, un navegador interpretaría lo siguiente:

``` html
<h3>En el
                comenzado</h3>
```

 como equivalente a:

``` html
<h3>En el comenzado</h3>
```

 El único lugar donde esto no aplica es en el elemento `<pre>`, el cual será discutido en detalle más adelante en este apartado.

Esto puede ser una fuente de confusión para los nuevos autores de un documento HTML, quienes pueden tratar de rellenar el texto con espacios adicionales para lograr la sangría deseada, para conseguir más espacio después de un punto entre oraciones o para introducir más espacio vertical entre los párrafos. Influir en el diseño visual de vuestros documentos no es algo que se logre desde el código HTML, sino que se logra a través de CSS.

## Elementos de bloque

En este subapartado explicaremos la sintaxis y el uso de los elementos de bloque más frecuentes utilizados para formatear texto.

### Títulos de sección de página

Una vez que hayáis dividido la página en secciones lógicas, cada una de estas secciones debería ir introducida por un título adecuado. De ello se habla con más detalle en el apartado Qué necesita una buena página web.

El HTML define seis niveles de títulos: `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>` y `<h6>` (desde el más importante hasta el menos importante). Hablando en general, `<h1>` sería el título principal de toda la página que introduciría el tema. `<h2>` se utilizaría para dividir la página en secciones, `<h3>` en subsecciones y así sucesivamente.

Es muy importante utilizar los niveles de títulos para describir el documento en referencia a las secciones, subsecciones, subsubsecciones, etc., ya que esto hace que el documento sea más [comprensible para los lectores de pantalla](http://www.accessibilitytips.com/2008/03/10/avoid-skipping-header-levels/) y para los procesos automatizados (como los robots de indexación de Google).

Un buen ejemplo de una estructura de títulos, utilizando este documento como plantilla, podría ser el siguiente:

``` html
<h1>Etiquetar contenido textual en HTML</h1>
<h2>Introducción</h2>
<h2>El espacio: la última frontera</h2>
<h2>Elementos de bloque</h2>
<h3>Títulos de sección de página</h3>
<h3>Párrafos genéricos</h3>
<h3>Citar otras fuentes</h3>
<h3>Texto preformateado</h3>
<h2>Elementos en línea</h2>

[…y así sucesivamente…]
```

### Párrafos genéricos

El párrafo es el componente básico de la mayoría de los documentos. En HTML, un párrafo se representa con el elemento p, que no tiene ningún atributo especial.

Por ejemplo:

``` html
<p>Este es un párrafo muy corto. Tiene soló dos oraciones.</p>
```

 En muchos artículos y libros, un párrafo puede contener sólo una frase. Aunque el significado (en cuanto a la prosa escrita) de la palabra párrafo está bastante claro, en la web hay áreas de texto mucho más cortas que a menudo aparecen entre elementos de párrafos por el simple hecho de que el autor cree que es más "semántico" que utilizar un elemento `<div>` (hablaremos de ello en otro apartado titulado "Contenedores genéricos").

Un párrafo es un conjunto de una o más frases, igual que en los periódicos y libros. En la web es una buena idea utilizar el elemento de párrafo para estos conjuntos de frases y no para cualquier parte aleatoria de texto de la página. Si son sólo unas cuantas palabras y no una frase propiamente dicha, entonces quizá sería mejor no etiquetarlo como un párrafo.

### Citar otras fuentes

A menudo, los artículos, los apuntes de bloques y los documentos de referencia citan total o parcialmente algún otro documento. En el HTML, estas citas se marcan con el elemento `<blockquote>` para citas largas, como frases enteras, párrafos, listas o similares.

Un elemento `<blockquote>` no puede contener texto, sino que debe tener en su interior otro elemento de bloque. Deberíais utilizar el mismo elemento de bloque que en el documento original. Si citáis un párrafo de texto, utilizad un párrafo; cuando citéis una lista, utilizad los elementos para listas; y así sucesivamente.

Si la cita es de otra página web, podéis indicarlo utilizando el atributo `cite`.

Como en el ejemplo siguiente:

``` html
<p>HTML 4.01 es la soló versión de HTML debes usar
 cuando estás creando una página web nueva, de acuerdo de la
especificación:</p>
<blockquote cite="http://www.w3.org/TR/html401/">
<p>Esto documento reemplaza versiones anteriores de HTML 4.0,
 pero W3C va continuar hacer esas especificaciones y
 su DTDs disponible a  el sitio web de W3C.</p>
</blockquote>
```

 Dependiente en el estilo, el content puede parece como esto en el navegador web:

HTML 4.01 es la soló versión de HTML debes usar cuando estás creando una página web nueva, de acuerdo de la especificación:

> Esto documento reemplaza versiones anteriores de HTML 4.0, pero W3C va continuar hacer esas especificaciones y su DTDs disponible a el sitio web de W3C.

El atributo `cite` no hace nada independiente, pero es útil para tener un registro de el origen de la cita en la misma pagina de la cita.

### Texto preformateado

Cualquier texto en el que el formato y el espacio en blanco (podéis ver más arriba) sean importantes se debería etiquetar con el elemento `pre`.

En la mayoría de los navegadores web, el texto marcado como preformateado se mostrará al usuario tal como aparezca en el código fuente, algunas veces utilizando un tipo de letra de ancho fijo, lo cual da al texto el aspecto de haber sido escrito con una máquina de escribir. Este uso de tipos de letras de ancho fijo es uno de los primeros recursos que utilizaron los programadores para el texto preformateado.

En éste podéis ver un fragmento de código escrito en el lenguaje de programación Perl:

``` html
<pre><code class="language-perl">
# read in the named file in its entirety
sub slurp {
   my $filename = shift;
   my $file     = new FileHandle $filename;

   if ( defined $file ) {
      local $/;
      return <$file>;
   }
   return undef;
};
</code></pre>
```

 El uso de `<code>` que se hace en este ejemplo se explicará en el apartado sobre los elementos semánticos menos conocidos, que encontraremos más adelante en este mismo módulo.

## Elementos en línea

En este subapartado explicaremos la sintaxis y el uso de los elementos en línea más frecuentes utilizados para formatear texto.

### Citas breves

Las citas breves que se utilizan en una frase o párrafo normal se ponen en el elemento `<q>`. Igual que el elemento `<blockquote>`, éste puede contener un atributo `cite`, que indica la página de Internet en la que se puede encontrar la cita.

Una cita breve aparece normalmente entre comillas. Según la [especificación HTML](http://www.w3.org/TR/html401/struct/text.html#h-9.2.2), estas citas las debe insertar el agente usuario para poder imbricarlas correctamente y que sepan el idioma que se utiliza en el documento. Se puede utilizar CSS para controlar las comillas utilizadas; este aspecto se tratará en el apartado sobre estilos de texto.

Un ejemplo de `<q>` en acción:

``` html
<p>Esto no terminar bien para mi. Ay pues,
      <q lang="fr">c'est la vie</q> como los francés dicen.</p>
```

### Énfasis

El HTML contiene dos métodos para indicar que el texto de su interior debe aparecer enfatizado delante del usuario, como por ejemplo los mensajes de error, las advertencias o las notas.

En los navegadores visuales esto significa normalmente la aplicación de un color o un tipo de letra diferente o la visualización del texto en negrita o cursiva. Para los usuarios de lectores de pantalla, el resultado puede ser una voz diferente o algún otro efecto acústico. Para presentar texto con énfasis hay que utilizar el elemento `<em>`.

Como en el ejemplo siguiente:

``` html
<p><em>Recuerda:</em>el hervidor es ser enchufado a noche.</p>
```

 Si hay que enfatizar toda una frase pero una parte concreta de ésta se debe enfatizar de una manera aún más importante, se debe utilizar el elemento `<strong>` para indicar un énfasis más fuerte de lo normal, como en el ejemplo siguiente:

``` html
<p><em>Recuerda: el hervidor<strong>debe</strong> ser desenchufado cada noche,
 o lo explotaría - <strong>matando todo</strong></em>.</p>
```

### Texto en cursiva

Normalmente se cree que la *cursiva* no describe el significado y que, por lo tanto, el elemento `<i>` no se debe utilizar (igual que muchos otros elementos presentacionales descritos en el subapartado siguiente).

Hay un par de casos en los que es correcto describir el contenido como cursiva. Ya se ha comentado que algunos conceptos se describen mejor como "cursiva" en lugar de tener que crear algunos elementos muy específicos y no utilizados. Éstos incluyen cosas como por ejemplo los nombres de barcos, los títulos de series de televisión, películas y libros, algunos términos técnicos y otras designaciones taxonómicas.

La razón es que la cursiva indica que el texto es especial y el contexto indica en qué sentido lo es. De hecho, esto ya queda reflejado en el borrador de la especificación de HTML5: "El elemento i representa un texto en una voz o un modo alternativo, o que de alguna manera queda fuera de la prosa normal. [...] El elemento i se debe utilizar como último recurso cuando no hay ningún otro elemento que sea más apropiado".

Como el CSS puede modificar el elemento `<i>` a fin de que no sea cursiva, en este contexto hay que interpretar el significado de "cursiva" fundamentalmente como "algo un tanto diferente". Yo no lo considero correcto, personalmente hablando, pero hay precedentes suficientes para utilizarlo de esta manera.

## Elementos presentacionales: no utilizar nunca

La especificación de HTML incluye varios elementos que se describen de manera general como "presentacionales", ya que sólo especifican qué aspecto debe tener el texto que contienen, pero no qué significan

La especificación ha etiquetado algunos de estos elementos como desaprobados. Eso significa que han sido sustituidos por un método más nuevo que permite conseguir los mismos resultados.

Aquí los describiremos brevemente, pero hay que tener en cuenta que esta explicación tiene casi exclusivamente un interés puramente histórico; estos elementos no se deben utilizar nunca en ninguna página web moderna. El efecto de todos estos elementos se debe conseguir de alguna otra manera, que se describirá en otros dos apartados: "Estilos de texto con el CSS" y "Elementos semánticos menos conocidos".

### `<font face="..." size="...">`

El navegador mostrará el texto en estos elementos utilizando un tipo de letra diferente del tipo por defecto; los tipos de letra, sin embargo, se deben definir con CSS.

### `<s>` y `<strike>`

El texto aparece rayado con una línea que lo atraviesa; si es sólo un efecto presentacional, este efecto se debería conseguir con CSS. Además, si el texto se quiere marcar como suprimido o no deseado, se debería etiquetar con el elemento del que se describe más adelante.

### `<u>`

El texto se subraya; es casi siempre un efecto visual y se debería conseguir con el CSS.

### `<tt>`

El texto se presenta en un tipo de letra de "teletipo" o de ancho fijo; este efecto se debería conseguir con el CSS o con algún elemento semántico más apropiado, como por ejemplo `<pre>`, tal como se ha visto anteriormente.

### `<big>` y `<small>`

Se ajusta el tamaño del texto; se debería conseguir con el CSS.

## Resumen

En este apartado hemos hablado de algunos de los elementos más comunes que se utilizan para etiquetar contenido textual. En el siguiente apartado hablaremos de otro tipo de contenido: las listas.
