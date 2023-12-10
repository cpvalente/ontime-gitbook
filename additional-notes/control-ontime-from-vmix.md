# Control Ontime from vMix

The most straightforward way to get Ontime synced with vMix is probably by using Ontime's [HTTP API](../control-and-feedback/ontime-apis/http-api.md) which provides easy access to the apps playback functions.&#x20;

Adapting from [this vMix forum post ](https://forums.vmix.com/posts/t7079-http-command-midi)we see that a workflow could look like:

* [ ] Go to **Settings** - **Scripting** and click **Add**
* [ ] Paste the following and **Save**

{% code lineNumbers="true" fullWidth="false" %}
```vbnet
' This code creates a POST request to start an event with id 4b044
Dim request As WebRequest
request = WebRequest.Create("http://localhost:4001/playback/start?eventId=4b044")
Dim response As WebResponse

request.Method = "POST"
request.ContentType = "application/x-www-form-urlencoded"

Dim stream As Stream = request.GetRequestStream()
stream.Close()

response = request.GetResponse()
Dim sr As New StreamReader(response.GetResponseStream())

```
{% endcode %}

{% hint style="info" %}
Remember to change ONTIME-IP with the IP address of the machine running the Ontime App (127.0.0.1 if the same)
{% endhint %}

From here you should be able to add the script as needed. Please follow vMix documentation for next steps
