---
description: Inject external data to the Ontime presenter view
---

# External data



<figure><img src="../.gitbook/assets/external in editor.jpg" alt=""><figcaption><p>In the editor, we getfeedback on the external data</p></figcaption></figure>

<figure><img src="../.gitbook/assets/external in timer.jpg" alt=""><figcaption><p>The external data is shown in the timer, and can be hidden in the view settings</p></figcaption></figure>

You can inject data into the ontime presenter view. This is useful in cases where you would like another software to push some data to Ontime. ie: a running time from video playback in VLC

## Setting external data

You can set the external fields using both the OSC or WebSocket API, again the APIs are fully compatible

## OSC

| Message                              | Payload       |
| ------------------------------------ | ------------- |
| /ontime/set-external-message-text    | string        |
| /ontime/set-external-message-visible | true \| false |

WebSocket

| Message                      | Payload       |
| ---------------------------- | ------------- |
| set-external-message-text    | string        |
| set-external-message-visible | true \| false |
