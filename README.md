# Bottega-M1C1

M1C1 CSS Grid Assignment

https://github.com/catharygr/Bottega-M1C1

¿Cuáles son algunas de las cosas que hacen que SCSS sea diferente de CSS? (coloca ejemplos)

El SCSS es un superset de CSS, que contiene todo el código de CSS y además está amplificado con variables, funciones, mixins, nesting, etc. Aunque en los últimos años he notado que el CSS ha incluido muchas de estas funcionalidades, como por ejemplo: variables, nidados, etc.

---

¿Qué es una variable SCSS? (porque crees que debes utilizarla pon un ejemplo de una variable, escribe una variable y como se pondría para utilizarla)

Una variable SCSS es una propiedad que nos permite reutilizar su valor en todo el proyecto sin tener que reescribir el valor en cada clase. Cuando cambiamos el valor de la variable, automáticamente se propaga en todo el proyecto sin que tengamos que cambiarlo manualmente.

$font-size-xl: 3rem;

h1 {
font-size: $font-size-xl;
}

---

¿Qué es un SCSS Mixin? (porque crees que debes utilizarla pon un ejemplo de un mixin, escribiendo cómo se crea y como se pondría para utilizarla)

El SCSS Mixin es parecido a una variable, pero en lugar de contener solo un valor, en este caso podemos escribir un bloque de CSS para reutilizarlo en partes del código que nos convenga. El mixin puede tener parámetros, lo que le da flexibilidad a la hora de reutilizarlo. Por ejemplo, podemos declarar un Flexbox:

@mixin centrar-con-flex($gap: 0) {
display: flex;
justify-content: center;
align-items: center;
gap: $gap;
}

Se usa así:

.container {
@include centrar-con-flex(20px);
// Y el resto del código CSS
}

---

¿Qué significa Unidad fraccionaria (fr) con CSS Grid?

Un fr es una fracción del espacio que ocupa el grid. Por ejemplo, tenemos un grid de dos columnas donde la primera columna es una fracción y la segunda es dos fracciones. El navegador divide la anchura en tres partes iguales, donde la primera parte corresponde a una fracción y a la segunda se le asignan dos fracciones. Todas las fracciones tienen el mismo tamaño.
