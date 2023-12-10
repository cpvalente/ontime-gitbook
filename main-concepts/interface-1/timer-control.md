---
description: Timer Control allows for control of running timers
---

# Timer Control

![timer control in app](<../../.gitbook/assets/200 editor overview.png>)

#### 3. Timer Control

Timer control is the most important control interface for running your timer.

All actions available here (and more) are also available through [one of the APIs](../../control-and-feedback/ontime-apis/), allowing you to create powerful integrations as eg. [companion ](../../additional-notes/companion-module.md)

component offers control over the playback of the currently selected event (event in green on event list). All the buttons in the interface are also available over the [OSC and Websocket APIs](../../control-and-feedback/ontime-apis/)

* **Start / Next** - When no event is running, Start will start the selected event (or first if there is no selection). Next will start the following event&#x20;
* **Play**
* **Pause**
* **Roll** - Roll is an advanced tool that enables ontime to run unattended. The application will use the system clock to run the events as scheduled. See [Roll](../../features/roll.md)
* **Previous**
* **Next**
* **Unload** - De-selects any running event
* **Reload** - Stops and resets running timer
* **-1 -5 +1 +5** - Increments / decrements currently running timer (time in minutes)

{% hint style="info" %}
Although the options for increment / decrement are limited to 1 and 5 minutes in the app. This limitation does not exist in the [integrations](../../control-and-feedback/ontime-apis/), meaning that an OSC device can increment / decrement any amount of time:

_/ontime/delay 10_\
_/ontime/delay -20_
{% endhint %}

\
