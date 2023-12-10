---
description: >-
  The typical screen used onstage. It displays a running timer for current
  speaker. It also contains information on current and next event
---

# Stage Timer

{% hint style="info" %}
https://MY.IP.ADDRESS:4001                       > [Stage view](stage-timer.md)

https://MY.IP.ADDRESS:4001/timer         > [Stage view](stage-timer.md)
{% endhint %}

![Stage timer view](<../.gitbook/assets/101 timer.png>)

### URL Modifiers <a href="#url-modifiers" id="url-modifiers"></a>

We never seemed to agree on the behaviour of the bar.\
Is it a countdown bar? ie: the bar shrinks as the timer progresses\
is it a progress bar? ie: the bar grows as the timer progresses

The conversations become quite philosophical and didnt really produce any good results.&#x20;

Now you can decide this yourself as a URL modifier. The default behaviour is for a progress bar since it had the most traction with the user base

{% hint style="info" %}
**Your bar, your rules**

_Countdown bar_: _/timer?progress=down_

_Progress bar: /timer?progress=up_
{% endhint %}

<table><thead><tr><th width="158.68203347016103"></th><th width="150">Options</th><th width="183.7777777777778">URL</th><th>Actions</th></tr></thead><tbody><tr><td>Progress Bar</td><td>up / down</td><td>/timer?progress=up</td><td>Whether bar counts up or down</td></tr></tbody></table>
