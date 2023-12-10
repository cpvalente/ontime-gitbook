---
description: A configurable view meant for Lower Third overlays on video feeds
---

# Lower Thirds

{% hint style="info" %}
https://MY.IP.ADDRESS:4001/lower       > [Lower Thirds](lower-thirds.md)
{% endhint %}

![Lower third view](<../.gitbook/assets/106 lower.jpg>)

{% hint style="info" %}
This workflow is thought and tested to be integrated with video servers capable of rendering a webpage, such as [OBS Studio ](../features/note-lower-thirds-in-obs.md)or disguise d3.&#x20;

The ontime view is not able to composite video
{% endhint %}

### URL Modifiers

The Lower Third views are configurable by using URL parameters

{% hint style="info" %}
You can chain parameters using the & character

eg: _/lower?bg=ff2\&text=f00\&size=0.6\&transition=5_
{% endhint %}

<table data-header-hidden><thead><tr><th>Parameter</th><th>Options</th><th width="150">URL</th><th>Action</th></tr></thead><tbody><tr><td>Parameter</td><td>Options</td><td>URL</td><td>Action</td></tr><tr><td>Preset</td><td>0-1</td><td>/lower?preset=1</td><td>Selects a style preset</td></tr><tr><td>Size</td><td>0.0 - n</td><td>/lower?size=0.8</td><td>Scales the current style (0.5 = 50% 1 = 100% 2 = 200%)</td></tr><tr><td>Transition</td><td>0 - n</td><td>/lower?transition=3</td><td>Transition in time in seconds (default 5)</td></tr><tr><td>Text</td><td>FFAA00</td><td>/lower?text=ffaa00</td><td>Text colour in hexadecimal</td></tr><tr><td>BG</td><td>FFFFFF</td><td>/lower?text=ffffff</td><td>Text background colour in hexadecimal</td></tr><tr><td>Key</td><td>00FF00</td><td>/lower?key=00ff00</td><td>Screen background colour in hexadecimal<strong>*</strong></td></tr><tr><td>Fadeout</td><td>0 - n</td><td>/lower?fadeout=3</td><td>Time (in seconds) the lower third displays before fading out</td></tr><tr><td>x</td><td>0-1920<strong>**</strong></td><td></td><td>Horizontal position of titles (in pixels)</td></tr><tr><td>y</td><td>0-1080<strong>**</strong></td><td></td><td>Vertical position of titles (in pixels)</td></tr><tr><td></td><td></td><td></td><td></td></tr></tbody></table>

{% hint style="info" %}
#### Notes

\*Useful for keying and compositing workflows

\*\*Value depends on screen size
{% endhint %}

{% hint style="info" %}
**Note on hexadecimal colours**

The colours in lower thirds are defined in hexadecimal. In short, we use 3 sets of hexadecimal values to define values for Red, Green and Blue.&#x20;

eg: FF0000 would generate a full red colour with no green or blue present

One neat trick is the ability to use a third set to set an alpha channel value. This is very useful for compositing

eg: FF000055 would generate a 30% transparent red.

In doubt, use a [colour picker ](https://image-color.com/color-picker)to help.
{% endhint %}

