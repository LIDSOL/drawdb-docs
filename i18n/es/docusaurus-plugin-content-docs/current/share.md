---
sidebar_position: 6
---

import ThemedImage from '@site/src/components/ThemedImage';

# Compartir un diagrama

Comparte y recibe diagramas fácilmente con unos pocos clics.

## Cómo compartir

Comparte un diagrama haciendo clic en el botón `Compartir` en la barra de menú, luego copia y distribuye el enlace generado que se puede usar para obtener una copia del diagrama.

:::info

Compartir un diagrama no inicia una sesión de colaboración y no permite que otros editen tu instancia del diagrama.

:::

<ThemedImage lightImageSrc={require("./img/light/share.png").default} darkImageSrc={require("./img/dark/share.png").default} alt="Share" />

## Qué sucede cuando compartes

Cuando haces clic en `Compartir`, se crea un gist secreto con el json sin procesar del diagrama. Luego, cuando cargas un diagrama desde un enlace compartido, el json se carga desde el gist.

:::warning

Si bien los gists secretos no son visibles para los motores de búsqueda, siguen siendo visibles si alguien se encuentra con la URL.

:::

Para obtener más información sobre los gists, consulta la [Documentación de GitHub](https://docs.github.com/es/get-started/writing-on-github/editing-and-sharing-content-with-gists/creating-gists).

En caso de que quieras eliminar un gist, puedes hacer clic en el botón `Dejar de compartir`.

Además, el gist no se sincroniza con tu diagrama de trabajo a menos que vuelvas a compartir haciendo clic en el botón `Compartir` de nuevo.
