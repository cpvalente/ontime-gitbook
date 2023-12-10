---
description: Using the lower thids in OBS Studio
---

# Note: Lower thirds in OBS

It is possible to use the lower thirds feature in OBS in any networked machine using the Browser Renderer.

* Please use an appropriate URL as defined in the [Lower Thirds Section ](../views/lower-thirds.md)
* Remember to clear the CSS properties to ensure a transparent background (on by default in OBS)
* The options "Shutdown source when not visible" and "Refresh browser when scene becomes active" ensures that the lower third animation play on load / unload

```
body { background-color: rgba(0, 0, 0, 0); margin: 0px auto; overflow: hidden; }
```

![Please note use of Custom CSS and active Shutdown and Reload scene properties](<../.gitbook/assets/broweser window settings.png>)

