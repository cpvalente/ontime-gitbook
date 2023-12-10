# Sync: Poll ontime status

In the scenario of syncing the state of ontime with 3rd party applications, ontime offers endpoints to poll the app status

### HTTP API

{% swagger method="get" path="/ontime/poll" baseUrl="http://<your_ip>:4001" summary="Returns object containing app timer status" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description=" " %}
```javascript
{
    "clock": 39981051,                  // clock in milliseconds
    "running": 1792,                    // current timer in milliseconds
    "durationSeconds": 1800,            // duration of current event
    "playback": "start",                // playback status
    "title": "Welcome to Ontime",       // current event title
    "presenter": "cpvalente",           // current event presenter 
    "timetag": "00:29:51"               // current timer string
}
```
{% endswagger-response %}
{% endswagger %}

### OSC and Websocket API

You can also poll using both the OSC and WebSocket APIs, [see the definition ](sync-poll-ontime-status.md#osc-and-websocket-api)
