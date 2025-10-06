---
sidebar_position: 2
---

import ThemedImage from '@site/src/components/ThemedImage';
import Flex from '@site/src/components/Flex';
import FAQ from '@site/src/components/FAQ';

# Menú Contextual de Clic Izquierdo

Este menú fue creado para proporcionar configuración rápida para objetos dentro del área del diagrama del lienzo. Dependiendo del menú contextual mostrado, habrá diferentes opciones. Para cerrar cualquier menú contextual, simplemente haz clic izquierdo en cualquier lugar fuera del menú o abre otro menú contextual.

## Menú Contextual del Lienzo

El menú contextual más general es para toda el área del diagrama, para abrirlo simplemente haz clic izquierdo en cualquier lugar del área del lienzo que no esté ocupado por un objeto. Esto abrirá un pequeño menú junto al cursor del ratón, como el que se muestra en la imagen a continuación.

<Flex>
<ThemedImage
    lightImageSrc={require("./img/light/context_menu/canvas_context_menu.png").default}
    darkImageSrc={require("./img/dark/context_menu/canvas_context_menu.png").default}
    alt="Abrir menú contextual del lienzo"
/>
</Flex>

### Opciones del Menú Contextual del Lienzo

| Opción | Descripción |
| --- | --- |
| **Agregar tabla** | Crea una nueva tabla de base de datos en el diagrama. Haz clic para agregar una tabla con columnas predeterminadas que puedes personalizar. |
| **Agregar área** | Añade un área/contenedor visual para agrupar tablas relacionadas u organizar el diseño de tu diagrama. |
| **Agregar nota** | Inserta una nota de texto o comentario en cualquier lugar del lienzo para documentar el diseño de tu base de datos. |
| **Deshacer** | Revierte la última acción realizada en el diagrama (atajo Ctrl+Z). |
| **Rehacer** | Vuelve a aplicar la última acción deshecha (atajo Ctrl+Y). Está deshabilitado cuando no hay acciones para rehacer. |
| **Selección de área** | Habilita el modo de selección de área para seleccionar múltiples objetos arrastrando un rectángulo de selección. |

## Menú Contextual de Tabla

El menú contextual de tabla proporciona opciones específicas para la tabla seleccionada. Para abrirlo, haz clic derecho en una tabla del diagrama, específicamente en el encabezado de la tabla o en un área vacía dentro de la tabla. Esto mostrará las siguientes opciones:

<Flex>
<ThemedImage
    lightImageSrc={require("./img/light/context_menu/table_context_menu.png").default}
    darkImageSrc={require("./img/dark/context_menu/table_context_menu.png").default}
/>
</Flex>

### Opciones del Menú Contextual de Tabla

| Opción | Descripción |
| --- | --- |
| **Editar** | Abre el panel lateral del editor de tabla para modificar las propiedades de la tabla, incluyendo nombre, columnas, índices y restricciones. |
| **Renombrar** | Te permite cambiar rápidamente el nombre de la tabla sin abrir el panel lateral completo del editor. |
| **Agregar campo** | Añade una nueva columna/campo a la tabla seleccionada con propiedades predeterminadas que puedes personalizar. |
| **Eliminar** | Elimina la tabla seleccionada del diagrama. |

## Menú Contextual de Campo

El menú contextual de campo proporciona opciones específicas para el campo/columna seleccionado dentro de una tabla. Para abrirlo, haz clic derecho en un campo de la tabla. Esto mostrará las siguientes opciones:

<Flex>
<ThemedImage
    lightImageSrc={require("./img/light/context_menu/field_context_menu.png").default}
    darkImageSrc={require("./img/dark/context_menu/field_context_menu.png").default}
/>
</Flex>

### Opciones del Menú Contextual de Campo

