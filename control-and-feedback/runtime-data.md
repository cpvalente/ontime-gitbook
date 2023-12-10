# Runtime Data

Ontime broadcasts its state over websockets on port 4001. This allows for integrations to sync to the state of the application. This broadcast happens at least once a second, depending on updates.

See below a full definition of the data that Ontime holds. You would use the Integrations feature to share these.&#x20;

If you prefer looking at code, please follow here

{% hint style="info" %}
The object broadcast object is formatted as below. With the type 'ontime' indicating that this is the application state update

`{`\
&#x20; `type: ontime,`\
&#x20; `payload: <RuntimeState>  (see below)`\
`}`

If you prefer looking at code, please follow

[https://github.com/cpvalente/ontime/blob/master/packages/types/src/definitions/runtime/RuntimeStore.type.ts](https://github.com/cpvalente/ontime/blob/master/packages/types/src/definitions/runtime/RuntimeStore.type.ts)
{% endhint %}

| Key                      | Subkey                | Description                                              | Tyåe                                             |   |
| ------------------------ | --------------------- | -------------------------------------------------------- | ------------------------------------------------ | - |
| **timer**                |                       | **Information related to running timer**                 |                                                  |   |
|                          | clock                 | Time now                                                 | number \| null                                   |   |
|                          | current               | Running countdown                                        | number \| null                                   |   |
|                          | elapsed               | Elapsed time in current timer                            | number \| null                                   |   |
|                          | expectedFinish        | Expected finish for current timer                        | number \| null                                   |   |
|                          | addedTime             | Time added by user\*\*                                   | number \| null                                   |   |
|                          | startedAt             | When did the timer start                                 | number \| null                                   |   |
|                          | finishedAt            | When did the timer go past 0                             | number \| null                                   |   |
|                          | secondaryTimer        | User in roll mode                                        | number \| null                                   |   |
|                          | selectedEventId       | ID of loaded event                                       | string \| null                                   |   |
|                          | duration              | Duration of loaded event                                 | number \| null                                   |   |
|                          | timerType             | How is the time displayed                                | 'count-down' \| 'count-up' \| 'clock'            |   |
|                          | endAction             | What happens when this timer finishes                    | 'none' \| 'stop' \| 'load-next' \| 'play-next'   |   |
| **playback**             |                       | Playback state                                           | 'roll' \| 'play' \| 'pause' \| 'stop' \| 'armed' |   |
| **timerMessage**         |                       | **Information related to Message shown in timer**        |                                                  |   |
|                          | text                  | Text of message                                          | string                                           |   |
|                          | visible               | Whether the message is visible                           | boolean                                          |   |
| **publicMessage**        |                       | **Information related to Message shown in public view**  |                                                  |   |
|                          | text                  | Text of message                                          | string                                           |   |
|                          | visible               | Whether the message is visible                           | boolean                                          |   |
| **lowerMessage**         |                       | **Information related to Message shown in lower thirds** |                                                  |   |
|                          | text                  | Text of message                                          | string                                           |   |
|                          | visible               | Whether the message is visible                           | boolean                                          |   |
| **onAir**                |                       | Whether onAir is active                                  | boolean                                          |   |
| **loaded**               |                       | **Information related to loaded events**                 |                                                  |   |
|                          | numEvents             | Number of timer events                                   | number                                           |   |
|                          | selectedEventIndex    | Index of selected event                                  | number \| null                                   |   |
|                          | selectedEventId       | ID of selected event                                     | string \| null                                   |   |
|                          | selectedPublicEventId | ID of public selected event                              | string \| null                                   |   |
|                          | nextEventId           | ID of next event                                         | string \| null                                   |   |
|                          | nextPublicEventId     | ID of next public event                                  | string \| null                                   |   |
| e**ventNow / eventNext** |                       | **currently loaded event / upcoming event**              |                                                  |   |
|                          | cue                   | Value of cue field                                       | string                                           |   |
|                          | title                 | Value of title field                                     | string                                           |   |
|                          | subtitle              | Value of subtitle field                                  | string                                           |   |
|                          | presenter             | Value of presenter field                                 | string                                           |   |
|                          | note                  | Value of note field                                      | string                                           |   |
|                          | colour                | User defined colour                                      | string                                           |   |
|                          | isPublic              | Whether the event should is public                       | boolean                                          |   |
|                          | delay                 | Any rundown delays affecting the event                   | number                                           |   |
|                          | timeStart             | Scheduled start                                          | number                                           |   |
|                          | timeEnd               | Scheduled end                                            | number                                           |   |
|                          | duration              | Scheduled duration                                       | number                                           |   |
|                          | user0-user9           | User added data to the event \*\*\*                      | string                                           |   |



* All times are in milliseconds from midnight
* \*\* Can be negative
* \*\*\* Not user by ontime

