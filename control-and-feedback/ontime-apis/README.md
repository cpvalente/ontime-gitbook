# Ontime APIs

{% hint style="info" %}
Ontime has a strong focus on integrations. We want ontime to play well into your workflow.&#x20;

Have an idea of how could this be better? Let's chat! Get in touch on email [mail@getontime.no ](<mailto:mail@getontime.no >)or [open an issue in GitHub](https://github.com/cpvalente/ontime/issues)
{% endhint %}

We would like you to [build your own views ](../../features/make-your-own-viewer.md)and your own controllers, and let Ontime handle the distribution and time-keeping

The Ontime app window, as well as the editor page, communicate with ontime through an open API. You can leverage this API yourself to extend the feature set or integrate into your workflow



The OSC and Websocket API allow for low latency communication to ontime server. Both APIs are identical, so it is up to you to choose the most convenient protocol

The [HTTP API ](http-api.md)has access to a smaller subset of features

### OSC and WebSocket API

{% hint style="info" %}
Maybe you know your way around code? That is the best and most up-to-date source!

[https://github.com/cpvalente/ontime/blob/master/apps/server/src/controllers/integrationController.ts](https://github.com/cpvalente/ontime/blob/master/apps/server/src/controllers/integrationController.ts)
{% endhint %}

| Message                    | Payload                        | Description                                                 | Return                                                           |
| -------------------------- | ------------------------------ | ----------------------------------------------------------- | ---------------------------------------------------------------- |
| test-ontime                |                                |                                                             | "hello"                                                          |
| ontime-poll                |                                | Returns the entire runtime state                            | { topic: "poll", payload: [\<RuntimeData>](../runtime-data.md) } |
| set-onair                  | "false" \| "true" \| undefined | Sets on air to given value, toggle if none is given         |                                                                  |
| onair                      |                                | Set on air to **true**                                      |                                                                  |
| offair                     |                                | Set on air to **false**                                     |                                                                  |
| set-timer-message-text     | string                         | Sets text of timer message                                  |                                                                  |
| set-timer-message-visible  | "false" \| "true" \| undefined | Sets visibility to given value, toggle if none is given     |                                                                  |
| set-public-message-text    | string                         | Sets text of public message                                 |                                                                  |
| set-public-message-visible | "false" \| "true" \| undefined | Sets visibility to given value, toggle if none is given     |                                                                  |
| set-lower-message-text     | string                         | Sets text of lower message                                  |                                                                  |
| set-lower-message-visible  | "false" \| "true" \| undefined | Sets visibility to given value, toggle if none is given     |                                                                  |
| start                      |                                | Starts selected timer                                       |                                                                  |
| start-next                 |                                | Loads and starts next timer in rundown                      |                                                                  |
| startindex                 | number                         | Loads and starts event at index (first event is 1)          |                                                                  |
| startid                    | string                         | Loads and starts event with given ID                        |                                                                  |
| startcue                   | string                         | Loads and starts event with given cue                       |                                                                  |
| pause                      |                                | Pauses playback                                             |                                                                  |
| previous                   |                                | Loads previous event                                        |                                                                  |
| next                       |                                | Loads next event                                            |                                                                  |
| stop                       |                                | Stops playback                                              |                                                                  |
| reload                     |                                | Reloads selected event                                      |                                                                  |
| roll                       |                                | Sets playback mode to roll                                  |                                                                  |
| delay                      | number                         | Adds a delay of given time to a playing event               |                                                                  |
| loadindex                  | number                         | Loads event at given index (first event is 1)               |                                                                  |
| loadid                     | number                         | Loads event at given ID                                     |                                                                  |
| loadcue                    | string                         | Loads event with given cue                                  |                                                                  |
| get-playback               |                                | Returns playback portion [Runtime Data](../runtime-data.md) | {topic: "playback", payload: \<RuntimeData.playback>}            |
| get-timer                  |                                | Returns timer portion [Runtime Data](../runtime-data.md)    | {topic: "timer", payload: \<RuntimeData.timer>}                  |