| Opción | Descripción |
| --- | --- |
| **Editar** | Abre el panel lateral del editor de campo para modificar las propiedades del campo, incluyendo nombre, tipo de datos, restricciones y valores predeterminados. |
| **Renombrar** | Esto abrirá una ventana emergente para cambiar rápidamente el nombre del campo sin abrir el panel lateral completo del editor. Cuando se selecciona un campo de clave foránea, la ventana emergente también te permitirá actualizar la tabla y columna referenciadas. |
| **Establecer clave primaria** | Establece la restricción de clave primaria en el campo. Esta opción aparece cuando el campo no es actualmente una clave primaria. |
| **Quitar clave primaria** | Elimina la restricción de clave primaria del campo. Esta opción aparece cuando el campo está actualmente establecido como clave primaria. **Nota:** Si la clave primaria también es una clave foránea, la restricción de clave foránea debe eliminarse primero. |
| **Permitir NULL** | Cambia el campo para permitir valores NULL. Esta opción aparece cuando el campo está actualmente establecido como NOT NULL. **Nota:** Esta opción no está disponible para campos de clave primaria. |
| **Establecer NOT NULL** | Establece el campo como NOT NULL, lo que significa que no puede aceptar valores NULL. Esta opción aparece cuando el campo actualmente permite valores NULL. |
| **Establecer único** | Añade una restricción única al campo, asegurando que todos los valores en esta columna sean distintos. Esta opción solo aparece si el campo no tiene actualmente una restricción única. |
| **Quitar único** | Elimina la restricción única del campo. Esta opción solo aparece si el campo tiene actualmente una restricción única. **Nota:** Esta restricción no se puede eliminar si el campo es una clave primaria. |
| **Habilitar autoincremento** | Habilita la propiedad de autoincremento en el campo, que genera automáticamente un valor único para nuevos registros. Esta opción solo aparece si el campo no tiene actualmente el autoincremento habilitado. |
| **Deshabilitar autoincremento** | Deshabilita la propiedad de autoincremento en el campo. Esta opción solo aparece si el campo tiene actualmente el autoincremento habilitado. |
| **Eliminar** | Elimina el campo seleccionado de la tabla. |

## Menú Contextual de Relación

El menú contextual de relación proporciona opciones específicas para la relación/conexión seleccionada entre tablas. Para abrirlo, haz clic derecho en una línea de relación en el diagrama. Esto mostrará las siguientes opciones:

<Flex>
<ThemedImage
    lightImageSrc={require("./img/light/context_menu/relationship_context_menu.png").default}
    darkImageSrc={require("./img/dark/context_menu/relationship_context_menu.png").default}
/>
</Flex>

### Opciones del Menú Contextual de Relación

| Opción | Descripción |
| --- | --- |
| **Editar** | Abre el panel lateral del editor de relación para modificar las propiedades de la relación, incluyendo nombre, cardinalidad y otras configuraciones. |
| **Establecer nombre predeterminado** | Restablece el nombre de la relación al nombre predeterminado generado automáticamente basado en las tablas conectadas. |
| **Renombrar** | Abre un diálogo para cambiar rápidamente el nombre de la relación sin acceder al panel lateral completo del editor. |
| **Intercambiar dirección** | Invierte la dirección de la relación, cambiando qué tabla es la padre y cuál es la hija. |
| **Mostrar etiqueta** | Alterna la visibilidad de la etiqueta/nombre de la relación en el diagrama. Cuando está habilitado, el nombre de la relación aparece en el medio de la línea de conexión. |
| **Tipo de relación** | Abre un submenú para cambiar el tipo de relación (uno-a-uno, uno-a-muchos y subtipo). |
| **Cardinalidad** | Abre un submenú para modificar las configuraciones de cardinalidad de la relación. Para relaciones Uno-a-Muchos, los valores disponibles incluyen (1, _), (0, _), y valores personalizados donde \* puede ser reemplazado con cualquier número mayor a 1. Para relaciones Uno-a-Uno, los valores disponibles son (1, 1) y (0, 1). |
| **Eliminar** | Elimina la relación seleccionada del diagrama. **Nota:** Esto también eliminará cualquier restricción de clave foránea asociada con esta relación. |

## Menú Contextual de Relación de Subtipo

