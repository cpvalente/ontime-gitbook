---
description: Use a custom stylesheet to define viewer styles
---

# Custom Styling

You can override the app-defined styles by changing a supplied CSS override file. The file is located in a user directory, which changes depending on your Operating System

**For PC users:**\
`AppData/Roaming/Ontime/styles/override.css`

**For Mac users:**\
`Library/Application Support/Ontime/styles/override.css`

**For Linux users:**\
`Home/Ontime/styles/override.css`



This feature can be toggled on / off at Settings -> Viewers.

### Notes on style overriding

There are a few **CSS variables** which allow for quick customisation of the viewers. This would be the fastest way to get some branding going

```
// COMMENTS FOR CONVENIENCE, REMEMBER THAT COMMENTS ARE NOT ALLOWED IN CSS
:root {
  --background-color-override: #f3f4f8;        // page background (default black)
  --color-override: #5051f9;                   // text colour (default white)
  --accent-color-override: #23235f;            // accent colour (default pink)
  --timer-color-override: #5051f9;             // timer colour (default white)
  --outdent-background-color-override: white;  // block background (default gray)
}
```

Alternatively, you can **define your own style sheets**. This means that you can fully customise any page as you wish. This implies inspecting the page to find the relevant selectors

```
// Overriding font for timers
.timer {
  font-family: "Comic Sans MS", serif !important;
}
```
