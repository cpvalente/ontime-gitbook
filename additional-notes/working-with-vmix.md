# Working with vMix

## Control Ontime from vMix

The most straightforward way to get Ontime synced with vMix is by using Ontime's [HTTP API](../control-and-feedback/ontime-apis/http-api.md) which provides easy access to the apps playback functions.

Adapting from [this vMix forum post ](https://forums.vmix.com/posts/t7079-http-command-midi)we see that a workflow could look like:

- [ ] Go to **Settings** - **Scripting** and click **Add**
- [ ] Paste the following and **Save**

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

## Pull Ontime info into vMix

Here's a quick example on how you could bring Ontime event info into vMix

### Show the current Ontime timer in a vMix Title input

**In vMix**

- Click on the **Settings** button at the top right to show the settings window, then click **Web Controller** to show the settings needed.
- Update the following bare-minimum settings, and make a note of the _Web Site Address_ for later.
  - TCP API Enabled: checked
  - if you have a password set, allow _API_ access witout login.
  - Restrict access to LAN only: up to you.
- Create a new Title input, to hold the data:
  - Choose **Add Input**, **Title** then pick a title type, such as _Text Middle Centre_, under **GT Text**.
- Give the Title a name (with no spaces), such as _TIMER_. This isn't necessary, but makes it easier for shows with a large number of inputs. Click on the cog icon of the input to set the name.

**In Ontime**

- In Ontime, click on the **Integrations** icon (the puzzle piece) to access the **Integrations Settings** window.
- Click on the **HTTP Integration** tab, then **On Every Second**, and finally the **Add new** button.
- In the URL box, type: `http://localhost:8088/API/?Function=SetText&Input=TIMER&SelectedName=Message.Text&Value={{human.runningTimer}}`
  - Be sure to use the IP address and Port from vMix (vMix: Settings > Web Controller).
  - `Input=TIMER` can also be the input number such as 'Input=1' if you prefer to use input numbers.
  - `SelectedName=Message.Text` needs to be the name of the text entry within the input (vMix: Right-click the input).
  - Please see the [full list of data](../control-and-feedback/runtime-data.md) you can pull in.
  - You can also call [many different vMix API calls](https://www.vmix.com/help26/DeveloperAPI.html).
- Make sure the button to the right of the URL is on then hit the **Save** button.
- Run a countdown and notice that the time shows up in the TIMER input in vMix

This can be easily adapted using the Ontime HTTP Integration settings, along with your choice of [vMix API calls](https://www.vmix.com/help26/DeveloperAPI.html). For example, you could bring in an event Title and Subtitle into vMix as a Lower Third input.