Una vez que se crea una relación de subtipo, puedes acceder a su menú contextual haciendo clic derecho en la línea de relación de subtipo en el diagrama. Esto mostrará las siguientes opciones:

<Flex>
<ThemedImage
    lightImageSrc={require("./img/light/context_menu/subtype_context_menu.png").default}
    darkImageSrc={require("./img/dark/context_menu/subtype_context_menu.png").default}
/>
</Flex>

### Opciones del Menú Contextual de Relación de Subtipo

Las opciones son las mismas que el menú contextual de relación regular, con la excepción de la opción "Cardinalidad", que no está disponible para relaciones de subtipo.

| Opción | Descripción |
| --- | --- |
| **Editar** | Abre el panel lateral del editor de relación para modificar las propiedades de la relación, incluyendo nombre, cardinalidad y otras configuraciones. |
| **Establecer nombre predeterminado** | Restablece el nombre de la relación al nombre predeterminado generado automáticamente basado en las tablas conectadas. |
| **Renombrar** | Abre un diálogo para cambiar rápidamente el nombre de la relación sin acceder al panel lateral completo del editor. |
| **Intercambiar dirección** | Invierte la dirección de la relación, cambiando qué tabla es la padre y cuál es la hija. |
| **Mostrar etiqueta** | Alterna la visibilidad de la etiqueta/nombre de la relación en el diagrama. Cuando está habilitado, el nombre de la relación aparece en el medio de la línea de conexión. |
| **Tipo de relación** | Abre un submenú para cambiar el tipo de relación (uno-a-uno, uno-a-muchos y subtipo). **Nota:** Al cambiar de subtipo a otro tipo de relación, solo se preservará la conexión con la primera tabla en la relación de subtipo. |
| **Eliminar** | Esta opción también proporciona la propiedad de eliminar solo una de las conexiones en la relación de subtipo o eliminar toda la relación. |

## Menú Contextual de Nota

El menú contextual de nota proporciona opciones específicas para la nota seleccionada en el diagrama. Para abrirlo, haz clic derecho en una nota. Esto mostrará las siguientes opciones:

<Flex>
<ThemedImage
    lightImageSrc={require("./img/light/context_menu/note_context_menu.png").default}
    darkImageSrc={require("./img/dark/context_menu/note_context_menu.png").default}
/>
</Flex>

### Opciones del Menú Contextual de Nota

| Opción | Descripción |
| --- | --- |
| **Editar** | Abre el panel lateral del editor de nota para modificar todas las propiedades de la nota, incluyendo contenido, color y configuraciones de posición. |
| **Renombrar** | Te permite cambiar rápidamente el título de la nota sin abrir el panel lateral completo del editor. |
| **Editar contenido** | Abre un editor de texto específicamente para modificar el contenido/texto del cuerpo de la nota. |
| **Cambiar color** | Abre el panel lateral del editor de nota para modificar el color de la nota. |
| **Eliminar** | Elimina la nota seleccionada del diagrama. |

## Menú Contextual de Área

El menú contextual de área proporciona opciones específicas para el área/contenedor seleccionado en el diagrama. Para abrirlo, haz clic derecho en un área. Esto mostrará las siguientes opciones:

<Flex>
<ThemedImage
    lightImageSrc={require("./img/light/context_menu/area_context_menu.png").default}
    darkImageSrc={require("./img/dark/context_menu/area_context_menu.png").default}
/>
</Flex>

### Opciones del Menú Contextual de Área

| Opción | Descripción |
| --- | --- |
| **Editar** | Abre el panel lateral del editor de área para modificar las propiedades del área, incluyendo nombre, color, tamaño y configuraciones de posición. |
| **Renombrar** | Te permite cambiar rápidamente el nombre/título del área sin abrir el panel lateral completo del editor. |
| **Cambiar color** | Abre el panel lateral del editor de área para modificar el color del área. |
| **Eliminar** | Elimina el área seleccionada del diagrama. **Nota:** Esto no eliminará las tablas u objetos dentro del área, solo el contenedor en sí. |
