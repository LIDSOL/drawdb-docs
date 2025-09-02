---
sidebar_position: 8
---

# Cómo funciona

drawDB es una sencilla aplicación de ReactJS. A continuación se ofrece una descripción general de alto nivel de cómo se construyen las cosas, pero, en general, si te preguntas cómo funciona algo, lo primero que te viene a la mente es probablemente la respuesta.

## Lienzo del editor

El lienzo es un elemento `<svg/>` y toda la interacción se maneja a través de eventos de puntero. Las tablas, áreas y notas son elementos `<foreignObject/>`, las relaciones son `<path/>` que se calculan en función de las coordenadas y anchos de los campos de inicio y fin.

## Almacenamiento de diagramas

Los diagramas y las tablas se almacenan en el navegador, específicamente en IndexedDB. Dado que todo se almacena en el navegador, antes de restablecer o cambiar a un navegador diferente, si deseas guardar tus diagramas, expórtalos como archivos JSON.

Además, cuando compartes un diagrama, se crea un gist que contiene el diagrama en JSON.

## Exportación

Todas las funciones de exportación toman el diagrama y generan una cadena utilizando plantillas de cadena predefinidas.

## Importación

Puedes importar diagramas desde JSON o desde SQL.

Cuando importas desde SQL, el código fuente se pasa a un analizador y luego el AST resultante se utiliza para construir un objeto de diagrama.

## Internacionalización

i18n se utiliza para la internacionalización. Para agregar un nuevo idioma, todo lo que necesitas hacer es agregar `<tu-idioma>.js` similar a [`en.js`](https://github.com/drawdb-io/drawdb/blob/main/src/i18n/locales/en.js) pero con valores traducidos en `src/i18n/locales`.

<br/>

P.D. Si tienes alguna pregunta, contáctame en Discord. 
