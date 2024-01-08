---
description: Sync your rundown to a Google Sheet
---

# Google Sheet

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>Google sheet modal is available in the left app menu</p></figcaption></figure>

Ontime supports the syncing of the rundown to a google sheet

You need to provide Ontime with the necessary permissions. From there, we can read and write to the Google Sheet spreadsheet.

This is ideal for collaboration or extensive data manipulation.



{% hint style="info" %}
**Spreadsheet template**

By duplicating our template, you can get started quicker with using spreadsheets in Ontime.
{% endhint %}

### Step 1 - Upload client secret

You will need to create a token in your Google Account and upload it to Ontime [https://console.cloud.google.com](https://console.cloud.google.com)\


{% hint style="info" %}
#### Create a token in Google Cloud Console

This guide is copied from the Google documentation at [https://console.cloud.google.com](https://console.cloud.google.comhttps/console.cloud.google.com)

* On the **Google Cloud Console**, **Create a Project**, and in the `APIs and services > Enabled APIs and servers`, make sure you enable the **Google Sheets API**.
* Go to [https://console.cloud.google.com/apis/credentials](https://console.cloud.google.com/apis/credentials), click `Create Credentials`, and select `OAuth client ID`.
* Select `Desktop App` as the `Application Type`, and give the app a name.
* Download the file with the `Client ID` and upload it to the Ontime interface.
{% endhint %}

### Step 2 - Authenticate

Once we have the Client ID token Ontime can request Google permission to access the data in the spreadsheet.

For your security, the authentication is kept in memory and wiped when Ontime quits.\
This means that you would need to re-authenticate every time you start Ontime.

### Step 3 - Add Document ID

You will need to provide Ontime with the ID of the document to import.

The Document ID is available in the URL after the `d`, such as `https://docs.google.com/spreadsheets/d/<Document ID>/edit#gid=0`

Click the `Connect` button to establish connection and get the worksheet options

### Step 4 - Select the worksheet

Once connected, the dropdown will populate with a list of worksheets available in the document.

Select the one with your rundown.

### Step 5 - Upload / Download at will

Now Ontime is connected to your Google Sheet document.

You can get the data from your Google Sheet into Ontime by pressing the `Download` button at any time.

You can also push your local data from Ontime to the Google Sheet by clicking the `Upload` button.
