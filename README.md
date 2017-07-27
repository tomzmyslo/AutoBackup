# AutoBackup
Launch daemon to trigger backups via `tmutil startbackup` when [Time Machine](https://en.wikipedia.org/wiki/Time_Machine_(macOS)) automatic backups stop working.

This daemon is setup to run a backup every hour from 6:00am to 8:00pm. This works well if you are running backups on Macs in a business environment. Feel free to fork and add backup intervals as needed.

#### Prerequisites
Make sure you meet these requirements before installing the daemon.

* A Mac

* An external hard drive

* The external hard drive is setup as your backup drive

#### Installation
1. Fork and download the repository to your Mac

1. Make any interval changes (*see instructions below*) to the .plist file in your favorite text editor

1. On your Mac, open a new **Terminal** window and type the following command:

    `$ open ~/Library/LaunchAgents`
    
1. Drag a copy of the .plist into the window you opened

1. Open **System Preferences**, select the **Time Machine** pane and disable "automatic backups"

1. Close all open applications and reboot your Mac


#### Interval Format
The following example would add a backup at midnight. Change the hour and minute integer according to your desired backup requirements.
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
