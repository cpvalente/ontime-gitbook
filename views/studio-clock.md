---
description: >-
  A studio clock screen. It displays current time along with running timer and
  information on all events.
---

# Studio Clock

{% hint style="info" %}
https://MY.IP.ADDRESS:4001/studio        > [Studio Clock View](studio-clock.md)
{% endhint %}

![](<../.gitbook/assets/107 studio (1).png>)

{% hint style="info" %}
The **On Air** state can be toggled on / off using either the [OSC ](broken-reference)or [HTTP APIs](../control-and-feedback/ontime-apis/http-api.md)
{% endhint %}

### URL Modifiers

The Studio Clock views are configurable by using URL parameters

{% hint style="info" %}
URL parameters pair great with the [URL Aliases feature](../features/url-aliases.md)
{% endhint %}

| Parameter | Options       | URL                  | Action                 |
| --------- | ------------- | -------------------- | ---------------------- |
| seconds   | true \| false | /studio?seconds=true | Shows seconds in clock |
