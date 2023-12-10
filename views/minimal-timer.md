---
description: Just the event timer, nothing else.
---

# Minimal Timer

![A minimal stage timer, just a running timer](<../.gitbook/assets/103 minimal.png>)

Sometimes you just need a timer. This is it.

### URL Modifiers

Sometimes you need to customise that timer. This is also it.\


{% hint style="info" %}
With the minimal timer view, you can use the URL parameters the quickly customise the appearance of that clock. This pairs great with the [aliases feature](../features/url-aliases.md)

See below the customisable features, your URL would end up looking like

`http://127.0.0.1:4001/minimal?key=f00&text=0ff&font=arial&size=1.2&alignx=start&offsetx=100&aligny=end&offsety=-100&hidenav=true&hideovertime=false`


{% endhint %}

| Parameter            | Options                | URL                         | Action                                                                  |
| -------------------- | ---------------------- | --------------------------- | ----------------------------------------------------------------------- |
| Key                  | 00FF00                 | /minimal?key=00ff00         | Background colour in hexadecimal                                        |
| Text Colour          | FF00FF                 | /minimal?text=ff00ff        | Text colour in hexadecimal                                              |
| Text Background      | 000000a                | /minimal?textbg=000000a     | Colour of text background in hexadecimal                                |
| Font                 | Arial                  | /minimal?font=Arial         | Font family, will use the fonts available in the system                 |
| Text Size            | 0.0 - n                | /minimal?size=1.5           | Scales the current style (0.5 = 50% 1 = 100% 2 = 200%)                  |
| Align Horizontal     | start \| center \| end | /minimal?alignx=start       | Moves the horizontally in page to start = left \| center \| end = right |
| Offset Horizontal    | number                 | /minimal?offsetx=100        | Offsets the timer horizontal position by a given amount in pixels       |
| Align Vertical       | start \| center \| end | /minimal?aligny=end         | Moves the vertically in page to start = left \| center \| end = right   |
| Offset Vertical      | number                 | /minimal?offsety=-100       | Offsets the timer vertical position by a given amount in pixels         |
| Hide Nav             | true \| false          | /minimal?hidenav=true       | Whether to hide the nav logo in the right corner                        |
| Hide Overtime        | true \| false          | /minimal?hideovertime=true  | Whether to supress overtime styles (red borders and red text)           |
| Hide Message Overlay | true \| false          | /minimal?hidemessages=false | Whether to hide the overlay from showing timer screen messages          |



