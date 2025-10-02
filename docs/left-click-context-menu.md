---
sidebar_position: 2
---

import ThemedImage from '../src/components/ThemedImage';
import Flex from '../src/components/Flex';
import FAQ from '../src/components/FAQ';

# Left Click Context Menu

This menu was created to provide quick configuration for objects inside the canvas diagram area. Depending on the context menu displayed there will be different options. In order to close any context menu just left click anywhere outside the menu or open another context menu.

## Canvas Context Menu

The most general context menu is for all the diagram area, to open it just left click anywhere in the canvas area that is not occupied by an object. This will open a small menu next to the mouse cursor. like the one in the image below.

<Flex>
<ThemedImage
    lightImageSrc={require("./img/light/context_menu/canvas_context_menu.png").default}
    darkImageSrc={require("./img/dark/context_menu/canvas_context_menu.png").default}
    alt="Open canvas context menu"
/>
</Flex>

### Canvas Context Menu Options

| Option | Description |
| --- | --- |
| **Add table** | Creates a new database table in the diagram. Click to add a table with default columns that you can customize. |
| **Add area** | Adds a visual area/container to group related tables or organize your diagram layout. |
| **Add note** | Inserts a text note or comment anywhere on the canvas to document your database design. |
| **Undo** | Reverts the last action performed on the diagram (Ctrl+Z shortcut). |
| **Redo** | Re-applies the last undone action (Ctrl+Y shortcut). It is disabled when no actions to redo. |
| **Area Selection** | Enables area selection mode to select multiple objects by dragging a selection rectangle. |

## Table Context Menu

The table context menu provides options specific to the selected table. To open it, right-click on a table in the diagram, specifically on the table header or an empty area within the table. This will display the following options:

<Flex>
<ThemedImage
    lightImageSrc={require("./img/light/context_menu/table_context_menu.png").default}
    darkImageSrc={require("./img/dark/context_menu/table_context_menu.png").default}
/>
</Flex>

### Table Context Menu Options

| Option | Description |
| --- | --- |
| **Edit** | Opens the table editor side panel to modify table properties, including name, columns, indexes, and constraints. |
| **Rename** | Allows you to quickly rename the table without opening the full editor side panel. |
| **Add field** | Adds a new column/field to the selected table with default properties that you can customize. |
| **Delete** | Removes the selected table from the diagram. |

## Field Context Menu

The field context menu provides options specific to the selected field/column within a table. To open it, right-click on a field in the table. This will display the following options:

<Flex>
<ThemedImage
    lightImageSrc={require("./img/light/context_menu/field_context_menu.png").default}
    darkImageSrc={require("./img/dark/context_menu/field_context_menu.png").default}
/>
</Flex>

### Field Context Menu Options

| Option | Description |
| --- | --- |
| **Edit** | Opens the field editor side panel to modify field properties, including name, data type, constraints, and default values. |
| **Rename** | This will open a pop-up window to quickly rename the field without opening the full editor side panel. When a foreign key field is selected, the pop-up will also allow you to update the referenced table and column. |
| **Set Primary Key** | Sets the primary key constraint on the field. This option appears when the field is not currently a primary key. |
| **Remove Primary Key** | Removes the primary key constraint from the field. This option appears when the field is currently set as a primary key. **Note:** If the primary key is also a foreign key, the foreign key constraint must be removed first. |
| **Allow NULL** | Changes the field to allow NULL values. This option appears when the field is currently set to NOT NULL. **Note:** This option is not available for primary key fields. |
| **Set NOT NULL** | Sets the field to NOT NULL, meaning it cannot accept NULL values. This option appears when the field currently allows NULL values. |
| **Set Unique** | Adds a unique constraint to the field, ensuring all values in this column are distinct. This option only appears if the field does not currently have a unique constraint. |
| **Remove Unique** | Removes the unique constraint from the field. This option only appears if the field currently has a unique constraint. **Note:** This constraint cannot be removed if the field is a primary key. |
| **Enable Auto Increment** | Enables the auto-increment property on the field, which automatically generates a unique value for new records. This option only appears if the field does not currently have auto-increment enabled. |
| **Disable Auto Increment** | Disables the auto-increment property on the field. This option only appears if the field currently has auto-increment enabled. |
| **Delete** | Removes the selected field from the table. |

## Relationship Context Menu

The relationship context menu provides options specific to the selected relationship/connection between tables. To open it, right-click on a relationship line in the diagram. This will display the following options:

