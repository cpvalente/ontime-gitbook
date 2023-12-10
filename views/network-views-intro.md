# Network views (Intro)

Any device in the same network with a browser can render the data views designed.

Reaching the different views is possible by navigating to the IP address of the machine that hosts ontime (show in the apps info view) on the **default port 4001** and using the ontime logo on the top right corner to select the desired view. In the examples below MY.IP.ADDRESS should be replaced by the given IP. In the local machine that would be **127.0.0.1**

{% hint style="info" %}
https://MY.IP.ADDRESS:4001                        > [Stage view](stage-timer.md)

https://MY.IP.ADDRESS:4001/minimal      > [Minimal Timer](minimal-timer.md)

https://MY.IP.ADDRESS:4001/sm              > [Stage Manager / Backstage View](backstage-info.md)

https://MY.IP.ADDRESS:4001/public         > [Public / Foyer View](public-info.md)

https://MY.IP.ADDRESS:4001/lower          > [Lower Thirds](lower-thirds.md)

https://MY.IP.ADDRESS:4001/studio         > [Studio Clock](studio-clock.md)

https://MY.IP.ADDRESS:4001/countdown > [Countdown](countdown.md)

https://MY.IP.ADDRESS:4001/cuesheet    > [Cuesheet](cuesheet.md)
{% endhint %}

In case of unnatended machines or automations, it is possible to use a straight URL for every view

There are two main types of views available to be used, **Private Views** and **Public Views**

### Private Views

These refer to all views which would be typically used in a backstage context.&#x20;

* **Stage Timer / Minimal Timer** - Common screen type used for speakers onstage, contains the running timer as well as the ability to receive direct messages from the operator
* **Backstage Info** - An overview of the schedule and ongoing events. Contains also private events, pertinent to backstage only
* **Studio Clock** - A schedule overview with a typical LED studio clock
* **Cuesheet** - A collaborative cuesheet / rundown table with the possibility for custom user fields

### Public Views

These refer to all views which would be typically used in a audience context.&#x20;

* **Public Info** - An overview of the schedule and ongoing events
* **Lower Thirds** - A set of programmable lower third events containing event info.
