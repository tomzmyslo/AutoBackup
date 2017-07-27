# AutoBackup
Launch daemon to trigger backups via `tmutil startbackup` when [Time Machine](https://en.wikipedia.org/wiki/Time_Machine_(macOS)) automatic backups stop working.

This daemon is setup to run a backup every hour from 6:00am to 8:00pm. This works well if you are running backups on Macs in a business environment. Feel free to fork and add backup intervals as needed.

#### Interval Format
This would add a backup at midnight. Change the hour and minute integer according to your desired backup requirements.
```xml
<dict>
  <key>Hour</key>
  <integer>0</integer>
  <key>Minute</key>
  <integer>0</integer>
</dict>
```
##### *Note:* This daemon requires you to use military time for hours and minutes.

###### _Special thanks to kainjow on the MacRumors Forum who wrote the basis for this code. It can be found [here](https://forums.macrumors.com/threads/time-machine-not-making-automatic-backups.2032122/)._
