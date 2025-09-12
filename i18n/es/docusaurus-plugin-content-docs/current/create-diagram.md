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

Las siguientes bases de datos son compatibles:

- MySQL
- PostgreSQL
- SQLite
- MariaDB
- MSSQL
- Oracle

Por el momento, la importación de diagramas SQL no está habilitada para Oracle Database.

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

Aunque únicamente el Nombre, Tipo de dato, No nulo y Primaria son visibles desde el panel de configuración, los demás campos se pueden definir en el panel de edición de la columna, que se abrirá al hacer clic en el ícono de los tres puntos.

<ThemedImage
    lightImageSrc={require("./img/light/more-options-fields.png").default}
    darkImageSrc={require("./img/dark/more-options-fields.png").default}
    alt="Editar campos"
/>

:::info

Si se definen varias claves primarias, se generará una clave primaria compuesta en la salida SQL.

:::

:::info

La restricción de verificación se inyectará en la salida SQL tal como está.

:::

:::info

Se pueden crear atributos secuencialmente presionando enter en el último campo.

:::

:::info

Para definir un atributo como llave primaria, selecciona la casilla con un ícono de llave. Si deseas que el atributo sea nulo o no nulo, selecciona la casilla con un ícono de signo de interrogación.

:::

### Índices

Puedes definir los siguientes campos para un índice:

- Campos
- Único
- Nombre

## Relaciones

Para crear una relación y definir claves foráneas, mantenga pulsado el punto azul en la clave principal y arrástrelo a la tabla con la que desea establecer la relación. Esto generará automáticamente la llave foránea en la tabla hija que contendrá la información de la clave principal.

<ThemedImage
    lightImageSrc={require("./img/light/create-relationship.gif").default}
    darkImageSrc={require("./img/dark/create-relationship.gif").default}
    alt="Crear una relación"
/>

El gif muestra una de las tres posibles notaciones seleccionables en el modelador; para cada notación, la representación y algunas acciones pueden variar.

<!-- Si en algún momento te das cuenta de que las claves están invertidas, puedes intercambiarlas desde la pestaña `Relaciones`. Abre la relación que deseas editar, haz clic en el botón de más (tres puntos) junto a las columnas primaria y foránea, y luego intercambia. -->

:::info

Para eliminar la relación, simplemente haga doble clic en la relación y seleccione el botón Eliminar o elimine la clave foránea generada automáticamente de la tabla.

:::

:::info

Para alternar entre relaciones identificativas y no identificativas, basta con dar doble clic, seleccionar el ícono de edición o abrir directamente el panel de configuración de la tabla hija y modificar el atributo de llave primaria. Si la llave foránea también forma parte de la llave primaria, la relación será identificativa; en caso contrario, será no identificativa.

:::

Puedes definir los siguientes campos para una relación:

- Nombre
- Tipo de relación
  - Uno a uno
  - Uno a muchos
  - Subtipo
  - Cardinalidad
    - Solo disponible para Uno a uno
      - (0,1)
      - (1,1)
    - Solo disponible para Uno a muchos
      - (0,*)
      - (1,*)
- Restricción de subtipo (Solo disponible para relaciones de subtipo)
  - Excluyente Total
  - Excluyente Parcial
  - Traslape Total
  - Traslape Parcial
- Acción al eliminar
- Acción al actualizar
  - Sin acción
  - Restringir
  - Cascada
  - Establecer nulo
  - Establecer por defecto

### Entidades de Supertipos y Subtipos

Para crear alguna relación que utilice este concepto, es necesario crear en primera instancia una relación comun y corriente para posteriormente ir a su panel de configuración y seleccionar en el apartado de tipos de relaciones el de subtipo.

Al seleccionarlo, la notación de la relación cambiará y se generará un punto azul al lado de esta, el cual permitirá añadir más subtipos a tu modelo de jerarquía.

<ThemedImage
    lightImageSrc={require("./img/light/subtype-relationship.gif").default}
    darkImageSrc={require("./img/dark/subtype-relationship.gif").default}
    alt="Create a relationship"
/>

:::info

Para eliminar cualquiera de los subtipos que participan en la relación, basta con eliminar la llave foranea que se genero en la tabla hija o bien acceder al panel de configuración de la relación y eliminar el subtipo que desees.

En caso de que se desee eliminar toda la relación de subtipo, basta con seleccionar el botón de eliminar relación.

:::
<FAQ header="¿Cómo puedo definir relaciones de muchos a muchos?">

Para modelar relaciones de muchos a muchos, deberás usar una tabla de unión.

Una tabla de unión es una tercera tabla que contiene claves foráneas a las dos tablas que deseas conectar. Además, puedes agregar cualquier otra columna específica de la relación a la tabla. Por ejemplo:

<ThemedImage lightImageSrc={require("./img/light/many-to-many.png").default} darkImageSrc={require("./img/dark/many-to-many.png").default} alt="Elige una base de datos" />

</FAQ>

## Áreas temáticas

Puedes agregar áreas temáticas desde la pestaña `Áreas temáticas` en la barra lateral o desde la barra de herramientas. Agrupan lógicamente las tablas en áreas temáticas para facilitar la navegación por el diagrama; tienen un propósito puramente visual y no se traducen en ninguna lógica SQL y no se reflejan en los scripts generados.
Puedes agregar áreas temáticas desde la pestaña `Áreas temáticas` en la barra lateral o desde la barra de herramientas. Agrupan lógicamente las tablas en áreas temáticas para facilitar la navegación por el diagrama; tienen un propósito puramente visual y no se traducen en ninguna lógica SQL ni se reflejan en los scripts generados.

## Notas

Puedes agregar notas desde la pestaña `Notas` en la barra lateral o desde la barra de herramientas. Puedes usar notas para capturar cualquier comentario adicional en el diagrama.
Puedes agregar notas desde la pestaña `Notas` en la barra lateral o desde la barra de herramientas. Puedes usar notas para capturar cualquier comentario adicional en el diagrama.

## Tipos personalizados

Si el tipo de diagrama admite tipos personalizados, habrá una pestaña adicional de `Tipos` en la barra lateral. En los diagramas genéricos, las siguientes conversiones se realizarán al exportar a SQL.

| **Base de datos** | **Comportamiento** |
| --- | --- |
| **MySQL/MariaDB** | Un JSON con la correspondiente validación de JSON |
| **PostgreSQL** | Un tipo compuesto |
| **SQLite** | BLOB |
| **MSSQL** | Un alias de tipo para el primer campo |

Al agregar un nuevo tipo, se agregará a la lista de tipos que puedes elegir al editar una columna.

## Enums (PostgreSQL)

Si el diagrama es para PostgreSQL, habrá una pestaña adicional de `Enums` en la barra lateral donde puedes definir valores de enumeración. Al agregar una nueva enumeración, se agregará a la lista de tipos que puedes elegir al editar una columna.
Si el diagrama es para PostgreSQL, habrá una pestaña adicional de `Enums` en la barra lateral donde puedes definir valores de enumeración. Al agregar una nueva enumeración, se agregará a la lista de tipos que puedes elegir al editar una columna.
