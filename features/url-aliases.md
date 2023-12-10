---
description: Define configurable aliases to ease onsite setup
---

# URL Aliases



Custom aliases allow providing a short name for any ontime URL.

It serves two primary purposes:

* [Providing dynamic URLs for automation or unattended screens](url-aliases.md#url-automation)
* [Simplifying complex URLs](url-aliases.md#simplifying-complex-or-lengthy-urls)

{% hint style="info" %}
The URL Aliases feature means to provide aliases to the parameters section of the url, ie: the bit after ontime's port.\
192.168.10.1:4001/**`THIS-HERE`**

See more in the [URL Aliases Settings](broken-reference)
{% endhint %}

### URL Automation

URL Automation is meant for cases in which we would like to change the URL from Ontime without the need for changes on the consumers of the views.

Consider the case of unattended screens or hardware integrations, where access to change the browser URL may be impractical

{% hint style="info" %}
Example

We could for create an alias for a specific screen that relates to its role, position or type\
eg: `192.168.10.10:4001/thirdfloor`

And in Ontime, configure `thirdfloor` to be an alias to any of the views such as `public` or `backstage`, eventually also changing this throughout the event without need for changes in the third floor viewer
{% endhint %}

### Simplifying complex or lengthy URLs

With the view customisations through URL parameters, the URL can become complex, making recreating and sharing difficult.

Leveraging URL Aliases, you can create a simple URL that can encode a view with given styles.

{% hint style="info" %}
Example

The custom url `lower?bg=ff2&text=f00&size=0.6&transition=5` could be simply called `mylower o`r `shell-event-lower` or quickly recalling
{% endhint %}

