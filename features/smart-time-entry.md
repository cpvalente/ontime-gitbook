# Smart Time Entry

{% hint style="info" %}
There are ongoing improvements with the time entry so this documentation will be improved once features go into the build
{% endhint %}

When entering times in an event block ontime makes available a few shortcuts

| Note                                                                                                                                   | Entry                                   | Result                                                      |
| -------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------- | ----------------------------------------------------------- |
| Ontime accepts `.` `,` `:` and `spaces` as separators between hh:mm:ss                                                                 | <p>0.1<br>0 1<br>0:1<br>0,1</p>         | 00:00:01                                                    |
| The keyword `p` returns the end time of the previous event                                                                             | p                                       | <p>(if previous event finishes at 09:00:00)<br>09:00:00</p> |
| Starting a time entry with a + sign, adds the time to the previous event                                                               | +10:10                                  | <p>(if previous event finishes at 09:00:00)<br>09:10:10</p> |
| Any time overflow is considered                                                                                                        | 120                                     | 02:00:00 (120 minutes)                                      |
| Any time overflow is considered                                                                                                        | 0.120                                   | 00:02:00 (120 seconds)                                      |
| 0 append is not necessary                                                                                                              | <p>2.2.2<br>2 2 2<br>2:2:2<br>2,2,2</p> | 02:02:02                                                    |
| You can enter a full time tag without spacers. Note that you need 6 digits for this hhmmss, otherwise it will be considered as minutes | 123456                                  | 12:34:56                                                    |
| You can use a separator as short for 0                                                                                                 | 10: or :10                              | 10:00:00 or 00:10:00                                        |
| A single numeric field is read as minutes                                                                                              | 10                                      | 00:10:00                                                    |
| Two numeric fields are read as minutes:seconds                                                                                         | 1.2                                     | 00:01:02                                                    |
| Tree numeric fields are read as hours:minutes:seconds                                                                                  | <p>1.2.3<br>1 2 3<br>1:2:3<br>1,2,3</p> | 01:02:03                                                    |
