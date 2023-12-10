---
description: A timer to another any scheduled event
---

# Countdown

<div>

<img src="../.gitbook/assets/108 countdown 1 (1).png" alt="Countdown to anything!">

 

<figure><img src="../.gitbook/assets/108 countdown 2.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
https://MY.IP.ADDRESS:4001/countdown > [Countdown](countdown.md)
{% endhint %}

Imagine a case where a particular department in the building needs to keep track of a specific event. eg: the actor dressing room number 3 needs to know when it is his time to enter, he does not concern himself of any other times.

Enter Countdown view!

With this view you can choose any scheduled event, from here, ontime will keep track of its running status and either show the Running timer of the event (if running) or a countdown to the event start

{% hint style="info" %}
When calling the route `<ontime-ip>:4001/countdown` you are able to choose any of the events in the list. From here ontime will follow the event by its ID.&#x20;

You can also use the direct routes `<ontime-ip>:4001/countdown?event=1` to follow an event by its order in the list (subject to change) or `<ontime-ip>:4001/countdown?eventid=test` to follow a specific event regardless of its position

This is a great workflow to pair with [URL aliases](../features/url-aliases.md)
{% endhint %}



Good stuff!