<Flex>
<ThemedImage
    lightImageSrc={require("./img/light/context_menu/relationship_context_menu.png").default}
    darkImageSrc={require("./img/dark/context_menu/relationship_context_menu.png").default}
/>
</Flex>

### Relationship Context Menu Options

| Option | Description |
| --- | --- |
| **Edit** | Opens the relationship editor dialog to modify relationship properties, including name, cardinality, and other settings. |
| **Set Default Name** | Resets the relationship name to the automatically generated default name based on the connected tables. |
| **Rename** | Opens a dialog to quickly rename the relationship without accessing the full editor. |
| **Swap Direction** | Reverses the direction of the relationship, switching which table is the parent and which is the child. |
| **Show Label** | Toggles the visibility of the relationship label/name on the diagram. When enabled, the relationship name appears in the middle of the connection line. |
| **Relationship Type** | Opens a submenu to change the type of relationship (one-to-one, one-to-many and subtype). |
| **Cardinality** | Opens a submenu to modify the cardinality settings for the relationship. For One-to-Many relationships, available values include (1, _), (0, _), and custom values where \* can be replaced with any number greater than 1. For One-to-One relationships, available values are (1, 1) and (0, 1). |
| **Delete** | Removes the selected relationship from the diagram. **Note:** This will also remove any foreign key constraints associated with this relationship. |

## Subtype Relationship Context Menu

Once a subtype relationship is created, you can access its context menu by right-clicking on the subtype relationship line in the diagram. This will display the following options:

<Flex>
<ThemedImage
    lightImageSrc={require("./img/light/context_menu/subtype_context_menu.png").default}
    darkImageSrc={require("./img/dark/context_menu/subtype_context_menu.png").default}
/>
</Flex>

### Subtype Relationship Context Menu Options

The options are the same as the regular relationship context menu, with the exception of the "Cardinality" option, which is not available for subtype relationships.

| Option | Description |
| --- | --- |
| **Edit** | Opens the relationship editor dialog to modify relationship properties, including name, cardinality, and other settings. |
| **Set Default Name** | Resets the relationship name to the automatically generated default name based on the connected tables. |
| **Rename** | Opens a dialog to quickly rename the relationship without accessing the full editor. |
| **Swap Direction** | Reverses the direction of the relationship, switching which table is the parent and which is the child. |
| **Show Label** | Toggles the visibility of the relationship label/name on the diagram. When enabled, the relationship name appears in the middle of the connection line. |
| **Relationship Type** | Opens a submenu to change the type of relationship (one-to-one, one-to-many and subtype). **Note:** When changing from subtype to another relationship type, only the connection to the first table in the subtype relationship will be preserved. |
| **Delete** | This option provides also the property to delete only one of the connections in the subtype relationship or delete the entire relationship. |

## Note Context Menu

The note context menu provides options specific to the selected note in the diagram. To open it, right-click on a note. This will display the following options:

<Flex>
<ThemedImage
    lightImageSrc={require("./img/light/context_menu/note_context_menu.png").default}
    darkImageSrc={require("./img/dark/context_menu/note_context_menu.png").default}
/>
</Flex>

### Note Context Menu Options

| Option | Description |
| --- | --- |
| **Edit** | Opens the note editor side panel to modify all note properties, including content, color, and position settings. |
| **Rename** | Allows you to quickly change the note's title without opening the full editor side panel. |
| **Edit Content** | Opens a text editor specifically for modifying the note's content/body text. |
| **Change Color** | Opens the note editor side panel to modify note color. |
| **Delete** | Removes the selected note from the diagram. |

## Area Context Menu

The area context menu provides options specific to the selected area/container in the diagram. To open it, right-click on an area. This will display the following options:

<Flex>
<ThemedImage
    lightImageSrc={require("./img/light/context_menu/area_context_menu.png").default}
    darkImageSrc={require("./img/dark/context_menu/area_context_menu.png").default}
/>
</Flex>

### Area Context Menu Options

| Option | Description |
| --- | --- |
| **Edit** | Opens the area editor side panel to modify area properties, including name, color, size, and position settings. |
| **Rename** | Allows you to quickly change the area's name/title without opening the full editor side panel. |
| **Change Color** | Opens the area editor side panel to modify area color. |
| **Delete** | Removes the selected area from the diagram. **Note:** This will not delete the tables or objects inside the area, only the container itself. |
