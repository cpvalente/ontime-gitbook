# Integrations

**Integrations** is a feature to allow Ontime to share its data with other parts of your workflow. Meant for generic software and hardware integrations. This can be set up in the [Integration Settings modal](../main-concepts/interface-1/integration-settings.md)

<div data-full-width="false">

<figure><img src="../.gitbook/assets/212 editor + integrations + osc sett (1).png" alt=""><figcaption><p>OSC Settings</p></figcaption></figure>

 

<figure><img src="../.gitbook/assets/211 editor + integrations + osc int.png" alt=""><figcaption><p>OSC Integration Settings</p></figcaption></figure>

</div>

### The ontime lifecycle

During the running of your event, Ontime server will go through a few lifecycle events.&#x20;

The integration feature allows you to leverage these events to send data&#x20;

* On Load - Triggered when an event is loaded
* On Start - Triggered when an event starts
* On Pause - Triggered when an event is paused
* On Stop - Triggered when playback is stopped
* On Every Second - Triggered once a second (great for sending your timer data out)
* On Finish - Triggered when a timer passes the 0 mark and becomes in overtime

{% hint style="info" %}
Example:

If you add a message to the On Load lifecycle: eg: `/ontime/loaded-event` , you would see this message in the OSC Port you have configured in OSC Settings every time an event is loaded
{% endhint %}

### Using variables in integrations

You can embed data from the application runtime in the message using templates `/your-message/{{ontime-data}} {{ontime-more-data}}`

This means that any of the data described in the [runtime data ](runtime-data.md)is available to be sent as part of the message payload

When the lifecycle event is triggered, your message is parsed, and Ontime places the updated piece of data in place of the template

Extending the example above, you could compose a message that sends the id of the loaded event with

```
/send-this/load-{{loaded.selectedEventIndex}}
```

Inside the template (double brackets), you can add any of the keys described in [runtime data](runtime-data.md). Use the  `.` when referencing a subkey

`{{titlesPublic.noteNext}}`

`{{playback}}`

`{{timer.current}}`



### Human readable data

The above data defined in runtime data will give you the data from Ontime as it is consumed in-app. For example, all times are in milliseconds.

This is great for software - to - software communications, but it might not be ideal if you want to consume the data yourself.

For this use cases, we have defined a small list of human-readable timer values that you can use in your integration messages. The usage would look like

{% hint style="info" %}
\*Timer values will return "null" if no event is loaded
{% endhint %}

| Variable           | Usage                    | Result                                                                |
| ------------------ | ------------------------ | --------------------------------------------------------------------- |
| human.clock        | \{{human.clock\}}        | Current clock in (hh:mm:ss)                                           |
| human.duration     | \{{human.duration\}}     | Duration of current timer in  (hh:mm:ss)\*                            |
| human.expectedEnd  | \{{human.expectedEnd\}}  | Time at which the current event is expected to finish in (hh:mm:ss)\* |
| human.runningTimer | \{{human.runningTimer\}} | Current running timer in (hh:mm:ss)\*                                 |
| human.elapsedTime  | \{{human.elapsedTime\}}  | Elapsed time of current timer in (hh:mm:ss)\*                         |
| human.startedAt    | \{{human.startedAt\}}    | Time when the current time started (hh:mm:ss)\*                       |
