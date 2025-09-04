---
sidebar_position: 2
---

import ThemedImage from '@site/src/components/ThemedImage';
import Flex from '@site/src/components/Flex';
import FAQ from '@site/src/components/FAQ';

# Crear un diagrama

Para comenzar, ve al [editor en línea](https://www.drawdb.app/editor). Si se carga un diagrama anterior, puedes ir a `Archivo > Nuevo` y elegir la opción de diagrama en blanco.

<Flex>
<ThemedImage 
    lightImageSrc={require("./img/light/file-new.png").default}
    darkImageSrc={require("./img/dark/file-new.png").default}
    alt="Nuevo archivo"
/>
<ThemedImage 
    lightImageSrc={require("./img/light/create-blank-diagram.png").default}
    darkImageSrc={require("./img/dark/create-blank-diagram.png").default}
    alt="Crear un diagrama en blanco"
/>
</Flex>

## Elige una base de datos

Puedes crear diagramas específicos de la base de datos o genéricos.

- Los diagramas genéricos se pueden importar o exportar a cualquiera de los sabores de SQL compatibles; sin embargo, admiten un número menor de tipos.
- Los diagramas específicos de la base de datos admiten todos los tipos de datos para la base de datos seleccionada y otras características específicas de la base de datos.

Se admiten las siguientes bases de datos:

- MySQL
- PostgreSQL
- SQLite
- MariaDB
- MSSQL

<ThemedImage
    lightImageSrc={require("./img/light/pick-db.png").default}
    darkImageSrc={require("./img/dark/pick-db.png").default}
    alt="Elige una base de datos"
/>

## Tablas

Agrega tablas desde la barra lateral o la barra de herramientas y define las columnas.

<ThemedImage
    lightImageSrc={require("./img/light/define-tables.gif").default} 
    darkImageSrc={require("./img/dark/define-tables.gif").default} 
    alt="Definir tablas"
/>

### Campos de la tabla

Puedes definir los siguientes campos para una columna:

- Nombre
- Tipo de dato
- No nulo
- Primaria
- Única
- Autoincremental
- Por defecto
- Restricción de verificación
- Comentario

:::info

Si se definen varias claves primarias, se generará una clave primaria compuesta en la salida SQL.

:::

:::info

La restricción de verificación se inyectará en la salida SQL tal como está.

:::

### Índices

Puedes definir los siguientes campos para un índice:

- Campos
- Único
- Nombre

## Relaciones

Para crear relaciones y definir claves foráneas, haz clic y mantén presionado el punto azul en la columna de la clave foránea, luego arrástralo y suéltalo en la columna de la clave primaria. Esta acción sigue la lógica de `columna_inicio REFERENCIA columna_fin`, donde la columna desde la que arrastras se designará como la clave foránea, vinculándola a la clave primaria en la columna de destino.

<ThemedImage
    lightImageSrc={require("./img/light/create-relationship.gif").default}
    darkImageSrc={require("./img/dark/create-relationship.gif").default}
    alt="Crear una relación"
/>

Por ejemplo, en la imagen de arriba, como `posts.user_id` es la clave foránea, comenzamos a arrastrar desde `user_id` a `users.id`.

Si en algún momento te das cuenta de que las claves están invertidas, puedes intercambiarlas desde la pestaña `Relaciones`. Abre la relación que deseas editar, haz clic en el botón de más (tres puntos) junto a las columnas primaria y foránea, y luego intercambia.

Puedes definir los siguientes campos para una relación:

- Nombre
- Cardinalidad
  - Uno a uno
  - Uno a muchos
  - Muchos a uno
- Acción al eliminar
- Acción al actualizar
  - Sin acción
  - Restringir
  - Cascada
  - Establecer nulo
  - Establecer por defecto

<FAQ header="¿Cómo puedo definir relaciones de muchos a muchos?">

Para modelar relaciones de muchos a muchos, deberás usar una tabla de unión.

Una tabla de unión es una tercera tabla que contiene claves foráneas a las 2 tablas que deseas conectar. Además, puedes agregar cualquier otra columna específica de la relación a la tabla. Por ejemplo:

<ThemedImage lightImageSrc={require("./img/light/many-to-many.png").default} darkImageSrc={require("./img/dark/many-to-many.png").default} alt="Elige una base de datos" />

</FAQ>

## Áreas temáticas

Puedes agregar áreas temáticas desde la pestaña `Áreas temáticas` en la barra lateral o desde la barra de herramientas. Agrupan lógicamente las tablas en áreas temáticas para facilitar la navegación por el diagrama; tienen un propósito puramente visual y no se traducen en ninguna lógica SQL y no se reflejan en los scripts generados.

## Notas

Puedes agregar notas desde la pestaña `Notas` en la barra lateral o desde la barra de herramientas. Puedes usar notas para capturar cualquier comentario adicional en el diagrama.

## Tipos personalizados

Si el tipo de diagrama admite tipos personalizados, habrá una pestaña adicional de `Tipos` en la barra lateral. En los diagramas genéricos, las siguientes conversiones se realizarán al exportar a SQL.

| **Base de datos** | **Comportamiento** |
| --- | --- |
| **MySQL/MariaDB** | Un JSON con la correspondiente verificación de validación de JSON |
| **PostgreSQL** | Un tipo compuesto |
| **SQLite** | BLOB |
| **MSSQL** | Un alias de tipo para el primer campo |

Al agregar un nuevo tipo, se agregará a la lista de tipos que puedes elegir al editar una columna.

## Enums (PostgreSQL)

Si el diagrama es para PostgreSQL, habrá una pestaña adicional de `Enums` en la barra lateral donde puedes definir valores de enumeración. Al agregar una nueva enumeración, se agregará a la lista de tipos que puedes elegir al editar una columna.
