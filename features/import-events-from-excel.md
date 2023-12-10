# Import events from Excel

![Template sheet](<../.gitbook/assets/excel import.png>)

You can import an Excel file containing your rundown. See [the template from the above screenshot ](https://docs.google.com/spreadsheets/d/1TYZhAELRFQa\_2QBO8Q651fMHdem6AXmFLjEDoksJd8Y/edit?usp=sharing)

Ontime allows importing rundown and project data from a spreadsheet.\
For a successful import, there are a few conventions to follow

1. Ontime reads a single worksheet
2. The name of the worksheet and columns is given in the app on import
3. Ontime creates an event for every row on the table
4. All fields in an event (row) are optional. Missing data will be defaulted if needed
5. Time fields not provided will be calculated at import. The times can be either an Excel time field or a short text entry as described in the docs eg: `00:10:15` or `10h15`
6. Any text under a field named **Is Public** will make the event public. We show this as a toggle for simplicity
7. See below the expected data types of the rundown data

### Project data

{% hint style="info" %}
The project data can be defined in the sheet. These fields must have their data on the cell to its right (see screenshot or template)
{% endhint %}

| Field Name          | Data type |
| ------------------- | --------- |
| Project name        | Text      |
| Project description | Text      |
| Public URL          | Text      |
| Backstage URL       | Text      |
| Public Info         | Text      |
| Backstage Info      | Text      |

### Rundown

{% hint style="info" %}
Field names are not case-sensitive. Meaning: both **Event Title** and **event title** would be recognised on import
{% endhint %}

| Event Field | Data Type                                             | Notes                              |
| ----------- | ----------------------------------------------------- | ---------------------------------- |
| Cue         | Text                                                  |                                    |
| Time start  | Excel time \| Text                                    |                                    |
| Time End    | Excel time \| Text                                    |                                    |
| Duration    | Excel time \| Text                                    |                                    |
| Title       | Text                                                  |                                    |
| Subtitle    | Text                                                  |                                    |
| Presenter   | Text                                                  |                                    |
| Note        | Text                                                  |                                    |
| Timer Type  | 'count-down' \| 'count-up' \| 'time-to-end \| 'clock' |                                    |
| End Action  | 'none' \| 'stop' \| 'load-next' \| 'play-next'        |                                    |
| Colour      | Text                                                  |                                    |
| Public      | Text                                                  | any text means the event is public |
| Skip        | Text                                                  | any text means the event is public |



### User Fields

{% hint style="info" %}
There are ten custom fields available.

These can have any name, the names are given to Ontime on import
{% endhint %}

|       |      |
| ----- | ---- |
| user0 | Text |
| user1 | Text |
| user2 | Text |
| user3 | Text |
| user4 | Text |
| user5 | Text |
| user6 | Text |
| user7 | Text |
| user8 | Text |
| user9 | Text |
