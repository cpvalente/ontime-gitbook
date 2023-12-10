---
description: Just a big fat clock, nothing else.
---

# Clock

![Just the current time](<../.gitbook/assets/102 clock.png>)

Sometimes you just need to know the time. This is it.

### URL Modifiers

Sometimes you need to customise that timer. This is also it.\


{% hint style="info" %}
With the clock view, you can use the URL parameters the quickly customise the appearance of that clock. This pairs great with the [aliases feature](../features/url-aliases.md)

See below the customisable features, your URL would end up looking like

`http://127.0.0.1:4001/clock?key=f00&text=0ff&font=arial&size=1.2&alignx=start&offsetx=100&aligny=end&offsety=-100`


{% endhint %}

| Parameter           | Options                | URL                   | Action                                                                                        |
| ------------------- | ---------------------- | --------------------- | --------------------------------------------------------------------------------------------- |
| Key                 | 00FF00                 | /clock?key=00ff00     | Background colour in hexadecimal                                                              |
| Text Colour         | FF00FF                 | /clock?text=ff00ff    | Text colour in hexadecimal                                                                    |
| Text Background     | 000000a                | /clock?textbg=000000a | Colour of text background in hexadecimal                                                      |
| Font                | Arial                  | /clock?font=Arial     | Font family, will use the fonts available in the system                                       |
| Text Size           | 0.0 - n                | /clock?size=1.5       | Scales the current style (0.5 = 50% 1 = 100% 2 = 200%)                                        |
| Align Horizontal    | start \| center \| end | /clock?alignx=start   | Moves the horizontally in page to start = left \| center \| end = right                       |
| Offset Horizontal   | number                 | /clock?offsetx=100    | Offsets the timer horizontal position by a given amount in pixels                             |
| Align Vertical      | start \| center \| end | /clock?aligny=end     | Moves the vertically in page to start = left \| center \| end = right                         |
| Offset Vertical     | number                 | /clock?offsety=-100   | Offsets the timer vertical position by a given amount in pixels                               |
| Hide Nav            | true \| false          | /clock?hidenav=true   | Whether to hide the nav logo in the right corner                                              |
|                     |                        |                       |                                                                                               |
| 12  / 24 hour timer | 12 \| 24               | /clock?format=12      | Whether to show the time in 12 or 24 hour mode. Overrides the global setting from preferences |



