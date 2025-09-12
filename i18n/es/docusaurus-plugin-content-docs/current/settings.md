---
sidebar_position: 4
---

import ThemedImage from '@site/src/components/ThemedImage';

# Configuración general

Puedes personalizar la configuración general del editor en el menú `Configuración`.

<ThemedImage lightImageSrc={require("./img/light/settings.png").default} darkImageSrc={require("./img/dark/settings.png").default} alt="New File" />

Esta configuración se guarda en el almacenamiento local y se aplica a todos tus diagramas.

## Configuración

| Configuración | Descripción |
| -------- | ------- |
| Mostrar línea de tiempo | Muestra el historial de edición del diagrama. Esto es esencialmente todos los elementos en la pila utilizados para deshacer cambios. |
| Autoguardado | Desactiva / activa el guardado automático de cambios. |
| Desplazamiento | Desactiva / activa el movimiento del lienzo. |
| Ancho de la tabla | Establece el ancho de las tablas. |
| Defaults | Establece los valores de campo y tamaños de tipo predeterminados para los nuevos campos. |
| Idioma | Establece el idioma de la interfaz de usuario. |
| Vaciar almacenamiento | Esto elimina permanentemente todos los diagramas y plantillas de IndexedDB. |

Para personalizar tus valores predeterminados puedes seleccionar la opción de valores predeterminados en el menú de configuración para cambiar varios aspectos, como el tipo de dato por defecto, si el valor nulo o no nulo es el predeterminado, cambiar a mayúsculas, entre otros.

<div style={{ textAlign: "center" }}>
  <ThemedImage
    lightImageSrc={require("./img/light/Default1.jpeg").default}
    darkImageSrc={require("./img/dark/Default1.jpeg").default}
    alt="New File"
  />
</div>

<div style={{ textAlign: "center" }}>
  <ThemedImage
    lightImageSrc={require("./img/light/Default2.jpeg").default}
    darkImageSrc={require("./img/dark/Default2.jpeg").default}
    alt="New File"
  />
</div>
