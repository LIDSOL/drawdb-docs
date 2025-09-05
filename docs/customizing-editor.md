---
sidebar_position: 3
---

import ThemedImage from '../src/components/ThemedImage';

# Customizing the editor

You can customize editor settings in the `View` menu.

<ThemedImage lightImageSrc={require("./img/light/menu-view.png").default} darkImageSrc={require("./img/dark/menu-view.png").default} alt="New File" />

## Settings

| Setting | Description | Shortcut |
| --- | --- | --- |
| Menubar | Toggle the menubar (header section containing diagram name and menus) | N/A |
| Sidebar | Toggle the sidebar (panel to the right) | N/A |
| Issues | Toggle the issues section in the sidebar | N/A |
| Strict mode | Disable error checking | Ctrl+Shift+M |
| Presentation mode | Enter presentation mode | N/A |
| Field details | Disable showing pop ups when you hover over tables | Ctrl+Shift+F |
| Reset view | Set the canvas cooridantes and zoom to default | Ctrl+R |
| Show grid | Toggle the canvas grid | Ctrl+Shift+G |
| Show cardinality | Toggle showing cardinality labels(1, n) for relationships | N/A |
| Notation | Set notation style for relationships | N/A |
| Show relationship labels | Toggle showing relationship names on the diagram | N/A |
| Show debug coordinates | Display debug coordinate information | N/A |
| Theme | Set the editor theme to dark or light | N/A |
| Zoom in | Set editor zoom | Ctrl+(Wheel/Up) |
| Zoom out | Set editor zoom | Ctrl+(Wheel/Down) |
| Fullscreen | Enter fullscreen | N/A |

To personalize your default settings you can select the default option on your settings menu to change various aspects such as fefault data type, change if null or not null is default,change to capital letters among other things.


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
